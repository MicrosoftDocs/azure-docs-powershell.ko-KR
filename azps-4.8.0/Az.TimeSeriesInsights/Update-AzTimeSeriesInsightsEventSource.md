---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204179"
---
# <span data-ttu-id="6a794-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="6a794-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="6a794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a794-102">SYNOPSIS</span></span>
<span data-ttu-id="6a794-103">지정 된 구독, 리소스 그룹 및 환경에서 지정한 이름으로 이벤트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="6a794-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a794-104">SYNTAX</span></span>

### <span data-ttu-id="6a794-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a794-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6a794-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a794-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a794-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6a794-107">DESCRIPTION</span></span>
<span data-ttu-id="6a794-108">지정 된 구독, 리소스 그룹 및 환경에서 지정한 이름으로 이벤트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="6a794-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6a794-109">EXAMPLES</span></span>

### <span data-ttu-id="6a794-110">예제 1: 이름별로 지정 된 이벤트 원본 업데이트</span><span class="sxs-lookup"><span data-stu-id="6a794-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="6a794-111">이 명령은 특정 이벤트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="6a794-112">예제 3: 개체 별로 지정 된 이벤트 원본 업데이트</span><span class="sxs-lookup"><span data-stu-id="6a794-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="6a794-113">이 명령은 특정 이벤트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="6a794-114">변수</span><span class="sxs-lookup"><span data-stu-id="6a794-114">PARAMETERS</span></span>

### <span data-ttu-id="6a794-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a794-115">-DefaultProfile</span></span>
<span data-ttu-id="6a794-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-117">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="6a794-117">-EnvironmentName</span></span>
<span data-ttu-id="6a794-118">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a794-119">-InputObject</span></span>
<span data-ttu-id="6a794-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6a794-121">-Name</span></span>
<span data-ttu-id="6a794-122">지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a794-123">-ResourceGroupName</span></span>
<span data-ttu-id="6a794-124">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a794-125">-SubscriptionId</span></span>
<span data-ttu-id="6a794-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-127">태그</span><span class="sxs-lookup"><span data-stu-id="6a794-127">-Tag</span></span>
<span data-ttu-id="6a794-128">이벤트 원본에 대 한 추가 속성의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-128">Key-value pairs of additional properties for the event source.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a794-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6a794-129">-Confirm</span></span>
<span data-ttu-id="6a794-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a794-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a794-131">-WhatIf</span></span>
<span data-ttu-id="6a794-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a794-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a794-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a794-134">CommonParameters</span></span>
<span data-ttu-id="6a794-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a794-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a794-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a794-137">입력</span><span class="sxs-lookup"><span data-stu-id="6a794-137">INPUTS</span></span>

### <span data-ttu-id="6a794-138">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="6a794-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6a794-139">출력</span><span class="sxs-lookup"><span data-stu-id="6a794-139">OUTPUTS</span></span>

### <span data-ttu-id="6a794-140">Api20200515. IEventSourceResource에 대 한 정보를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="6a794-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="6a794-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6a794-141">NOTES</span></span>

<span data-ttu-id="6a794-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="6a794-142">ALIASES</span></span>

<span data-ttu-id="6a794-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6a794-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a794-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a794-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a794-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a794-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a794-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a794-147">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6a794-148">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="6a794-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6a794-149">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6a794-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6a794-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a794-151">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6a794-152">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6a794-153">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6a794-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6a794-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a794-154">RELATED LINKS</span></span>
