---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211669"
---
# <span data-ttu-id="e636a-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="e636a-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="e636a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e636a-102">SYNOPSIS</span></span>
<span data-ttu-id="e636a-103">지정 된 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e636a-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="e636a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e636a-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e636a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e636a-105">DESCRIPTION</span></span>
<span data-ttu-id="e636a-106">사용 된 리소스를 비롯 하 여 계획에 남아 있는 리소스를 포함 하 여 특정 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e636a-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="e636a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e636a-107">EXAMPLES</span></span>

### <span data-ttu-id="e636a-108">예제 1: 특정 약정 계획에 대 한 사용 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="e636a-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="e636a-109">변수</span><span class="sxs-lookup"><span data-stu-id="e636a-109">PARAMETERS</span></span>

### <span data-ttu-id="e636a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e636a-110">-DefaultProfile</span></span>
<span data-ttu-id="e636a-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e636a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e636a-112">-이름</span><span class="sxs-lookup"><span data-stu-id="e636a-112">-Name</span></span>
<span data-ttu-id="e636a-113">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e636a-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e636a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e636a-114">-ResourceGroupName</span></span>
<span data-ttu-id="e636a-115">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e636a-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="e636a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e636a-116">CommonParameters</span></span>
<span data-ttu-id="e636a-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e636a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e636a-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e636a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e636a-119">입력</span><span class="sxs-lookup"><span data-stu-id="e636a-119">INPUTS</span></span>

### <span data-ttu-id="e636a-120">않아야</span><span class="sxs-lookup"><span data-stu-id="e636a-120">None</span></span>

## <span data-ttu-id="e636a-121">출력</span><span class="sxs-lookup"><span data-stu-id="e636a-121">OUTPUTS</span></span>

### <span data-ttu-id="e636a-122">MachineLearning. CommitmentPlans. \ PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="e636a-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="e636a-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e636a-123">NOTES</span></span>
<span data-ttu-id="e636a-124">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="e636a-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e636a-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e636a-125">RELATED LINKS</span></span>