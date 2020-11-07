---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: b758c3a76c27fb2a1f06c7b6c940d3c3a7ef1c11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873586"
---
# <span data-ttu-id="750a4-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="750a4-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="750a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="750a4-102">SYNOPSIS</span></span>
<span data-ttu-id="750a4-103">작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-103">Removes a job</span></span>

## <span data-ttu-id="750a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="750a4-104">SYNTAX</span></span>

### <span data-ttu-id="750a4-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="750a4-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750a4-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="750a4-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750a4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="750a4-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="750a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="750a4-108">DESCRIPTION</span></span>
<span data-ttu-id="750a4-109">Remove-AzSqlElasticJob cmdlet은 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="750a4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="750a4-110">EXAMPLES</span></span>

### <span data-ttu-id="750a4-111">예제 1-작업 제거</span><span class="sxs-lookup"><span data-stu-id="750a4-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="750a4-112">작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-112">Removes a job</span></span>

## <span data-ttu-id="750a4-113">변수</span><span class="sxs-lookup"><span data-stu-id="750a4-113">PARAMETERS</span></span>

### <span data-ttu-id="750a4-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="750a4-114">-AgentName</span></span>
<span data-ttu-id="750a4-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="750a4-115">The agent name</span></span>

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

### <span data-ttu-id="750a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750a4-116">-DefaultProfile</span></span>
<span data-ttu-id="750a4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="750a4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="750a4-118">-Force</span></span>
<span data-ttu-id="750a4-119">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="750a4-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750a4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="750a4-120">-InputObject</span></span>
<span data-ttu-id="750a4-121">작업 입력 개체</span><span class="sxs-lookup"><span data-stu-id="750a4-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="750a4-122">-이름</span><span class="sxs-lookup"><span data-stu-id="750a4-122">-Name</span></span>
<span data-ttu-id="750a4-123">작업 이름</span><span class="sxs-lookup"><span data-stu-id="750a4-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="750a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="750a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="750a4-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="750a4-125">The resource group name</span></span>

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

### <span data-ttu-id="750a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="750a4-126">-ResourceId</span></span>
<span data-ttu-id="750a4-127">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="750a4-127">The agent resource id</span></span>

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

### <span data-ttu-id="750a4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="750a4-128">-ServerName</span></span>
<span data-ttu-id="750a4-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="750a4-129">The server name</span></span>

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

### <span data-ttu-id="750a4-130">-확인</span><span class="sxs-lookup"><span data-stu-id="750a4-130">-Confirm</span></span>
<span data-ttu-id="750a4-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="750a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="750a4-132">-WhatIf</span></span>
<span data-ttu-id="750a4-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="750a4-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="750a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750a4-135">CommonParameters</span></span>
<span data-ttu-id="750a4-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="750a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750a4-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="750a4-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750a4-138">입력</span><span class="sxs-lookup"><span data-stu-id="750a4-138">INPUTS</span></span>

### <span data-ttu-id="750a4-139">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="750a4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="750a4-140">출력</span><span class="sxs-lookup"><span data-stu-id="750a4-140">OUTPUTS</span></span>

### <span data-ttu-id="750a4-141">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="750a4-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="750a4-142">상속자</span><span class="sxs-lookup"><span data-stu-id="750a4-142">NOTES</span></span>

## <span data-ttu-id="750a4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="750a4-143">RELATED LINKS</span></span>