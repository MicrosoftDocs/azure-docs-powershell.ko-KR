---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217071"
---
# <span data-ttu-id="1e06e-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="1e06e-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="1e06e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e06e-102">SYNOPSIS</span></span>
<span data-ttu-id="1e06e-103">일괄 처리 계산 노드에서 사용자 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="1e06e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e06e-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e06e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e06e-105">DESCRIPTION</span></span>
<span data-ttu-id="1e06e-106">**AzBatchComputeNodeUser** Cmdlet은 Azure Batch compute 노드에서 사용자 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="1e06e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e06e-107">EXAMPLES</span></span>

### <span data-ttu-id="1e06e-108">예제 1: 확인 하지 않고 계산 노드에서 사용자 삭제</span><span class="sxs-lookup"><span data-stu-id="1e06e-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="1e06e-109">이 명령은 ComputeNode01 이라는 계산 노드에서 User14 이라는 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="1e06e-110">계산 노드는 Pool01 라는 풀에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="1e06e-111">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1e06e-112">따라서 명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1e06e-113">변수</span><span class="sxs-lookup"><span data-stu-id="1e06e-113">PARAMETERS</span></span>

### <span data-ttu-id="1e06e-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1e06e-114">-BatchContext</span></span>
<span data-ttu-id="1e06e-115">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1e06e-116">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1e06e-117">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1e06e-118">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1e06e-119">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1e06e-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="1e06e-120">-ComputeNodeId</span></span>
<span data-ttu-id="1e06e-121">이 cmdlet이 사용자 계정을 삭제 하는 계산 노드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e06e-122">-DefaultProfile</span></span>
<span data-ttu-id="1e06e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e06e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1e06e-124">-Name</span></span>
<span data-ttu-id="1e06e-125">삭제할 사용자 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="1e06e-126">와일드 카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e06e-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1e06e-127">-PoolId</span></span>
<span data-ttu-id="1e06e-128">사용자 계정을 삭제할 계산 노드가 포함 된 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="1e06e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1e06e-129">-Confirm</span></span>
<span data-ttu-id="1e06e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e06e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e06e-131">-WhatIf</span></span>
<span data-ttu-id="1e06e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e06e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e06e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e06e-134">CommonParameters</span></span>
<span data-ttu-id="1e06e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e06e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e06e-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e06e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e06e-137">입력</span><span class="sxs-lookup"><span data-stu-id="1e06e-137">INPUTS</span></span>

### <span data-ttu-id="1e06e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e06e-138">System.String</span></span>

### <span data-ttu-id="1e06e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1e06e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1e06e-140">출력</span><span class="sxs-lookup"><span data-stu-id="1e06e-140">OUTPUTS</span></span>

### <span data-ttu-id="1e06e-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1e06e-141">System.Void</span></span>

## <span data-ttu-id="1e06e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1e06e-142">NOTES</span></span>

## <span data-ttu-id="1e06e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e06e-143">RELATED LINKS</span></span>

[<span data-ttu-id="1e06e-144">새로운 AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="1e06e-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="1e06e-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1e06e-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1e06e-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e06e-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)