---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993356"
---
# Remove-AzServiceBusSubscription

## SYNOPSIS
지정된 Service Bus 네임스페이스에서 토픽에 대한 구독을 제거합니다.

## 구문

### SubscriptionPropertiesSet(기본값)
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SubscriptionInputObjectSet
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SubscriptionResourceIdSet
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzServiceBusSubscription** cmdlet은 지정된 Service Bus 네임스페이스에서 토픽에 대한 구독을 제거합니다.

## 예제

### 예제 1
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

지정된 Service Bus 네임스페이스의 `SB-TopicSubscription-Example1` 토픽에 대한 `SB-Topic_exampl1` 구독을 `SB-Example1` 제거합니다.

### 예제 2: InputObject - 변수 사용:
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### 예제 3: InputObject - 배관 사용:
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### 예제 4: ResourceId - 변수 사용:
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### 예제 5: ResourceId - 문자열 값 사용:
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

-ResourceId 매개 변수에 대한 ARM/string의 $resourceid ID를 통해 제공된 구독을 제거합니다. 

## 매개 변수

### -AsJob
백그라운드에서 cmdlet 실행

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
Service Bus 구독 개체

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
구독 이름

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -네임스페이스
네임스페이스 이름

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
명령이 성공하면 이를 지정하면 true가 반환됩니다.

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

### -ResourceGroupName
리소스 그룹의 이름

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Service Bus 구독 리소스 ID

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Topic
토픽 이름

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes

## 출력

### System.Boolean

## 참고 사항

## 관련 링크
