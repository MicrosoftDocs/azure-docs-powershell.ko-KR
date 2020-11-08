---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214022"
---
# <span data-ttu-id="f8ff4-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="f8ff4-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="f8ff4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ff4-103">자격 증명 모음에 있는 Azure Site Recovery 이벤트의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="f8ff4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8ff4-104">SYNTAX</span></span>

### <span data-ttu-id="f8ff4-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8ff4-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8ff4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ff4-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8ff4-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="f8ff4-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8ff4-108">ByName</span><span class="sxs-lookup"><span data-stu-id="f8ff4-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8ff4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f8ff4-109">DESCRIPTION</span></span>
<span data-ttu-id="f8ff4-110">**Get-AzRecoveryServicesAsrEvent** 는 지정 된 선택 필터에 따라 자격 증명 모음에 있는 이벤트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="f8ff4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f8ff4-111">EXAMPLES</span></span>

### <span data-ttu-id="f8ff4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8ff4-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="f8ff4-113">모든 이벤트의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-113">List of all events.</span></span>

### <span data-ttu-id="f8ff4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f8ff4-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="f8ff4-115">이름을 기준으로 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-115">Get event by name.</span></span>

### <span data-ttu-id="f8ff4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="f8ff4-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="f8ff4-117">영향을 받는 개체에 대 한 이벤트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-117">List of event for affected Object.</span></span>

### <span data-ttu-id="f8ff4-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="f8ff4-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="f8ff4-119">시간 시작 시간 및 종료 시간, 심각도 위험 및 상태 유형 VmHealth 사이의 이벤트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="f8ff4-120">변수</span><span class="sxs-lookup"><span data-stu-id="f8ff4-120">PARAMETERS</span></span>

### <span data-ttu-id="f8ff4-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f8ff4-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="f8ff4-122">검색에 대 한 AffectedObject FriendlyName을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ff4-123">-DefaultProfile</span></span>
<span data-ttu-id="f8ff4-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8ff4-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f8ff4-125">-EndTime</span></span>
<span data-ttu-id="f8ff4-126">검색 창의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="f8ff4-127">이 매개 변수를 사용 하 여 지정 된 시간 이전에 발생 한 이벤트만 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="f8ff4-128">-EventType</span></span>
<span data-ttu-id="f8ff4-129">이벤트 유형별로 이벤트를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-130">-패브릭</span><span class="sxs-lookup"><span data-stu-id="f8ff4-130">-Fabric</span></span>
<span data-ttu-id="f8ff4-131">지정 된 패브릭에 따라 이벤트를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="f8ff4-132">-FabricId</span></span>
<span data-ttu-id="f8ff4-133">필터링 할 fabricId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-134">-이름</span><span class="sxs-lookup"><span data-stu-id="f8ff4-134">-Name</span></span>
<span data-ttu-id="f8ff4-135">검색할 이벤트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ff4-136">-ResourceId</span></span>
<span data-ttu-id="f8ff4-137">이벤트의 ResourceId 이벤트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-138">-심각도</span><span class="sxs-lookup"><span data-stu-id="f8ff4-138">-Severity</span></span>
<span data-ttu-id="f8ff4-139">필터링 할 이벤트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f8ff4-140">-StartTime</span></span>
<span data-ttu-id="f8ff4-141">검색 창의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="f8ff4-142">이 매개 변수를 사용 하 여 지정 된 시간 이후에 발생 한 이벤트만 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ff4-143">CommonParameters</span></span>
<span data-ttu-id="f8ff4-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ff4-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8ff4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ff4-146">입력</span><span class="sxs-lookup"><span data-stu-id="f8ff4-146">INPUTS</span></span>

### <span data-ttu-id="f8ff4-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f8ff4-147">System.String</span></span>

## <span data-ttu-id="f8ff4-148">출력</span><span class="sxs-lookup"><span data-stu-id="f8ff4-148">OUTPUTS</span></span>

### <span data-ttu-id="f8ff4-149">SiteRecovery. ASREvent에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="f8ff4-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="f8ff4-150">상속자</span><span class="sxs-lookup"><span data-stu-id="f8ff4-150">NOTES</span></span>

## <span data-ttu-id="f8ff4-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8ff4-151">RELATED LINKS</span></span>