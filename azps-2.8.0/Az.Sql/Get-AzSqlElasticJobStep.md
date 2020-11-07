---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 16899acb35270e01b80e267aab6fe6ab03827c02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873669"
---
# <span data-ttu-id="6f9cd-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="6f9cd-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="6f9cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9cd-103">하나 이상의 작업 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-103">Gets one or more job steps</span></span>

## <span data-ttu-id="6f9cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f9cd-104">SYNTAX</span></span>

### <span data-ttu-id="6f9cd-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f9cd-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f9cd-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="6f9cd-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f9cd-107">엔터티가</span><span class="sxs-lookup"><span data-stu-id="6f9cd-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f9cd-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="6f9cd-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f9cd-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6f9cd-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f9cd-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9cd-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f9cd-111">설명은</span><span class="sxs-lookup"><span data-stu-id="6f9cd-111">DESCRIPTION</span></span>
<span data-ttu-id="6f9cd-112">Get-AzSqlElasticJobStep cmdlet은 작업에서 하나 이상의 작업 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="6f9cd-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6f9cd-113">EXAMPLES</span></span>

### <span data-ttu-id="6f9cd-114">예제 1-작업에서 작업 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-114">Example 1 - Gets a job step from a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="6f9cd-115">작업에서 작업 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-115">Gets a job step from a job</span></span>

## <span data-ttu-id="6f9cd-116">변수</span><span class="sxs-lookup"><span data-stu-id="6f9cd-116">PARAMETERS</span></span>

### <span data-ttu-id="6f9cd-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6f9cd-117">-AgentName</span></span>
<span data-ttu-id="6f9cd-118">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9cd-119">-DefaultProfile</span></span>
<span data-ttu-id="6f9cd-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f9cd-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="6f9cd-121">-JobName</span></span>
<span data-ttu-id="6f9cd-122">작업 이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-123">-이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-123">-Name</span></span>
<span data-ttu-id="6f9cd-124">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6f9cd-125">-ParentObject</span></span>
<span data-ttu-id="6f9cd-126">작업 입력 개체</span><span class="sxs-lookup"><span data-stu-id="6f9cd-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6f9cd-127">-ParentResourceId</span></span>
<span data-ttu-id="6f9cd-128">작업 리소스 id</span><span class="sxs-lookup"><span data-stu-id="6f9cd-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f9cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f9cd-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f9cd-131">-ServerName</span></span>
<span data-ttu-id="6f9cd-132">서버 이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-133">-버전</span><span class="sxs-lookup"><span data-stu-id="6f9cd-133">-Version</span></span>
<span data-ttu-id="6f9cd-134">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="6f9cd-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9cd-135">CommonParameters</span></span>
<span data-ttu-id="6f9cd-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9cd-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f9cd-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9cd-138">입력</span><span class="sxs-lookup"><span data-stu-id="6f9cd-138">INPUTS</span></span>

### <span data-ttu-id="6f9cd-139">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="6f9cd-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6f9cd-140">출력</span><span class="sxs-lookup"><span data-stu-id="6f9cd-140">OUTPUTS</span></span>

### <span data-ttu-id="6f9cd-141">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="6f9cd-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="6f9cd-142">상속자</span><span class="sxs-lookup"><span data-stu-id="6f9cd-142">NOTES</span></span>

## <span data-ttu-id="6f9cd-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f9cd-143">RELATED LINKS</span></span>