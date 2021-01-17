---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323371"
---
# <span data-ttu-id="d9a3c-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d9a3c-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="d9a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a3c-103">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-103">The operation to create or update a export.</span></span>
<span data-ttu-id="d9a3c-104">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d9a3c-105">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d9a3c-106">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d9a3c-107">구문</span><span class="sxs-lookup"><span data-stu-id="d9a3c-107">SYNTAX</span></span>

### <span data-ttu-id="d9a3c-108">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="d9a3c-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d9a3c-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d9a3c-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9a3c-110">설명</span><span class="sxs-lookup"><span data-stu-id="d9a3c-110">DESCRIPTION</span></span>
<span data-ttu-id="d9a3c-111">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-111">The operation to create or update a export.</span></span>
<span data-ttu-id="d9a3c-112">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d9a3c-113">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d9a3c-114">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d9a3c-115">예제</span><span class="sxs-lookup"><span data-stu-id="d9a3c-115">EXAMPLES</span></span>

### <span data-ttu-id="d9a3c-116">예제 1: 범위 및 이름으로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="d9a3c-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="d9a3c-117">범위 및 이름으로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="d9a3c-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="d9a3c-118">예제 2: InputObject로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="d9a3c-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="d9a3c-119">InputObject로 AzCostManagementExport 업데이트</span><span class="sxs-lookup"><span data-stu-id="d9a3c-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="d9a3c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9a3c-120">PARAMETERS</span></span>

### <span data-ttu-id="d9a3c-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="d9a3c-121">-ConfigurationColumn</span></span>
<span data-ttu-id="d9a3c-122">내보내기에 포함될 열 이름의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="d9a3c-123">제공되지 않은 경우 내보내기에는 사용 가능한 모든 열이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="d9a3c-124">사용 가능한 열은 고객 채널에 따라 다를 수 있습니다(예제 참조).</span><span class="sxs-lookup"><span data-stu-id="d9a3c-124">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="d9a3c-125">-DataSetGranularity</span></span>
<span data-ttu-id="d9a3c-126">내보내기 행의 세분성입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="d9a3c-127">현재는 '매일'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-127">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a3c-128">-DefaultProfile</span></span>
<span data-ttu-id="d9a3c-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9a3c-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="d9a3c-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="d9a3c-131">내보내기 데이터를 끌어오는 시간 프레임입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="d9a3c-132">사용자 지정인 경우 특정 기간을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-132">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="d9a3c-133">-DefinitionType</span></span>
<span data-ttu-id="d9a3c-134">내보내기 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-134">The type of the export.</span></span>
<span data-ttu-id="d9a3c-135">'Usage'는 'ActualCost'에 해당하며 서비스 예약에 대한 요금 또는 상금에 대한 데이터를 아직 제공하지 않는 내보내기에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="d9a3c-136">-DestinationContainer</span></span>
<span data-ttu-id="d9a3c-137">내보내기 업로드할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d9a3c-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d9a3c-138">-DestinationResourceId</span></span>
<span data-ttu-id="d9a3c-139">내보내기 배달될 저장소 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="d9a3c-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="d9a3c-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="d9a3c-141">내보내기 업로드할 디렉터리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d9a3c-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="d9a3c-142">-ETag</span></span>
<span data-ttu-id="d9a3c-143">리소스의 eTag입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-143">eTag of the resource.</span></span>
<span data-ttu-id="d9a3c-144">동시 업데이트 시나리오를 처리하기 위해 이 필드는 사용자가 최신 버전을 업데이트하는지 여부를 결정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="d9a3c-145">-Format</span><span class="sxs-lookup"><span data-stu-id="d9a3c-145">-Format</span></span>
<span data-ttu-id="d9a3c-146">배달되는 내보내기 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-146">The format of the export being delivered.</span></span>
<span data-ttu-id="d9a3c-147">현재는 'Csv'만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-147">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a3c-148">-InputObject</span></span>
<span data-ttu-id="d9a3c-149">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-150">-Name</span><span class="sxs-lookup"><span data-stu-id="d9a3c-150">-Name</span></span>
<span data-ttu-id="d9a3c-151">이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d9a3c-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="d9a3c-153">재발의 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-153">The start date of recurrence.</span></span>

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

### <span data-ttu-id="d9a3c-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d9a3c-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="d9a3c-155">재발의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-155">The end date of recurrence.</span></span>

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

### <span data-ttu-id="d9a3c-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="d9a3c-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="d9a3c-157">일정 재발입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-157">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="d9a3c-158">-ScheduleStatus</span></span>
<span data-ttu-id="d9a3c-159">내보내기 일정의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-159">The status of the export's schedule.</span></span>
<span data-ttu-id="d9a3c-160">'비활성'인 경우 내보내기 일정이 일시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-160">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a3c-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="d9a3c-161">-Scope</span></span>
<span data-ttu-id="d9a3c-162">이 매개 변수는 '구독', 'ResourceGroup' 및 '서비스 제공' 관점에서 costmanagement의 범위를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="d9a3c-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d9a3c-163">-TimePeriodFrom</span></span>
<span data-ttu-id="d9a3c-164">데이터 내보내기 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-164">The start date for export data.</span></span>

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

### <span data-ttu-id="d9a3c-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d9a3c-165">-TimePeriodTo</span></span>
<span data-ttu-id="d9a3c-166">내보내기 데이터의 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-166">The end date for export data.</span></span>

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

### <span data-ttu-id="d9a3c-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9a3c-167">-Confirm</span></span>
<span data-ttu-id="d9a3c-168">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a3c-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a3c-169">-WhatIf</span></span>
<span data-ttu-id="d9a3c-170">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9a3c-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a3c-171">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a3c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a3c-172">CommonParameters</span></span>
<span data-ttu-id="d9a3c-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a3c-174">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a3c-175">입력</span><span class="sxs-lookup"><span data-stu-id="d9a3c-175">INPUTS</span></span>

### <span data-ttu-id="d9a3c-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="d9a3c-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="d9a3c-177">출력</span><span class="sxs-lookup"><span data-stu-id="d9a3c-177">OUTPUTS</span></span>

### <span data-ttu-id="d9a3c-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span><span class="sxs-lookup"><span data-stu-id="d9a3c-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="d9a3c-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9a3c-179">NOTES</span></span>

<span data-ttu-id="d9a3c-180">별칭</span><span class="sxs-lookup"><span data-stu-id="d9a3c-180">ALIASES</span></span>

<span data-ttu-id="d9a3c-181">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d9a3c-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d9a3c-182">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9a3c-183">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d9a3c-184">INPUTOBJECT: <ICostManagementIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d9a3c-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d9a3c-185">`[AlertId <String>]`: 경고 ID</span><span class="sxs-lookup"><span data-stu-id="d9a3c-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="d9a3c-186">`[ExportName <String>]`: 이름을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="d9a3c-187">`[ExternalCloudProviderId <String>]`: 연결된 계정의 경우 '{externalSubscriptionId}'이고 차원/쿼리 작업에 사용되는 통합 계정의 경우 '{externalBillingAccountId}'일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="d9a3c-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: 차원/쿼리 작업과 연결된 외부 클라우드 공급자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="d9a3c-189">여기에는 연결된 계정에 대한 'externalSubscriptions', 통합된 계정에 대한 'externalBillingAccounts'가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="d9a3c-190">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d9a3c-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d9a3c-191">`[Scope <String>]`: 보기 작업과 연결된 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="d9a3c-192">여기에는 구독 범위의 'subscriptions/{subscriptionId}', resourceGroup 범위에 대한 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}', 청구 계정 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}'이 포함됩니다. Department 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, BillingProfile 범위에 대한 'providers/Microsoft.Billing/billingAccounts/{billingAccounts/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft 관리 그룹 범위에 대한 관리/managementGroups/{managementGroupId}', 외부 청구 계정 범위에 대한 'providers/Microsoft.CostManagement/externalBillingAccountName}', 외부 구독 범위에 대한 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}'.</span><span class="sxs-lookup"><span data-stu-id="d9a3c-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="d9a3c-193">`[ViewName <String>]`: 이름 보기</span><span class="sxs-lookup"><span data-stu-id="d9a3c-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="d9a3c-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9a3c-194">RELATED LINKS</span></span>
