---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d2745a0dd73141c1da7d049494e3a1545ee92599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535835"
---
# <span data-ttu-id="3e46e-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3e46e-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="3e46e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e46e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e46e-103">새 약정 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e46e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e46e-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e46e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e46e-105">DESCRIPTION</span></span>
<span data-ttu-id="3e46e-106">기존 리소스 그룹에 Azure 기계 학습 약정 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="3e46e-107">동일한 이름의 약정 계획이 리소스 그룹에 있는 경우 해당 호출이 업데이트 작업으로 작동 하 고 기존 약정 계획을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="3e46e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3e46e-108">EXAMPLES</span></span>

### <span data-ttu-id="3e46e-109">예제 1: 새 약정 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="3e46e-109">Example 1: Create a new commitment plan</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="3e46e-110">"MyResourceGroup" 그룹 및 미국 중부 US 지역에서 "MyCommitmentPlanName" 이라는 새 Azure 기계 학습 약정 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="3e46e-111">이 예제에서는 DevTest/Standard가 사용 되며, 약정 계획에서 제공 하는 리소스가 DevTest/Standard의 한계로 인해 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="3e46e-112">이 예제에서 SkuCapacity는 계획 비용의 1x가 DevTest 것을 의미 하 고, 계획에 포함 된 리소스는 DevTest에서 제공 하는 1x가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="3e46e-113">변수</span><span class="sxs-lookup"><span data-stu-id="3e46e-113">PARAMETERS</span></span>

### <span data-ttu-id="3e46e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e46e-114">-DefaultProfile</span></span>
<span data-ttu-id="3e46e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3e46e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e46e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3e46e-116">-Force</span></span>
<span data-ttu-id="3e46e-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e46e-118">-위치</span><span class="sxs-lookup"><span data-stu-id="3e46e-118">-Location</span></span>
<span data-ttu-id="3e46e-119">Azure ML 약정 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3e46e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="3e46e-120">-Name</span></span>
<span data-ttu-id="3e46e-121">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3e46e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e46e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e46e-123">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3e46e-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3e46e-124">-SkuCapacity</span></span>
<span data-ttu-id="3e46e-125">Azure ML 약정 계획을 구축할 때 사용할 SKU의 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3e46e-126">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="3e46e-126">-SkuName</span></span>
<span data-ttu-id="3e46e-127">Azure ML 약정 계획을 구축할 때 사용할 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3e46e-128">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="3e46e-128">-SkuTier</span></span>
<span data-ttu-id="3e46e-129">Azure ML 약정 계획을 구축할 때 사용할 SKU의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3e46e-130">-확인</span><span class="sxs-lookup"><span data-stu-id="3e46e-130">-Confirm</span></span>
<span data-ttu-id="3e46e-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e46e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e46e-132">-WhatIf</span></span>
<span data-ttu-id="3e46e-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e46e-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e46e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e46e-135">CommonParameters</span></span>
<span data-ttu-id="3e46e-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e46e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e46e-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e46e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e46e-138">입력</span><span class="sxs-lookup"><span data-stu-id="3e46e-138">INPUTS</span></span>

### <span data-ttu-id="3e46e-139">않아야</span><span class="sxs-lookup"><span data-stu-id="3e46e-139">None</span></span>

## <span data-ttu-id="3e46e-140">출력</span><span class="sxs-lookup"><span data-stu-id="3e46e-140">OUTPUTS</span></span>

### <span data-ttu-id="3e46e-141">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="3e46e-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="3e46e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="3e46e-142">NOTES</span></span>
<span data-ttu-id="3e46e-143">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="3e46e-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3e46e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e46e-144">RELATED LINKS</span></span>