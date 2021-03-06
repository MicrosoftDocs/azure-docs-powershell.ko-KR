---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/get-azpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyEvent.md
ms.openlocfilehash: 7c9ee7af59acc90fba6a17e78ffd3dfc4822472d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989170"
---
# Get-AzPolicyEvent

## SYNOPSIS
리소스가 만들어지거나 업데이트될 때 생성된 정책 평가 이벤트를 얻습니다.

## 구문

### SubscriptionScope(기본값)
```
Get-AzPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>] [-OrderBy <String>]
 [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>]
 [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
리소스가 만들어지거나 업데이트될 때 생성된 정책 평가 이벤트를 얻습니다. 정책 이벤트 레코드는 지정된 시간 간격(기본값에서 마지막 날)에 따라 다양한 범위에서 검색할 수 있습니다. 결과를 필터링하고 그룹화하고 그룹 집계를 계산할 수 있습니다.

## 예제

### 예제 1: 현재 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.

### 예제 2: 지정된 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

지정된 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 3: 관리 그룹 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -ManagementGroupName "myManagementGroup"
```

지정된 관리 그룹 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 4: 현재 구독의 리소스 그룹 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup"
```

지정된 리소스 그룹 내의 모든 리소스(현재 세션 컨텍스트의 구독)에 대한 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 5: 지정된 구독의 리소스 그룹 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

지정된 리소스 그룹 내의 모든 리소스(지정된 구독에서)에 대한 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 6: 리소스에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

지정된 리소스에 대한 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 7: 현재 구독에서 정책 집합 정의에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 집합 정의(현재 세션 컨텍스트의 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 8: 지정된 구독에서 정책 집합 정의에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 집합 정의(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 9: 현재 구독에서 정책 정의에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 정의(현재 세션 컨텍스트의 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 10: 지정된 구독에서 정책 정의에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

지정된 정책 정의(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.

### 예제 11: 현재 구독에서 정책 할당에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정된 정책 할당(현재 세션 컨텍스트의 구독에 있는 구독에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 12: 지정된 구독에서 정책 할당에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정된 정책 할당(지정된 구독에 있는)의 영향이 있는 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.

### 예제 13: 현재 구독의 지정된 리소스 그룹에서 정책 할당에 대한 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

지정된 정책 할당(현재 세션 컨텍스트의 구독의 리소스 그룹에 있는)의 영향을 받을 모든 리소스(현재 세션 컨텍스트의 테넌트 내)에 대해 마지막 날에 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 14: OrderBy, Top 및 Select 쿼리 옵션을 사용하여 현재 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다. 명령은 타임스탬프 및 정책 할당 이름 속성에 따라 결과를 순서대로 지정하고 해당 순서대로 나열된 상위 5개만 사용됩니다.
또한 각 레코드에 대한 열의 하위 집합만 나열하기로 선택합니다.

### 예제 15: 시작 및 쿼리 옵션으로 현재 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

현재 세션 컨텍스트에서 구독 내의 모든 리소스에 대해 지정된 날짜 범위 내에서 생성된 정책 이벤트 레코드를 얻습니다.

### 예제 16: 필터 쿼리 옵션을 사용하여 현재 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다.
명령은 정책 정의 작업(거부 또는 감사 작업 포함) 및 리소스 위치(eastus 위치 제외)에 따라 필터링하여 반환되는 결과를 제한합니다.

### 예제 17: 행 수 집계 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻습니다.
```powershell
PS C:\> Get-AzPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드의 수를 얻습니다.
명령은 추가Properties 속성 내에서 반환되는 정책 이벤트 레코드의 수만 반환합니다.

### 예제 18: 집계를 사용하여 그룹 지정 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다. 명령은 정책 정의 작업(감사 및 거부 이벤트만 포함)에 따라 필터링하여 반환되는 결과를 제한합니다.
정책 할당, 정책 정의, 정책 정의 작업 및 리소스 ID에 따라 결과를 그룹화하고, 추가Properties 속성 내에서 반환되는 각 그룹의 레코드 수를 계산합니다.
내선 순서로 개수 집계를 통해 결과를 순서대로 순서를 정하고, 해당 순서대로 나열된 상위 5개만이 표시됩니다.

### 예제 19: 집계 없이 그룹 지정 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻기
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다. 명령은 정책 정의 작업(감사 및 거부 이벤트만 포함)에 따라 필터링하여 반환되는 결과를 제한합니다.
리소스 ID를 기반으로 결과를 그룹화합니다. 그러면 하나 이상의 감사 또는 거부 정책에 대한 정책 이벤트를 생성한 구독 내의 모든 리소스 목록을 생성합니다.

### 예제 20: 여러 그룹 지정 적용을 사용하여 현재 구독 범위에서 정책 이벤트 얻습니다.
```powershell
PS C:\> Get-AzPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

현재 세션 컨텍스트의 구독 내의 모든 리소스에 대해 마지막 날에 생성된 정책 이벤트 레코드를 를 선택합니다. 명령은 정책 정의 작업(거부 이벤트만 포함)에 따라 필터링하여 반환되는 결과를 제한합니다.
정책 할당, 정책 정의 및 리소스 ID를 기준으로 결과를 먼저 그룹화합니다. 그런 다음 리소스 ID를 제외한 동일한 속성으로 이 그룹화의 결과를 더 그룹화하고, 이러한 각 그룹의 레코드 수를 계산합니다. 이는 AdditionalProperties 속성 내에서 반환됩니다.
내선 순서로 개수 집계를 통해 결과를 순서대로 순서를 정하고, 해당 순서대로 나열된 상위 5개만이 표시됩니다.
이렇게 하여 거부된 리소스 수가 가장 많은 상위 5개 거부 정책을 생성합니다.

## 매개 변수

### -적용
OData 표기어를 사용하여 집계에 식을 적용합니다.

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

### -Filter
OData 표기어를 사용하여 식 필터링

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

### -From
쿼리할 간격의 시작 시간을 지정하는 ISO 8601 서식 타임스탬프입니다.
지정하지 않으면 기본값은 'To' 매개 변수 값에서 1일을 1일로 입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
관리 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
OData 표기어를 사용하여 식 순서를 정합니다.
선택적 'desc'(기본값) 또는 'asc'가 있는 하나 이상의 콤마로 구분된 열 이름입니다.

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

### -PolicyAssignmentName
정책 할당 이름입니다.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
정책 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
정책 집합 정의 이름입니다.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Select
OData 표기식을 사용하여 식을 선택합니다.
하나 이상의 콤마로 구분된 열 이름입니다.
각 레코드의 열을 요청된 열로 제한합니다.

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

### -SubscriptionId
구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
쿼리할 간격의 종료 시간을 지정하는 ISO 8601 서식 타임스탬프입니다.
지정하지 않으면 기본적으로 요청 시간으로 설정됩니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
반환할 최대 레코드 수입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
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

### System.String

## 출력

### Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent

## 참고 사항

## 관련 링크
