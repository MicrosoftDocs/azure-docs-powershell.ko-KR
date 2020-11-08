---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226123"
---
# <span data-ttu-id="feaea-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="feaea-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="feaea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feaea-102">SYNOPSIS</span></span>
<span data-ttu-id="feaea-103">로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="feaea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="feaea-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="feaea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="feaea-105">DESCRIPTION</span></span>
<span data-ttu-id="feaea-106">로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="feaea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="feaea-107">EXAMPLES</span></span>

### <span data-ttu-id="feaea-108">예제 1: 로그 분석 작업 영역에 대 한 모니터 로그 분석 솔루션 만들기</span><span class="sxs-lookup"><span data-stu-id="feaea-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="feaea-109">이 명령은 로그 분석 작업 영역에 대 한 모니터 로그 분석 솔루션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="feaea-110">일반적으로 사용 되는 형식은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-110">Commonly used types are:</span></span>

| <span data-ttu-id="feaea-111">입력할</span><span class="sxs-lookup"><span data-stu-id="feaea-111">Type</span></span> | <span data-ttu-id="feaea-112">설명은</span><span class="sxs-lookup"><span data-stu-id="feaea-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="feaea-113">Security센터 무료</span><span class="sxs-lookup"><span data-stu-id="feaea-113">SecurityCenterFree</span></span> |  <span data-ttu-id="feaea-114">Azure 보안 센터 – 무료 에디션</span><span class="sxs-lookup"><span data-stu-id="feaea-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="feaea-115">보안이</span><span class="sxs-lookup"><span data-stu-id="feaea-115">Security</span></span> | <span data-ttu-id="feaea-116">Azure 보안 센터</span><span class="sxs-lookup"><span data-stu-id="feaea-116">Azure Security Center</span></span> |
| <span data-ttu-id="feaea-117">업데이트</span><span class="sxs-lookup"><span data-stu-id="feaea-117">Updates</span></span> | <span data-ttu-id="feaea-118">업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="feaea-118">Update Management</span></span> |
| <span data-ttu-id="feaea-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="feaea-119">ContainerInsights</span></span> | <span data-ttu-id="feaea-120">컨테이너에 대 한 Azure 모니터</span><span class="sxs-lookup"><span data-stu-id="feaea-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="feaea-121">ServiceMap%)</span><span class="sxs-lookup"><span data-stu-id="feaea-121">ServiceMap</span></span> | <span data-ttu-id="feaea-122">서비스 지도</span><span class="sxs-lookup"><span data-stu-id="feaea-122">Service Map</span></span> |
| <span data-ttu-id="feaea-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="feaea-123">AzureActivity</span></span> | <span data-ttu-id="feaea-124">활동 로그 분석</span><span class="sxs-lookup"><span data-stu-id="feaea-124">Activity log analytics</span></span> |
| <span data-ttu-id="feaea-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="feaea-125">ChangeTracking</span></span> | <span data-ttu-id="feaea-126">변경 내용 추적 및 재고</span><span class="sxs-lookup"><span data-stu-id="feaea-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="feaea-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="feaea-127">VMInsights</span></span> | <span data-ttu-id="feaea-128">Vm 용 Azure 모니터</span><span class="sxs-lookup"><span data-stu-id="feaea-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="feaea-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="feaea-129">SecurityInsights</span></span> | <span data-ttu-id="feaea-130">Azure 센티널</span><span class="sxs-lookup"><span data-stu-id="feaea-130">Azure Sentinel</span></span> |
| <span data-ttu-id="feaea-131">네트워크 모니터링</span><span class="sxs-lookup"><span data-stu-id="feaea-131">NetworkMonitoring</span></span> | <span data-ttu-id="feaea-132">네트워크 성능 모니터</span><span class="sxs-lookup"><span data-stu-id="feaea-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="feaea-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="feaea-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="feaea-134">SQL 취약점 평가</span><span class="sxs-lookup"><span data-stu-id="feaea-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="feaea-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="feaea-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="feaea-136">SQL 고급 위협 방지</span><span class="sxs-lookup"><span data-stu-id="feaea-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="feaea-137">방지</span><span class="sxs-lookup"><span data-stu-id="feaea-137">AntiMalware</span></span> | <span data-ttu-id="feaea-138">맬웨어 방지 평가</span><span class="sxs-lookup"><span data-stu-id="feaea-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="feaea-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="feaea-139">AzureAutomation</span></span> | <span data-ttu-id="feaea-140">자동화 하이브리드 작업자</span><span class="sxs-lookup"><span data-stu-id="feaea-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="feaea-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="feaea-141">LogicAppsManagement</span></span> | <span data-ttu-id="feaea-142">논리 앱 관리</span><span class="sxs-lookup"><span data-stu-id="feaea-142">Logic Apps Management</span></span> |
| <span data-ttu-id="feaea-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="feaea-143">SQLDataClassification</span></span> | <span data-ttu-id="feaea-144">SQL 데이터 검색 & 분류</span><span class="sxs-lookup"><span data-stu-id="feaea-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="feaea-145">변수</span><span class="sxs-lookup"><span data-stu-id="feaea-145">PARAMETERS</span></span>

### <span data-ttu-id="feaea-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feaea-146">-DefaultProfile</span></span>
<span data-ttu-id="feaea-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feaea-148">-위치</span><span class="sxs-lookup"><span data-stu-id="feaea-148">-Location</span></span>
<span data-ttu-id="feaea-149">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-149">Resource location.</span></span>
<span data-ttu-id="feaea-150">로그 분석 작업 영역과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feaea-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feaea-151">-ResourceGroupName</span></span>
<span data-ttu-id="feaea-152">가져올 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-152">The name of the resource group to get.</span></span>
<span data-ttu-id="feaea-153">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feaea-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="feaea-154">-SubscriptionId</span></span>
<span data-ttu-id="feaea-155">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="feaea-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feaea-157">태그</span><span class="sxs-lookup"><span data-stu-id="feaea-157">-Tag</span></span>
<span data-ttu-id="feaea-158">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="feaea-158">Resource tags</span></span>

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

### <span data-ttu-id="feaea-159">-Type</span><span class="sxs-lookup"><span data-stu-id="feaea-159">-Type</span></span>
<span data-ttu-id="feaea-160">만들려는 솔루션의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-160">Type of the solution to be created.</span></span>
<span data-ttu-id="feaea-161">예를 들어 "컨테이너".</span><span class="sxs-lookup"><span data-stu-id="feaea-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feaea-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="feaea-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="feaea-163">솔루션이 배포/활성화 될 작업 영역의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feaea-164">-확인</span><span class="sxs-lookup"><span data-stu-id="feaea-164">-Confirm</span></span>
<span data-ttu-id="feaea-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feaea-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feaea-166">-WhatIf</span></span>
<span data-ttu-id="feaea-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feaea-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feaea-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feaea-169">CommonParameters</span></span>
<span data-ttu-id="feaea-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaea-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feaea-171">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="feaea-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feaea-172">입력</span><span class="sxs-lookup"><span data-stu-id="feaea-172">INPUTS</span></span>

## <span data-ttu-id="feaea-173">출력</span><span class="sxs-lookup"><span data-stu-id="feaea-173">OUTPUTS</span></span>

### <span data-ttu-id="feaea-174">MonitoringSolutions. Api20151101Preview. ISolution에 대 한</span><span class="sxs-lookup"><span data-stu-id="feaea-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="feaea-175">상속자</span><span class="sxs-lookup"><span data-stu-id="feaea-175">NOTES</span></span>

<span data-ttu-id="feaea-176">별칭과</span><span class="sxs-lookup"><span data-stu-id="feaea-176">ALIASES</span></span>

## <span data-ttu-id="feaea-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feaea-177">RELATED LINKS</span></span>



[<span data-ttu-id="feaea-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="feaea-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)
