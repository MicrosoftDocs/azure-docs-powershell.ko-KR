---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957584"
---
# New-AzDiskUpdateConfig

## SYNOPSIS
구성 가능한 디스크 업데이트 개체를 만듭니다.

## 구문

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzDiskUpdateConfig** cmdlet은 구성 가능한 디스크 업데이트 개체를 만듭니다.

## 예제

### 예제 1
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

첫 번째 명령은 저장소 계정 유형에 크기가 10GB인 로컬 빈 디스크 Premium_LRS 만듭니다. 또한 Windows OS 유형을 설정하고 암호화 설정을 사용할 수 있습니다. 두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대한 디스크 암호화 키 및 키 암호화 키 설정을 설정합니다.
마지막 명령은 디스크 업데이트 개체를 사용하며 리소스 그룹 'ResourceGroup01'에서 'Disk01'으로 기존 디스크를 업데이트합니다.

### 예제 2
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

이 명령은 리소스 그룹 'ResourceGroup01'의 이름 'Disk01'을 사용하여 기존 디스크를 10GB 디스크 크기로 업데이트합니다.

## 매개 변수

### -BurstingEnabled
디스크의 프로비전된 성능 대상을 초과하여 버스트할 수 있습니다. 버스팅은 기본적으로 사용하지 않도록 설정되어 있습니다. Ultra 디스크에는 적용되지 않습니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -DiskAccessId
{{ DiskAccessId 설명 }} 채우기

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskEncryptionKey
디스크의 디스크 암호화 키 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskEncryptionSetId
미사용 암호화를 사용하도록 설정하는 데 사용할 디스크 암호화 집합의 리소스 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskIOPSReadOnly
공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 IOPS 수입니다. 한 작업은 4k에서 256k 사이를 전송할 수 있습니다.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskIOPSReadWrite
이 디스크에 허용되는 IOPS의 수입니다. UltraSSD 디스크에 대해만 설정이 됩니다. 한 작업은 4k에서 256k 사이를 전송할 수 있습니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskMBpsReadOnly
공유 디스크를 ReadOnly로 탑재하는 모든 VM에서 허용되는 총 MBps().입니다. MBps는 초당 수백만의 bytes를 의미합니다. 여기서 MB는 ISO(10의 파워)를 사용하는 것입니다.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskMBpsReadWrite
이 디스크에 허용되는 대역폭; UltraSSD 디스크에 대해만 설정이 됩니다. MBps는 초당 수백만의 bytes를 의미합니다. 여기서 MB는 ISO(10의 파워)를 사용하는 것입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeGB
디스크 크기를 GB로 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionSettingsEnabled
암호화 설정을 사용하도록 설정합니다.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionType
디스크의 데이터를 암호화하는 데 사용되는 키 유형입니다.  사용 가능한 값은 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyEncryptionKey
디스크의 키 암호화 키를 지정합니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxSharesCount
디스크에 동시에 연결할 수 있는 VM의 최대 수입니다. 하나 이상의 값은 동시에 여러 VM에 탑재할 수 있는 디스크를 나타냅니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkAccessPolicy
{{ NetworkAccessPolicy 설명 }} 채우기

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OsType
OS 유형을 지정합니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuName
저장소 계정의 Sku 이름을 지정합니다.  사용 가능한 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS 및 UltraSSD_LRS.  UltraSSD_LRS CreateOption 매개 변수에 대한 빈 값에만 사용할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
해시 테이블의 형태로 키 값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
디스크의 성능 계층입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Int32

### System.Collections.Hashtable

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference

### Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate

## 참고 사항

## 관련 링크
