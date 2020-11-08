---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: 80cfa0453bf521ee8b29fb6a330ec194ada84383
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047244"
---
# <span data-ttu-id="6e8ac-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e8ac-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="6e8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8ac-103">작업의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="6e8ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e8ac-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e8ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e8ac-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8ac-106">**AzBatchTask** Cmdlet은 Azure Batch 서비스에서 작업의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="6e8ac-107">**Pscloudtask** 개체를 가져오려면 Get-AzBatchTask cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="6e8ac-108">해당 개체의 속성을 수정한 다음 현재 cmdlet을 사용 하 여 일괄 처리 서비스에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="6e8ac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6e8ac-109">EXAMPLES</span></span>

### <span data-ttu-id="6e8ac-110">예제 1: 작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="6e8ac-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="6e8ac-111">첫 번째 명령은 **Get-AzBatchTask** 를 사용 하 여 작업을 가져온 다음 $Task 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="6e8ac-112">다음 두 명령은 $Task 작업의 제약 조건을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="6e8ac-113">마지막 명령은 $Task의 로컬 개체와 일치 하도록 일괄 처리 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="6e8ac-114">변수</span><span class="sxs-lookup"><span data-stu-id="6e8ac-114">PARAMETERS</span></span>

### <span data-ttu-id="6e8ac-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6e8ac-115">-BatchContext</span></span>
<span data-ttu-id="6e8ac-116">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6e8ac-117">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6e8ac-118">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6e8ac-119">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6e8ac-120">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6e8ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8ac-121">-DefaultProfile</span></span>
<span data-ttu-id="6e8ac-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e8ac-123">-작업</span><span class="sxs-lookup"><span data-stu-id="6e8ac-123">-Task</span></span>
<span data-ttu-id="6e8ac-124">이 cmdlet이 일괄 처리 서비스를 업데이트 하는 **Pscloudtask** 를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8ac-125">CommonParameters</span></span>
<span data-ttu-id="6e8ac-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8ac-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e8ac-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8ac-128">입력</span><span class="sxs-lookup"><span data-stu-id="6e8ac-128">INPUTS</span></span>

### <span data-ttu-id="6e8ac-129">Microsoft.Azure.Commands.Batch. PSCloudTask에 대 한 모델</span><span class="sxs-lookup"><span data-stu-id="6e8ac-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="6e8ac-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6e8ac-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6e8ac-131">출력</span><span class="sxs-lookup"><span data-stu-id="6e8ac-131">OUTPUTS</span></span>

### <span data-ttu-id="6e8ac-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="6e8ac-132">System.Void</span></span>

## <span data-ttu-id="6e8ac-133">상속자</span><span class="sxs-lookup"><span data-stu-id="6e8ac-133">NOTES</span></span>

## <span data-ttu-id="6e8ac-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e8ac-134">RELATED LINKS</span></span>

[<span data-ttu-id="6e8ac-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e8ac-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="6e8ac-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="6e8ac-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6e8ac-137">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e8ac-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="6e8ac-138">제거-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e8ac-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="6e8ac-139">중지-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="6e8ac-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="6e8ac-140">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6e8ac-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

