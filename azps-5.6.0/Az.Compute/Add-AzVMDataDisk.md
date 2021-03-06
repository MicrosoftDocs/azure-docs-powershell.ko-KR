---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 685a1768dac652b3981bd081a2f8b29997c08639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981163"
---
# Add-AzVMDataDisk

## SYNOPSIS
가상 머신에 데이터 디스크를 추가합니다.

## 구문

### VmNormalDiskParameterSetName(기본값)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzVMDataDisk** cmdlet은 가상 머신에 데이터 디스크를 추가합니다.
가상 머신을 만들 때 데이터 디스크를 추가하거나 기존 가상 머신에 데이터 디스크를 추가할 수 있습니다.

## 예제

### 예제 1: 새 가상 머신에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

첫 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
다음 세 가지 명령은 3개의 데이터 디스크의 경로를 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03 변수에 할당합니다.
이 방법은 다음 명령의 가독성을 위한 것입니다.
마지막 3개의 명령은 각 명령에 저장된 가상 머신에 데이터 디스크를 $VirtualMachine.
명령은 디스크의 이름 및 위치 및 디스크의 다른 속성을 지정합니다.
각 디스크의 URI는 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03에 저장됩니다.

### 예제 2: 기존 가상 머신에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

첫 번째 명령은 [Get-AzVM](./Get-AzVM.md) cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.
명령은 가상 머신을 $VirtualMachine 저장합니다.
두 번째 명령은 데이터 디스크를 에 저장된 가상 머신에 $VirtualMachine.
마지막 명령은 ResourceGroup11에 저장된 가상 머신의 $VirtualMachine 업데이트합니다.

### 예제 3: 일반화된 사용자 이미지에서 새 가상 머신에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

첫 번째 명령은 가상 머신 개체를 만들고 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
다음 두 명령은 데이터 이미지 및 데이터 디스크에 대한 경로를 각각 $DataImageUri $DataDiskUri 할당합니다.
이 방법은 다음 명령의 가독성을 향상시키는 데 사용됩니다.
최종 명령은 데이터 디스크를 데이터 디스크에 저장된 가상 머신에 $VirtualMachine.
명령은 디스크 및 디스크의 다른 속성에 대한 이름과 위치를 지정합니다.

### 예제 4: 특수 사용자 이미지에서 새 가상 머신에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

첫 번째 명령은 가상 머신 개체를 만들고 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
다음 명령은 데이터 디스크의 경로를 변수에 $DataDiskUri 할당합니다.
이 방법은 다음 명령의 가독성을 향상시키는 데 사용됩니다.
최종 명령은 데이터 디스크를 에 저장된 가상 머신에 $VirtualMachine.
명령은 디스크의 이름 및 위치 및 디스크의 다른 속성을 지정합니다.

## 매개 변수

### -캐싱
디스크의 캐싱 모드를 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- ReadOnly
- ReadWrite
- None 기본값은 ReadWrite입니다.
이 값을 변경하면 가상 머신이 다시 시작됩니다.
이 설정은 디스크의 일관성 및 성능에 영향을 미치게 됩니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들고, 빈 디스크를 생성하거나, 기존 디스크를 연결하는지 여부를 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 연결합니다.
특수 디스크에서 가상 머신을 만들 수 있는 이 옵션을 지정합니다.
이 옵션을 지정하는 경우 *SourceImageUri* 매개 변수를 지정하지 않습니다.
*VhdUri는* Azure 플랫폼에서 VHD(가상 하드 디스크)의 위치를 가상 머신에 데이터 디스크로 연결하기 위해 필요한 모든 것입니다.
- 비어 있습니다.
빈 데이터 디스크를 만들 수 있습니다.
- FromImage.
일반화된 이미지 또는 디스크에서 가상 머신을 만들 수 있는 이 옵션을 지정합니다.
이 옵션을 지정하는 경우 Azure 플랫폼에 데이터 디스크로 연결할 VHD의 위치를 알려 주기 위해 *SourceImageUri* 매개 변수도 지정해야 합니다.
*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장될 위치를 식별하는 위치로 사용됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId
고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.  이는 관리 디스크에만 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
가상 머신에 연결할 빈 디스크의 크기를 기가바이트로 지정합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
데이터 디스크에 대한 LUN(논리 단위 번호)을 지정합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
관리 디스크의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
추가할 데이터 디스크의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
이 cmdlet이 연결한 디스크의 원본 URI를 지정합니다.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
관리 디스크의 저장소 계정 유형을 지정합니다.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
플랫폼 이미지 또는 사용자 이미지를 사용할 때 만들 가상 하드 디스크(VHD) 파일에 대한 URI(균일한 리소스 식별자)를 지정합니다.
이 cmdlet은 이미지 이진 큰 개체(Blob)를 이 위치에 복사합니다.
가상 머신을 시작할 위치입니다.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
데이터 디스크를 추가할 로컬 가상 머신 개체를 지정합니다.
**Get-AzVM** cmdlet을 사용하여 가상 머신 개체를 얻을 수 있습니다.
**New-AzVMConfig** cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
관리되는 데이터 디스크에서 WriteAccelerator를 사용하도록 설정하거나 사용하지 않도록 설정해야 하는지 여부를 지정합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## 참고 사항

## 관련 링크

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
