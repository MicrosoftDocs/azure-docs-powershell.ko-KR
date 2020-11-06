---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C831F934-7513-4882-A155-816E56CD9807
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJob.md
ms.openlocfilehash: fcb3586d1c27fd95c6bf386943830b92635162e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538024"
---
# <span data-ttu-id="5ffca-101">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5ffca-101">Disable-AzureBatchJob</span></span>

## <span data-ttu-id="5ffca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ffca-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffca-103">일괄 작업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-103">Disables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ffca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ffca-104">SYNTAX</span></span>

```
Disable-AzureBatchJob [-Id] <String> [-DisableJobOption] <DisableJobOption> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ffca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ffca-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffca-106">**-AzureBatchJob** Cmdlet은 Azure 일괄 작업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-106">The **Disable-AzureBatchJob** cmdlet disables an Azure Batch job.</span></span>
<span data-ttu-id="5ffca-107">작업을 사용 하도록 설정한 후에는 새 작업을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-107">After you enable a job, new tasks can run.</span></span>
<span data-ttu-id="5ffca-108">비활성화 된 작업은 새 작업을 실행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-108">Disabled jobs do not run new tasks.</span></span>
<span data-ttu-id="5ffca-109">나중에 비활성화 된 작업을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-109">You can enable a disabled job later.</span></span>

## <span data-ttu-id="5ffca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5ffca-110">EXAMPLES</span></span>

### <span data-ttu-id="5ffca-111">예제 1: 일괄 처리 작업 비활성화</span><span class="sxs-lookup"><span data-stu-id="5ffca-111">Example 1: Disable a Batch job</span></span>
```
PS C:\>Disable-AzureBatchJob -Id "Job-000001" -DisableJobOption "Terminate" -BatchContext $Context
```

<span data-ttu-id="5ffca-112">이 명령은 ID 작업-000001가 있는 작업을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-112">This command disables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="5ffca-113">명령은 작업에 대 한 활성 작업을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-113">The command terminates active tasks for the job.</span></span>
<span data-ttu-id="5ffca-114">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzureRmBatchAccountKeys** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="5ffca-115">변수</span><span class="sxs-lookup"><span data-stu-id="5ffca-115">PARAMETERS</span></span>

### <span data-ttu-id="5ffca-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5ffca-116">-BatchContext</span></span>
<span data-ttu-id="5ffca-117">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5ffca-118">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5ffca-119">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5ffca-120">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5ffca-121">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5ffca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffca-122">-DefaultProfile</span></span>
<span data-ttu-id="5ffca-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ffca-124">-DisableJobOption</span><span class="sxs-lookup"><span data-stu-id="5ffca-124">-DisableJobOption</span></span>
<span data-ttu-id="5ffca-125">이 cmdlet이 사용 하지 않도록 설정 하는 작업과 연결 된 활성 작업으로 수행할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-125">Specifies what to do with active tasks associated with the job that this cmdlet disables.</span></span>
<span data-ttu-id="5ffca-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-126">Valid values are:</span></span> 

- <span data-ttu-id="5ffca-127">Requeue</span><span class="sxs-lookup"><span data-stu-id="5ffca-127">Requeue</span></span> 
- <span data-ttu-id="5ffca-128">종료</span><span class="sxs-lookup"><span data-stu-id="5ffca-128">Terminate</span></span> 
- <span data-ttu-id="5ffca-129">Wait</span><span class="sxs-lookup"><span data-stu-id="5ffca-129">Wait</span></span>

```yaml
Type: DisableJobOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, Wait

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffca-130">-Id</span><span class="sxs-lookup"><span data-stu-id="5ffca-130">-Id</span></span>
<span data-ttu-id="5ffca-131">이 cmdlet이 사용 하지 않도록 설정할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-131">Specifies the ID of the job that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffca-132">CommonParameters</span></span>
<span data-ttu-id="5ffca-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffca-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ffca-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffca-135">입력</span><span class="sxs-lookup"><span data-stu-id="5ffca-135">INPUTS</span></span>

### <span data-ttu-id="5ffca-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5ffca-136">BatchAccountContext</span></span>
<span data-ttu-id="5ffca-137">' BatchContext ' 매개 변수는 파이프라인에서 ' BatchAccountContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="5ffca-138">이름</span><span class="sxs-lookup"><span data-stu-id="5ffca-138">String</span></span>
<span data-ttu-id="5ffca-139">' I d ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ffca-139">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5ffca-140">출력</span><span class="sxs-lookup"><span data-stu-id="5ffca-140">OUTPUTS</span></span>

## <span data-ttu-id="5ffca-141">상속자</span><span class="sxs-lookup"><span data-stu-id="5ffca-141">NOTES</span></span>

## <span data-ttu-id="5ffca-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ffca-142">RELATED LINKS</span></span>

[<span data-ttu-id="5ffca-143">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5ffca-143">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="5ffca-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5ffca-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5ffca-145">가져오기-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5ffca-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="5ffca-146">새-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5ffca-146">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="5ffca-147">-AzureBatchJob 제거</span><span class="sxs-lookup"><span data-stu-id="5ffca-147">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="5ffca-148">중지-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="5ffca-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="5ffca-149">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ffca-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

