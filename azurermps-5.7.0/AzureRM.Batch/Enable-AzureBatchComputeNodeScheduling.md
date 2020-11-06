---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 7cf3a056ec4266cccac577920f2f5b9292ce03be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534867"
---
# <span data-ttu-id="5277b-101">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="5277b-101">Enable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="5277b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5277b-102">SYNOPSIS</span></span>
<span data-ttu-id="5277b-103">지정 된 계산 노드에서 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-103">Enables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5277b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5277b-104">SYNTAX</span></span>

### <span data-ttu-id="5277b-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="5277b-105">Id (Default)</span></span>
```
Enable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5277b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5277b-106">InputObject</span></span>
```
Enable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5277b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5277b-107">DESCRIPTION</span></span>
<span data-ttu-id="5277b-108">AzureBatchComputeNodeScheduling cmdlet을 **사용** 하면 지정 된 계산 노드에서 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-108">The **Enable-AzureBatchComputeNodeScheduling** cmdlet enables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="5277b-109">계산 노드는 특정 응용 프로그램 작업을 전담 하는 Azure 가상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>

## <span data-ttu-id="5277b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5277b-110">EXAMPLES</span></span>

### <span data-ttu-id="5277b-111">예제 1: 계산 노드에서 작업 일정 사용</span><span class="sxs-lookup"><span data-stu-id="5277b-111">Example 1: Enable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Enable-AzureBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="5277b-112">이러한 명령은 계산 노드 tvm-1783593343_34-20151117t222514z에서 작업 일정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-112">These commands enable task scheduling on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="5277b-113">이렇게 하려면 예제의 첫 번째 명령은 batch 계정 contosobatchaccount의 계정 키를 포함 하는 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-113">To do this, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="5277b-114">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="5277b-115">그런 다음 두 번째 명령은이 개체 참조 및 **enable-AzureBatchComputeNodeScheduling** cmdlet을 사용 하 여 tvm-1783593343_34-20151117t222514z에서 풀 myPool에 연결 하 고 작업 예약을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-115">The second command then uses this object reference and the **Enable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and enable task scheduling on tvm-1783593343_34-20151117t222514z.</span></span>

### <span data-ttu-id="5277b-116">예제 2: 풀의 계산 노드에서 작업 예약 사용</span><span class="sxs-lookup"><span data-stu-id="5277b-116">Example 2: Enable task scheduling on compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzureBatchComputeNodeScheduling  -BatchContext $Context
```

<span data-ttu-id="5277b-117">이러한 명령을 사용 하면 풀 Pool06에 있는 모든 계산 노드에서 작업을 예약할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-117">These commands enable task scheduling on all the compute nodes found in the pool Pool06.</span></span>
<span data-ttu-id="5277b-118">이 작업을 수행 하기 위해 예제의 첫 번째 명령은 일괄 계정 contosobatchaccount의 계정 키를 포함 하는 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-118">To perform this task, the first command in the example creates an object reference containing the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="5277b-119">이 개체 참조는 $context 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-119">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="5277b-120">그런 다음이 예제의 두 번째 명령은이 개체 참조를 사용 하 여 Pool06에 있는 모든 계산 노드의 컬렉션을 반환 합니다. **AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="5277b-120">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="5277b-121">그런 다음 컬렉션의 각 계산 노드에서 작업 일정을 예약할 수 있도록 하는 **AzureBatchComputeNodeScheduling** cmdlet으로 해당 컬렉션을 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-121">That collection is then piped to the **Enable-AzureBatchComputeNodeScheduling** cmdlet, which enables task scheduling on each compute node in the collection.</span></span>

## <span data-ttu-id="5277b-122">변수</span><span class="sxs-lookup"><span data-stu-id="5277b-122">PARAMETERS</span></span>

### <span data-ttu-id="5277b-123">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5277b-123">-BatchContext</span></span>
<span data-ttu-id="5277b-124">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-124">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5277b-125">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-125">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5277b-126">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-126">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5277b-127">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-127">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5277b-128">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-128">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5277b-129">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="5277b-129">-ComputeNode</span></span>
<span data-ttu-id="5277b-130">작업 일정을 사용할 수 있는 계산 노드에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-130">Specifies an object reference to the compute node where task scheduling is enabled.</span></span>
<span data-ttu-id="5277b-131">이 개체 참조는 Get-AzureBatchComputeNode cmdlet을 사용 하 여 만들고 반환 된 계산 노드 개체를 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-131">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5277b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5277b-132">-DefaultProfile</span></span>
<span data-ttu-id="5277b-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5277b-134">-Id</span><span class="sxs-lookup"><span data-stu-id="5277b-134">-Id</span></span>
<span data-ttu-id="5277b-135">작업 일정을 사용할 수 있는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-135">Specifies the ID of the compute node where task scheduling is enabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5277b-136">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5277b-136">-PoolId</span></span>
<span data-ttu-id="5277b-137">작업 일정을 사용할 수 있는 계산 노드를 포함 하는 일괄 처리 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-137">Specifies the ID of the batch pool that contains the compute node where task scheduling is enabled.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5277b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5277b-138">CommonParameters</span></span>
<span data-ttu-id="5277b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5277b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5277b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5277b-141">입력</span><span class="sxs-lookup"><span data-stu-id="5277b-141">INPUTS</span></span>

### <span data-ttu-id="5277b-142">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5277b-142">BatchAccountContext</span></span>
<span data-ttu-id="5277b-143">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-143">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5277b-144">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="5277b-144">PSComputeNode</span></span>
<span data-ttu-id="5277b-145">' ComputeNode ' 매개 변수는 파이프라인에서 ' PSComputeNode ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5277b-145">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="5277b-146">출력</span><span class="sxs-lookup"><span data-stu-id="5277b-146">OUTPUTS</span></span>

## <span data-ttu-id="5277b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="5277b-147">NOTES</span></span>

## <span data-ttu-id="5277b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5277b-148">RELATED LINKS</span></span>

[<span data-ttu-id="5277b-149">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="5277b-149">Disable-AzureBatchComputeNodeScheduling</span></span>](./Disable-AzureBatchComputeNodeScheduling.md)

