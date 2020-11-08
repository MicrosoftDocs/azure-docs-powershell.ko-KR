---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216269"
---
# <span data-ttu-id="86def-101">Set-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-101">Set-AzBatchJob</span></span>

## <span data-ttu-id="86def-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86def-102">SYNOPSIS</span></span>
<span data-ttu-id="86def-103">일괄 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-103">Updates a Batch job.</span></span>

## <span data-ttu-id="86def-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86def-104">SYNTAX</span></span>

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86def-105">설명은</span><span class="sxs-lookup"><span data-stu-id="86def-105">DESCRIPTION</span></span>
<span data-ttu-id="86def-106">**AzBatchJob** Cmdlet은 Azure 일괄 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-106">The **Set-AzBatchJob** cmdlet updates an Azure Batch job.</span></span>
<span data-ttu-id="86def-107">**Pscloudjob** 개체를 가져오려면 Get-AzBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-107">Use the Get-AzBatchJob cmdlet to get a **PSCloudJob** object.</span></span>
<span data-ttu-id="86def-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="86def-109">예제의</span><span class="sxs-lookup"><span data-stu-id="86def-109">EXAMPLES</span></span>

### <span data-ttu-id="86def-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="86def-110">Example 1: Update a job</span></span>
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

<span data-ttu-id="86def-111">첫 번째 명령은 **Get-AzBatchJob** 를 사용 하 여 작업을 가져온 다음 $Job 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-111">The first command gets a job by using **Get-AzBatchJob** , and then stores it in the $Job variable.</span></span>
<span data-ttu-id="86def-112">두 번째 명령은 $Job 개체에 대 한 우선 순위 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-112">The second command modifies the priority specification on the $Job object.</span></span>
<span data-ttu-id="86def-113">마지막 명령은 $Job의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-113">The final command updates the Batch service to match the local object in $Job.</span></span>

## <span data-ttu-id="86def-114">변수</span><span class="sxs-lookup"><span data-stu-id="86def-114">PARAMETERS</span></span>

### <span data-ttu-id="86def-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="86def-115">-BatchContext</span></span>
<span data-ttu-id="86def-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="86def-117">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86def-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="86def-118">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86def-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="86def-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86def-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="86def-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="86def-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86def-121">-DefaultProfile</span></span>
<span data-ttu-id="86def-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86def-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86def-123">-작업</span><span class="sxs-lookup"><span data-stu-id="86def-123">-Job</span></span>
<span data-ttu-id="86def-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudjob** 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-124">Specifies a **PSCloudJob** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86def-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86def-125">CommonParameters</span></span>
<span data-ttu-id="86def-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86def-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86def-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86def-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86def-128">입력</span><span class="sxs-lookup"><span data-stu-id="86def-128">INPUTS</span></span>

### <span data-ttu-id="86def-129">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="86def-129">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="86def-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="86def-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="86def-131">출력</span><span class="sxs-lookup"><span data-stu-id="86def-131">OUTPUTS</span></span>

### <span data-ttu-id="86def-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="86def-132">System.Void</span></span>

## <span data-ttu-id="86def-133">상속자</span><span class="sxs-lookup"><span data-stu-id="86def-133">NOTES</span></span>

## <span data-ttu-id="86def-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86def-134">RELATED LINKS</span></span>

[<span data-ttu-id="86def-135">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-135">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="86def-136">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-136">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="86def-137">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-137">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="86def-138">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="86def-138">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="86def-139">새로운 AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-139">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="86def-140">제거-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-140">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="86def-141">중지-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="86def-141">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="86def-142">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="86def-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)