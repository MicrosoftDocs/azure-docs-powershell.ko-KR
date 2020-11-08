---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216675"
---
# <span data-ttu-id="4907a-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="4907a-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="4907a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4907a-102">SYNOPSIS</span></span>
<span data-ttu-id="4907a-103">새 작업 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="4907a-103">Creates a new job credential</span></span>

## <span data-ttu-id="4907a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4907a-104">SYNTAX</span></span>

### <span data-ttu-id="4907a-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4907a-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4907a-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="4907a-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4907a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4907a-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4907a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4907a-108">DESCRIPTION</span></span>
<span data-ttu-id="4907a-109">New-AzSqlElasticJobCredential cmdlet은 새 작업 자격 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4907a-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="4907a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4907a-110">EXAMPLES</span></span>

### <span data-ttu-id="4907a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4907a-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="4907a-112">새 작업 자격 증명 만들기</span><span class="sxs-lookup"><span data-stu-id="4907a-112">Creates a new job credential</span></span>

## <span data-ttu-id="4907a-113">변수</span><span class="sxs-lookup"><span data-stu-id="4907a-113">PARAMETERS</span></span>

### <span data-ttu-id="4907a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4907a-114">-AgentName</span></span>
<span data-ttu-id="4907a-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="4907a-115">The agent name</span></span>

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

### <span data-ttu-id="4907a-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="4907a-116">-Credential</span></span>
<span data-ttu-id="4907a-117">자격 증명</span><span class="sxs-lookup"><span data-stu-id="4907a-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4907a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4907a-118">-DefaultProfile</span></span>
<span data-ttu-id="4907a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4907a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4907a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4907a-120">-Name</span></span>
<span data-ttu-id="4907a-121">작업 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="4907a-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4907a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4907a-122">-ParentObject</span></span>
<span data-ttu-id="4907a-123">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="4907a-123">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4907a-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4907a-124">-ParentResourceId</span></span>
<span data-ttu-id="4907a-125">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="4907a-125">The agent resource id</span></span>

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

### <span data-ttu-id="4907a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4907a-126">-ResourceGroupName</span></span>
<span data-ttu-id="4907a-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4907a-127">The resource group name</span></span>

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

### <span data-ttu-id="4907a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4907a-128">-ServerName</span></span>
<span data-ttu-id="4907a-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="4907a-129">The server name</span></span>

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

### <span data-ttu-id="4907a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="4907a-130">-Confirm</span></span>
<span data-ttu-id="4907a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4907a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4907a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4907a-132">-WhatIf</span></span>
<span data-ttu-id="4907a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4907a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4907a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4907a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4907a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4907a-135">CommonParameters</span></span>
<span data-ttu-id="4907a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4907a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4907a-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4907a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4907a-138">입력</span><span class="sxs-lookup"><span data-stu-id="4907a-138">INPUTS</span></span>

### <span data-ttu-id="4907a-139">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4907a-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="4907a-140">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="4907a-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4907a-141">출력</span><span class="sxs-lookup"><span data-stu-id="4907a-141">OUTPUTS</span></span>

### <span data-ttu-id="4907a-142">ElasticJobs. AzureSqlElasticJobCredentialModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="4907a-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="4907a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4907a-143">NOTES</span></span>

## <span data-ttu-id="4907a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4907a-144">RELATED LINKS</span></span>