---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSparkPool.md
ms.openlocfilehash: fd1dbcc2e70b4d44de0c105af2332a9e4836d3bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047479"
---
# <span data-ttu-id="f8ff8-101">Get-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f8ff8-101">Get-AzSynapseSparkPool</span></span>

## <span data-ttu-id="f8ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ff8-103">Synapse Analytics Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-103">Gets a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f8ff8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8ff8-104">SYNTAX</span></span>

### <span data-ttu-id="f8ff8-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8ff8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8ff8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8ff8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSparkPool [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8ff8-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8ff8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSparkPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8ff8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f8ff8-108">DESCRIPTION</span></span>
<span data-ttu-id="f8ff8-109">**AzSynapseSparkPool** Cmdlet은 Azure Synapse Analytics Spark 풀에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-109">The **Get-AzSynapseSparkPool** cmdlet gets information about an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="f8ff8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f8ff8-110">EXAMPLES</span></span>

### <span data-ttu-id="f8ff8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8ff8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f8ff8-112">이 명령은 작업 영역 아래에 있는 모든 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-112">This command gets all Spark pools under a workspace.</span></span>

### <span data-ttu-id="f8ff8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f8ff8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="f8ff8-114">이 명령은 name ContosoSparkPool를 사용 하 여 workspace ContosoWorkspace의 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-114">This command gets the Spark pool under workspace ContosoWorkspace with name ContosoSparkPool.</span></span>

### <span data-ttu-id="f8ff8-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f8ff8-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSparkPool
```

<span data-ttu-id="f8ff8-116">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-116">This command gets all Spark pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="f8ff8-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="f8ff8-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSparkPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool"
```

<span data-ttu-id="f8ff8-118">이 명령은 지정 된 리소스 ID를 갖는 Spark 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-118">This command gets the Spark pool with the specified resource ID.</span></span>

## <span data-ttu-id="f8ff8-119">변수</span><span class="sxs-lookup"><span data-stu-id="f8ff8-119">PARAMETERS</span></span>

### <span data-ttu-id="f8ff8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ff8-120">-DefaultProfile</span></span>
<span data-ttu-id="f8ff8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8ff8-122">-이름</span><span class="sxs-lookup"><span data-stu-id="f8ff8-122">-Name</span></span>
<span data-ttu-id="f8ff8-123">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-123">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SparkPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ff8-124">-ResourceGroupName</span></span>
<span data-ttu-id="f8ff8-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ff8-126">-ResourceId</span></span>
<span data-ttu-id="f8ff8-127">Synapse Spark 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-127">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff8-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8ff8-128">-WorkspaceName</span></span>
<span data-ttu-id="f8ff8-129">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff8-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f8ff8-130">-WorkspaceObject</span></span>
<span data-ttu-id="f8ff8-131">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ff8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ff8-132">CommonParameters</span></span>
<span data-ttu-id="f8ff8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ff8-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ff8-135">입력</span><span class="sxs-lookup"><span data-stu-id="f8ff8-135">INPUTS</span></span>

### <span data-ttu-id="f8ff8-136">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f8ff8-137">출력</span><span class="sxs-lookup"><span data-stu-id="f8ff8-137">OUTPUTS</span></span>

### <span data-ttu-id="f8ff8-138">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="f8ff8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="f8ff8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f8ff8-139">NOTES</span></span>

## <span data-ttu-id="f8ff8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8ff8-140">RELATED LINKS</span></span>