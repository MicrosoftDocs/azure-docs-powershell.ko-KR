---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 3a715e0c4c2540a0905035afabc15ef46caa32bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991298"
---
# Get-AzEventGridTopicType

## SYNOPSIS
Azure Event Grid에서 지원하는 토픽 형식에 대한 세부 정보를 얻습니다.

## 구문

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
Azure Event Grid에서 지원하는 토픽 형식의 세부 정보를 얻습니다.
토픽 형식 이름을 지정하면 해당 토픽 형식에 대한 세부 정보가 반환됩니다.
토픽 형식 이름을 지정하지 않으면 모든 토픽 형식에 대한 세부 정보가 반환됩니다.
IncludeEventTypes를 지정하는 경우 각 토픽 유형에서 지원되는 이벤트 유형에 대한 정보가 응답에 포함됩니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

항목 형식의 목록을 얻습니다.

### 예제 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

StorageAccounts 토픽 유형에 대한 정보를 얻습니다.

### 예제 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

StorageAccounts에서 지원하는 이벤트 형식을 포함하여 StorageAccounts 토픽 형식에 대한 정보를 얻습니다.

## 매개 변수

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -IncludeEventTypeData
지정한 경우 응답에는 토픽 형식에서 지원되는 이벤트 형식이 포함됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
EventGrid 토픽 형식 이름입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo

## 참고 사항

## 관련 링크
