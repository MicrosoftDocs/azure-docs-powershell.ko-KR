---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: bce5110a4aa03686b8ae38ee03ea853bc6c89949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994196"
---
# Get-AzMapsAccountKey

## SYNOPSIS
계정에 대한 API 키를 얻습니다.
이러한 키는 Azure Maps에 대한 후속 호출에 사용되는 인증 메커니즘입니다.

## 구문

### NameParameterSet(기본값)
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObjectParameterSet
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
Get-AzMapsAccountKey cmdlet은 프로비전된 Azure Maps 계정에 대한 API 키를 얻습니다.
Azure Maps 계정에는 기본 및 보조 API 키가 두 개 있습니다.
키를 사용하면 Azure Maps 계정 엔드포인트와 상호 작용할 수 있습니다.
키를 New-AzMapsAccountKey(New-AzMapsAccountKey.md)를 사용하여 키를 다시 생성합니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

리소스 그룹 MyResourceGroup에서 MyAccount라는 계정에 대한 키를 반환합니다.

### 예제 2
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

지정된 Azure Maps 계정에 대한 키를 반환합니다.

## 매개 변수

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

### -InputObject
Get-AzMapsAccount에서 파이프된 맵 계정입니다.

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
계정 이름을 매핑합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
계정 ResourceId를 매핑합니다.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Maps.Models.PSMapsAccount

## 출력

### Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys

## 참고 사항

## 관련 링크
