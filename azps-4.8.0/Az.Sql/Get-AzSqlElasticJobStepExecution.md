---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212124"
---
# <span data-ttu-id="d6679-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="d6679-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="d6679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6679-102">SYNOPSIS</span></span>
<span data-ttu-id="d6679-103">하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="d6679-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6679-104">SYNTAX</span></span>

### <span data-ttu-id="d6679-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6679-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6679-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="d6679-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6679-107">엔터티가</span><span class="sxs-lookup"><span data-stu-id="d6679-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6679-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d6679-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6679-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6679-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6679-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d6679-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6679-111">설명은</span><span class="sxs-lookup"><span data-stu-id="d6679-111">DESCRIPTION</span></span>
<span data-ttu-id="d6679-112">Get-AzSqlElasticJobStepExecution cmdlet은 작업 실행에서 하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="d6679-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d6679-113">EXAMPLES</span></span>

### <span data-ttu-id="d6679-114">예제 1-작업 실행에서 하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="d6679-115">예제 2-작업 실행에서 하나 이상의 작업 단계 실행을 가져옵니다. 단계별 이름 필터링</span><span class="sxs-lookup"><span data-stu-id="d6679-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="d6679-116">하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="d6679-117">변수</span><span class="sxs-lookup"><span data-stu-id="d6679-117">PARAMETERS</span></span>

### <span data-ttu-id="d6679-118">-활성</span><span class="sxs-lookup"><span data-stu-id="d6679-118">-Active</span></span>
<span data-ttu-id="d6679-119">활성 실행을 기준으로 필터링 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d6679-120">-AgentName</span></span>
<span data-ttu-id="d6679-121">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="d6679-122">-CreateTimeMax</span></span>
<span data-ttu-id="d6679-123">생성 시간 최대값으로 필터링</span><span class="sxs-lookup"><span data-stu-id="d6679-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="d6679-124">-CreateTimeMin</span></span>
<span data-ttu-id="d6679-125">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="d6679-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6679-126">-DefaultProfile</span></span>
<span data-ttu-id="d6679-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6679-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="d6679-128">-EndTimeMax</span></span>
<span data-ttu-id="d6679-129">끝 시간 최대값으로 필터링</span><span class="sxs-lookup"><span data-stu-id="d6679-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="d6679-130">-EndTimeMin</span></span>
<span data-ttu-id="d6679-131">끝 시간 min으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="d6679-132">-JobExecutionId</span></span>
<span data-ttu-id="d6679-133">작업 실행 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="d6679-134">-JobName</span></span>
<span data-ttu-id="d6679-135">작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d6679-136">-ParentObject</span></span>
<span data-ttu-id="d6679-137">에이전트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d6679-138">-ParentResourceId</span></span>
<span data-ttu-id="d6679-139">작업 실행 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6679-140">-ResourceGroupName</span></span>
<span data-ttu-id="d6679-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6679-142">-ServerName</span></span>
<span data-ttu-id="d6679-143">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-144">-단계 이름</span><span class="sxs-lookup"><span data-stu-id="d6679-144">-StepName</span></span>
<span data-ttu-id="d6679-145">작업 단계 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6679-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6679-146">CommonParameters</span></span>
<span data-ttu-id="d6679-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6679-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6679-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6679-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6679-149">입력</span><span class="sxs-lookup"><span data-stu-id="d6679-149">INPUTS</span></span>

### <span data-ttu-id="d6679-150">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d6679-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="d6679-151">출력</span><span class="sxs-lookup"><span data-stu-id="d6679-151">OUTPUTS</span></span>

### <span data-ttu-id="d6679-152">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d6679-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="d6679-153">상속자</span><span class="sxs-lookup"><span data-stu-id="d6679-153">NOTES</span></span>

## <span data-ttu-id="d6679-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6679-154">RELATED LINKS</span></span>