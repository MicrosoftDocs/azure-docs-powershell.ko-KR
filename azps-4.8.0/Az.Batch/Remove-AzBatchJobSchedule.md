---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056552"
---
# <span data-ttu-id="2b89f-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="2b89f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b89f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b89f-103">일괄 작업 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="2b89f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b89f-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b89f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b89f-105">DESCRIPTION</span></span>
<span data-ttu-id="2b89f-106">**AzBatchJobSchedule** Cmdlet은 Azure Batch 작업 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="2b89f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b89f-107">EXAMPLES</span></span>

### <span data-ttu-id="2b89f-108">예제 1: 일괄 작업 일정 삭제</span><span class="sxs-lookup"><span data-stu-id="2b89f-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="2b89f-109">이 명령은 ID MyJobSchedule 인 작업 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="2b89f-110">이 명령은 작업을 삭제 하기 전에 확인을 요청 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="2b89f-111">Get-AzBatchAccountKey cmdlet을 사용 하 여 컨텍스트를 $Context 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2b89f-112">예제 2: 파이프라인을 사용 하 여 확인 없이 일괄 작업 삭제</span><span class="sxs-lookup"><span data-stu-id="2b89f-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="2b89f-113">이 명령은 Get-AzBatchJobSchedule cmdlet을 사용 하 여 ID MyJobSchedule 인 작업 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="2b89f-114">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업 일정을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2b89f-115">이 명령은 해당 작업 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="2b89f-116">명령에 *Force* 매개 변수가 포함 되어 있기 때문에 확인을 요청 하는 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="2b89f-117">변수</span><span class="sxs-lookup"><span data-stu-id="2b89f-117">PARAMETERS</span></span>

### <span data-ttu-id="2b89f-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2b89f-118">-BatchContext</span></span>
<span data-ttu-id="2b89f-119">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2b89f-120">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2b89f-121">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2b89f-122">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2b89f-123">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2b89f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b89f-124">-DefaultProfile</span></span>
<span data-ttu-id="2b89f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b89f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2b89f-126">-Force</span></span>
<span data-ttu-id="2b89f-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b89f-128">-Id</span><span class="sxs-lookup"><span data-stu-id="2b89f-128">-Id</span></span>
<span data-ttu-id="2b89f-129">제거할 작업 일정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-129">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b89f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="2b89f-130">-Confirm</span></span>
<span data-ttu-id="2b89f-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b89f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b89f-132">-WhatIf</span></span>
<span data-ttu-id="2b89f-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b89f-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b89f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b89f-135">CommonParameters</span></span>
<span data-ttu-id="2b89f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b89f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b89f-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b89f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b89f-138">입력</span><span class="sxs-lookup"><span data-stu-id="2b89f-138">INPUTS</span></span>

### <span data-ttu-id="2b89f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b89f-139">System.String</span></span>

### <span data-ttu-id="2b89f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2b89f-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2b89f-141">출력</span><span class="sxs-lookup"><span data-stu-id="2b89f-141">OUTPUTS</span></span>

### <span data-ttu-id="2b89f-142">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2b89f-142">System.Void</span></span>

## <span data-ttu-id="2b89f-143">상속자</span><span class="sxs-lookup"><span data-stu-id="2b89f-143">NOTES</span></span>

## <span data-ttu-id="2b89f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b89f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2b89f-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="2b89f-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="2b89f-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="2b89f-148">새로운 AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="2b89f-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="2b89f-150">중지-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="2b89f-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

