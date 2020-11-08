---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043009"
---
# <span data-ttu-id="ffc35-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="ffc35-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="ffc35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc35-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc35-103">풀 id로 그룹화 된 노드 상태별로 일괄 처리 노드 개수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="ffc35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffc35-104">SYNTAX</span></span>

### <span data-ttu-id="ffc35-105">AzureBatchPoolNodeCounts (기본값)</span><span class="sxs-lookup"><span data-stu-id="ffc35-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffc35-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="ffc35-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffc35-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ffc35-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffc35-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="ffc35-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffc35-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ffc35-109">DESCRIPTION</span></span>
<span data-ttu-id="ffc35-110">Get-AzBatchPoolNodeCount cmdlet을 사용 하면 고객이 풀 별로 그룹화 된 노드 상태별로 다시 돌아갈 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="ffc35-111">노드 상태는 만들기, 유휴, leavingPool, 오프 라인, 선취, 다시 부팅, reimaging, 실행, 시작, startTaskFailed, unknown, 사용할 수 없음, waitingForStartTask입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="ffc35-112">Cmdlet은 PoolId 또는 Pool 매개 변수를 사용 하 여 풀 id가 지정 된 풀만 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="ffc35-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ffc35-113">EXAMPLES</span></span>

### <span data-ttu-id="ffc35-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffc35-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="ffc35-115">현재 일괄 처리 계정 컨텍스트 아래에서 풀에 대 한 노드 상태별로 목록 노드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="ffc35-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="ffc35-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="ffc35-117">지정 된 풀 id에 대 한 노드 상태별 노드 수를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="ffc35-118">변수</span><span class="sxs-lookup"><span data-stu-id="ffc35-118">PARAMETERS</span></span>

### <span data-ttu-id="ffc35-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ffc35-119">-BatchContext</span></span>
<span data-ttu-id="ffc35-120">일괄 처리 서비스와 상호 작용할 때 사용할 BatchAccountContext 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="ffc35-121">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="ffc35-122">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="ffc35-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="ffc35-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc35-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc35-125">-DefaultProfile</span></span>
<span data-ttu-id="ffc35-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc35-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ffc35-127">-MaxCount</span></span>
<span data-ttu-id="ffc35-128">반환할 최대 풀 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="ffc35-129">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc35-130">-풀</span><span class="sxs-lookup"><span data-stu-id="ffc35-130">-Pool</span></span>
<span data-ttu-id="ffc35-131">노드 개수를 가져올 **Pscloudpool** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc35-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ffc35-132">-PoolId</span></span>
<span data-ttu-id="ffc35-133">노드 개수를 가져올 풀의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc35-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc35-134">CommonParameters</span></span>
<span data-ttu-id="ffc35-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc35-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc35-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffc35-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc35-137">입력</span><span class="sxs-lookup"><span data-stu-id="ffc35-137">INPUTS</span></span>

### <span data-ttu-id="ffc35-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ffc35-138">System.String</span></span>

### <span data-ttu-id="ffc35-139">Microsoft.Azure.Commands.Batch. PSCloudPool 모델</span><span class="sxs-lookup"><span data-stu-id="ffc35-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="ffc35-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ffc35-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ffc35-141">출력</span><span class="sxs-lookup"><span data-stu-id="ffc35-141">OUTPUTS</span></span>

### <span data-ttu-id="ffc35-142">Microsoft.Azure.Commands.Batch. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ffc35-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="ffc35-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ffc35-143">NOTES</span></span>

## <span data-ttu-id="ffc35-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffc35-144">RELATED LINKS</span></span>

[<span data-ttu-id="ffc35-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ffc35-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="ffc35-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="ffc35-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="ffc35-147">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ffc35-147">Azure Batch Cmdlets</span></span>]()
