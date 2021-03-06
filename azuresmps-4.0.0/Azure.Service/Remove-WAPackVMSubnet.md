---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047407"
---
# Remove-WAPackVMSubnet

## SYNOPSIS
가상 컴퓨터 서브넷 개체를 제거 합니다.

## 구문과

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**Remove-WAPackVMSubnet** cmdlet은 가상 컴퓨터 서브넷 개체를 제거 합니다.

## 예제의

### 예제 1: 가상 컴퓨터 서브넷 제거
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

첫 번째 명령은 **Get-help Apackvmsubnet** cmdlet을 사용 하 여 ContosoVMSubnet01 이라는 가상 컴퓨터 서브넷을 가져온 다음 해당 개체를 $VMSubnet 변수에 저장 합니다.

두 번째 명령은 $VMSubnet에 저장 된 가상 컴퓨터 서브넷을 제거 합니다.
명령에서 확인 하 라는 메시지를 표시 합니다.

### 예제 2: 확인 하지 않고 가상 컴퓨터 제거
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

첫 번째 명령은 **Get-WAPackVMSubnet** cmdlet을 사용 하 여 ContosoVMSubnet02 이라는 클라우드 서비스를 가져온 다음 해당 개체를 $VMSubnet 변수에 저장 합니다.

두 번째 명령은 $VMSubnet에 저장 된 가상 컴퓨터 서브넷을 제거 합니다.
이 명령에는 *Force* 매개 변수가 포함 됩니다.
명령에 확인 메시지가 표시 되지 않습니다.

## 변수

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMSubnet
가상 컴퓨터 서브넷을 지정 합니다.
가상 컴퓨터 서브넷을 얻으려면 **Get WAPackVMSubnet** cmdlet을 사용 합니다.

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-WAPackVMSubnet](./Get-WAPackVMSubnet.md)

[New-WAPackVMSubnet](./New-WAPackVMSubnet.md)


