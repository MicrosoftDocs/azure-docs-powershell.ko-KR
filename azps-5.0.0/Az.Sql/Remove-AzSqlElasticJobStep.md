---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216533"
---
# <span data-ttu-id="d058f-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="d058f-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="d058f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d058f-102">SYNOPSIS</span></span>
<span data-ttu-id="d058f-103">작업 단계를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-103">Removes the job step</span></span>

## <span data-ttu-id="d058f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d058f-104">SYNTAX</span></span>

### <span data-ttu-id="d058f-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d058f-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d058f-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="d058f-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d058f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d058f-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d058f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d058f-108">DESCRIPTION</span></span>
<span data-ttu-id="d058f-109">Remove-AzSqlElasticJobStep cmdlet은 작업에서 작업 단계를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="d058f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d058f-110">EXAMPLES</span></span>

### <span data-ttu-id="d058f-111">예제 1: 작업에서 작업 단계 제거</span><span class="sxs-lookup"><span data-stu-id="d058f-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="d058f-112">작업에서 작업 단계를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-112">Removes a job step from a job</span></span>

### <span data-ttu-id="d058f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d058f-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="d058f-114">변수</span><span class="sxs-lookup"><span data-stu-id="d058f-114">PARAMETERS</span></span>

### <span data-ttu-id="d058f-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d058f-115">-AgentName</span></span>
<span data-ttu-id="d058f-116">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="d058f-116">The agent name</span></span>

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

### <span data-ttu-id="d058f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d058f-117">-DefaultProfile</span></span>
<span data-ttu-id="d058f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d058f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d058f-119">-InputObject</span></span>
<span data-ttu-id="d058f-120">작업 단계 입력 개체</span><span class="sxs-lookup"><span data-stu-id="d058f-120">The job step input object</span></span>

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

### <span data-ttu-id="d058f-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="d058f-121">-JobName</span></span>
<span data-ttu-id="d058f-122">작업 이름</span><span class="sxs-lookup"><span data-stu-id="d058f-122">The job name</span></span>

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

### <span data-ttu-id="d058f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d058f-123">-Name</span></span>
<span data-ttu-id="d058f-124">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="d058f-124">The job step name</span></span>

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

### <span data-ttu-id="d058f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d058f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d058f-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d058f-126">The resource group name</span></span>

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

### <span data-ttu-id="d058f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d058f-127">-ResourceId</span></span>
<span data-ttu-id="d058f-128">작업 단계 리소스 id</span><span class="sxs-lookup"><span data-stu-id="d058f-128">The job step resource id</span></span>

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

### <span data-ttu-id="d058f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d058f-129">-ServerName</span></span>
<span data-ttu-id="d058f-130">서버 이름</span><span class="sxs-lookup"><span data-stu-id="d058f-130">The server name</span></span>

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

### <span data-ttu-id="d058f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d058f-131">-Confirm</span></span>
<span data-ttu-id="d058f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d058f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d058f-133">-WhatIf</span></span>
<span data-ttu-id="d058f-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d058f-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d058f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d058f-136">CommonParameters</span></span>
<span data-ttu-id="d058f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d058f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d058f-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d058f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d058f-139">입력</span><span class="sxs-lookup"><span data-stu-id="d058f-139">INPUTS</span></span>

### <span data-ttu-id="d058f-140">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d058f-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d058f-141">출력</span><span class="sxs-lookup"><span data-stu-id="d058f-141">OUTPUTS</span></span>

### <span data-ttu-id="d058f-142">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="d058f-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d058f-143">상속자</span><span class="sxs-lookup"><span data-stu-id="d058f-143">NOTES</span></span>

## <span data-ttu-id="d058f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d058f-144">RELATED LINKS</span></span>