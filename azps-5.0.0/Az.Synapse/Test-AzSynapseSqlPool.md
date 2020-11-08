---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215144"
---
# <span data-ttu-id="924e4-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="924e4-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="924e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="924e4-102">SYNOPSIS</span></span>
<span data-ttu-id="924e4-103">Synapse Analytics SQL 풀이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="924e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="924e4-104">SYNTAX</span></span>

### <span data-ttu-id="924e4-105">TestByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="924e4-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="924e4-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="924e4-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="924e4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="924e4-107">DESCRIPTION</span></span>
<span data-ttu-id="924e4-108">**AzSynapseSqlPool** Cmdlet은 SYNAPSE Analytics SQL 풀이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="924e4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="924e4-109">EXAMPLES</span></span>

### <span data-ttu-id="924e4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="924e4-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="924e4-111">이 명령은 지정 된 SQL 풀이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="924e4-112">변수</span><span class="sxs-lookup"><span data-stu-id="924e4-112">PARAMETERS</span></span>

### <span data-ttu-id="924e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924e4-113">-DefaultProfile</span></span>
<span data-ttu-id="924e4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="924e4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="924e4-115">-Name</span></span>
<span data-ttu-id="924e4-116">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="924e4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924e4-117">-ResourceGroupName</span></span>
<span data-ttu-id="924e4-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924e4-119">-버전</span><span class="sxs-lookup"><span data-stu-id="924e4-119">-Version</span></span>
<span data-ttu-id="924e4-120">Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="924e4-121">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924e4-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="924e4-122">-WorkspaceName</span></span>
<span data-ttu-id="924e4-123">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="924e4-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="924e4-124">-WorkspaceObject</span></span>
<span data-ttu-id="924e4-125">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="924e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924e4-126">CommonParameters</span></span>
<span data-ttu-id="924e4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="924e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924e4-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="924e4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924e4-129">입력</span><span class="sxs-lookup"><span data-stu-id="924e4-129">INPUTS</span></span>

### <span data-ttu-id="924e4-130">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="924e4-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="924e4-131">출력</span><span class="sxs-lookup"><span data-stu-id="924e4-131">OUTPUTS</span></span>

### <span data-ttu-id="924e4-132">System. 개체</span><span class="sxs-lookup"><span data-stu-id="924e4-132">System.Object</span></span>
## <span data-ttu-id="924e4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="924e4-133">NOTES</span></span>

## <span data-ttu-id="924e4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="924e4-134">RELATED LINKS</span></span>