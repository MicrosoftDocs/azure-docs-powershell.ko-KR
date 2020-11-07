---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 83d5733144c07c229cf8b5321ee9d3417ab112ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873853"
---
# <span data-ttu-id="c6f03-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c6f03-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c6f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f03-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f03-103">작업 단계를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-103">Removes the job step</span></span>

## <span data-ttu-id="c6f03-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6f03-104">SYNTAX</span></span>

### <span data-ttu-id="c6f03-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6f03-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6f03-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="c6f03-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6f03-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c6f03-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6f03-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c6f03-108">DESCRIPTION</span></span>
<span data-ttu-id="c6f03-109">Remove-AzSqlElasticJobStep cmdlet은 작업에서 작업 단계를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="c6f03-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c6f03-110">EXAMPLES</span></span>

### <span data-ttu-id="c6f03-111">예제 1-작업에서 작업 단계 제거</span><span class="sxs-lookup"><span data-stu-id="c6f03-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c6f03-112">작업에서 작업 단계를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-112">Removes a job step from a job</span></span>

## <span data-ttu-id="c6f03-113">변수</span><span class="sxs-lookup"><span data-stu-id="c6f03-113">PARAMETERS</span></span>

### <span data-ttu-id="c6f03-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c6f03-114">-AgentName</span></span>
<span data-ttu-id="c6f03-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="c6f03-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f03-116">-DefaultProfile</span></span>
<span data-ttu-id="c6f03-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6f03-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6f03-118">-InputObject</span></span>
<span data-ttu-id="c6f03-119">작업 단계 입력 개체</span><span class="sxs-lookup"><span data-stu-id="c6f03-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="c6f03-120">-JobName</span></span>
<span data-ttu-id="c6f03-121">작업 이름</span><span class="sxs-lookup"><span data-stu-id="c6f03-121">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c6f03-122">-Name</span></span>
<span data-ttu-id="c6f03-123">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="c6f03-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6f03-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6f03-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c6f03-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6f03-126">-ResourceId</span></span>
<span data-ttu-id="c6f03-127">작업 단계 리소스 id</span><span class="sxs-lookup"><span data-stu-id="c6f03-127">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6f03-128">-ServerName</span></span>
<span data-ttu-id="c6f03-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="c6f03-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-130">-확인</span><span class="sxs-lookup"><span data-stu-id="c6f03-130">-Confirm</span></span>
<span data-ttu-id="c6f03-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f03-132">-WhatIf</span></span>
<span data-ttu-id="c6f03-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6f03-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f03-135">CommonParameters</span></span>
<span data-ttu-id="c6f03-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f03-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c6f03-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f03-138">입력</span><span class="sxs-lookup"><span data-stu-id="c6f03-138">INPUTS</span></span>

### <span data-ttu-id="c6f03-139">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c6f03-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c6f03-140">출력</span><span class="sxs-lookup"><span data-stu-id="c6f03-140">OUTPUTS</span></span>

### <span data-ttu-id="c6f03-141">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c6f03-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c6f03-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c6f03-142">NOTES</span></span>

## <span data-ttu-id="c6f03-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6f03-143">RELATED LINKS</span></span>