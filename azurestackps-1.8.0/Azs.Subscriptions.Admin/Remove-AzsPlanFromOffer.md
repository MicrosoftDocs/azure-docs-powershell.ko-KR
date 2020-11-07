---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874789"
---
# <span data-ttu-id="b26fc-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="b26fc-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="b26fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b26fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b26fc-103">제안에서 계획의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="b26fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b26fc-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b26fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b26fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b26fc-106">제안에서 계획의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="b26fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b26fc-107">EXAMPLES</span></span>

### <span data-ttu-id="b26fc-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b26fc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="b26fc-109">변수</span><span class="sxs-lookup"><span data-stu-id="b26fc-109">PARAMETERS</span></span>

### <span data-ttu-id="b26fc-110">-Force</span><span class="sxs-lookup"><span data-stu-id="b26fc-110">-Force</span></span>
<span data-ttu-id="b26fc-111">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-111">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="b26fc-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="b26fc-113">구독자 별 최대 획득 수</span><span class="sxs-lookup"><span data-stu-id="b26fc-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="b26fc-114">-OfferName</span></span>
<span data-ttu-id="b26fc-115">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-116">-계획 Linktype</span><span class="sxs-lookup"><span data-stu-id="b26fc-116">-PlanLinkType</span></span>
<span data-ttu-id="b26fc-117">계획 링크의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-118">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="b26fc-118">-PlanName</span></span>
<span data-ttu-id="b26fc-119">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b26fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="b26fc-121">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b26fc-122">-Confirm</span></span>
<span data-ttu-id="b26fc-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b26fc-124">-WhatIf</span></span>
<span data-ttu-id="b26fc-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b26fc-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b26fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b26fc-127">CommonParameters</span></span>
<span data-ttu-id="b26fc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b26fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b26fc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b26fc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b26fc-130">입력</span><span class="sxs-lookup"><span data-stu-id="b26fc-130">INPUTS</span></span>

## <span data-ttu-id="b26fc-131">출력</span><span class="sxs-lookup"><span data-stu-id="b26fc-131">OUTPUTS</span></span>

## <span data-ttu-id="b26fc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b26fc-132">NOTES</span></span>

## <span data-ttu-id="b26fc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b26fc-133">RELATED LINKS</span></span>
