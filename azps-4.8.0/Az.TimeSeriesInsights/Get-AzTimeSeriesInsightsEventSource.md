---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214671"
---
# <span data-ttu-id="6b3af-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="6b3af-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="6b3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b3af-102">SYNOPSIS</span></span>
<span data-ttu-id="6b3af-103">지정한 환경에서 지정 된 이름의 이벤트 소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="6b3af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b3af-104">SYNTAX</span></span>

### <span data-ttu-id="6b3af-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b3af-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b3af-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6b3af-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b3af-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b3af-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b3af-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6b3af-108">DESCRIPTION</span></span>
<span data-ttu-id="6b3af-109">지정한 환경에서 지정 된 이름의 이벤트 소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="6b3af-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6b3af-110">EXAMPLES</span></span>

### <span data-ttu-id="6b3af-111">예제 1: 지정 된 환경에 모든 이벤트 원본 나열</span><span class="sxs-lookup"><span data-stu-id="6b3af-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="6b3af-112">이 명령은 지정 된 환경에 해당 하는 모든 이벤트 원본을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="6b3af-113">예제 2: 이름별로 지정 된 이벤트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b3af-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="6b3af-114">이 명령은 특정 이벤트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="6b3af-115">예제 3: 개체 별로 지정 된 이벤트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b3af-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="6b3af-116">이 명령은 특정 이벤트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="6b3af-117">변수</span><span class="sxs-lookup"><span data-stu-id="6b3af-117">PARAMETERS</span></span>

### <span data-ttu-id="6b3af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b3af-118">-DefaultProfile</span></span>
<span data-ttu-id="6b3af-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b3af-120">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="6b3af-120">-EnvironmentName</span></span>
<span data-ttu-id="6b3af-121">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3af-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b3af-122">-InputObject</span></span>
<span data-ttu-id="6b3af-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b3af-124">-이름</span><span class="sxs-lookup"><span data-stu-id="6b3af-124">-Name</span></span>
<span data-ttu-id="6b3af-125">지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b3af-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b3af-127">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3af-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b3af-128">-SubscriptionId</span></span>
<span data-ttu-id="6b3af-129">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b3af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b3af-130">CommonParameters</span></span>
<span data-ttu-id="6b3af-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b3af-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b3af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b3af-133">입력</span><span class="sxs-lookup"><span data-stu-id="6b3af-133">INPUTS</span></span>

### <span data-ttu-id="6b3af-134">ITimeSeriesInsightsIdentity (Microsoft. PowerShell. i m m)</span><span class="sxs-lookup"><span data-stu-id="6b3af-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="6b3af-135">출력</span><span class="sxs-lookup"><span data-stu-id="6b3af-135">OUTPUTS</span></span>

### <span data-ttu-id="6b3af-136">Api20200515. IEventSourceResource에 대 한 정보를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="6b3af-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="6b3af-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6b3af-137">NOTES</span></span>

<span data-ttu-id="6b3af-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="6b3af-138">ALIASES</span></span>

<span data-ttu-id="6b3af-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6b3af-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b3af-140">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b3af-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b3af-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b3af-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b3af-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b3af-143">`[AccessPolicyName <String>]`: 액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="6b3af-144">`[EnvironmentName <String>]`: 환경 이름</span><span class="sxs-lookup"><span data-stu-id="6b3af-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="6b3af-145">`[EventSourceName <String>]`: 지정 된 환경과 연결 된 시계열 Insights 이벤트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="6b3af-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6b3af-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b3af-147">`[ReferenceDataSetName <String>]`: 참조 데이터 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="6b3af-148">`[ResourceGroupName <String>]`: Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="6b3af-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6b3af-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6b3af-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b3af-150">RELATED LINKS</span></span>
