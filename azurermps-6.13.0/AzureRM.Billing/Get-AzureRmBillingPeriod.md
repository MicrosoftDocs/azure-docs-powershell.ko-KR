---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533428"
---
# <span data-ttu-id="70fdd-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="70fdd-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="70fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="70fdd-103">구독 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70fdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70fdd-104">SYNTAX</span></span>

### <span data-ttu-id="70fdd-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="70fdd-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70fdd-106">단일</span><span class="sxs-lookup"><span data-stu-id="70fdd-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70fdd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="70fdd-107">DESCRIPTION</span></span>
<span data-ttu-id="70fdd-108">**AzureRmBillingPeriod** cmdlet은 구독 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="70fdd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="70fdd-109">EXAMPLES</span></span>

### <span data-ttu-id="70fdd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="70fdd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="70fdd-111">구독에 사용 가능한 모든 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="70fdd-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="70fdd-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="70fdd-113">지정 된 이름을 사용 하 여 구독에 대 한 청구 기간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="70fdd-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="70fdd-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="70fdd-115">구독에 대 한 최대 2 개의 청구 기간을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="70fdd-116">변수</span><span class="sxs-lookup"><span data-stu-id="70fdd-116">PARAMETERS</span></span>

### <span data-ttu-id="70fdd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fdd-117">-DefaultProfile</span></span>
<span data-ttu-id="70fdd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70fdd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70fdd-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="70fdd-119">-MaxCount</span></span>
<span data-ttu-id="70fdd-120">반환할 최대 레코드 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70fdd-121">-이름</span><span class="sxs-lookup"><span data-stu-id="70fdd-121">-Name</span></span>
<span data-ttu-id="70fdd-122">가져올 특정 청구 기간의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-122">Name of a specific billing period to get.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70fdd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fdd-123">CommonParameters</span></span>
<span data-ttu-id="70fdd-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70fdd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fdd-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70fdd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fdd-126">입력</span><span class="sxs-lookup"><span data-stu-id="70fdd-126">INPUTS</span></span>

### <span data-ttu-id="70fdd-127">않아야</span><span class="sxs-lookup"><span data-stu-id="70fdd-127">None</span></span>

## <span data-ttu-id="70fdd-128">출력</span><span class="sxs-lookup"><span data-stu-id="70fdd-128">OUTPUTS</span></span>

### <span data-ttu-id="70fdd-129">PSBillingPeriod를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="70fdd-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="70fdd-130">상속자</span><span class="sxs-lookup"><span data-stu-id="70fdd-130">NOTES</span></span>

## <span data-ttu-id="70fdd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70fdd-131">RELATED LINKS</span></span>