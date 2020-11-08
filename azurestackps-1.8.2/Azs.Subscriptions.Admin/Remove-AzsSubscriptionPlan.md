---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046810"
---
# <span data-ttu-id="e6a0c-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="e6a0c-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="e6a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a0c-103">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="e6a0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6a0c-104">SYNTAX</span></span>

### <span data-ttu-id="e6a0c-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6a0c-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6a0c-106">리소스</span><span class="sxs-lookup"><span data-stu-id="e6a0c-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a0c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e6a0c-107">DESCRIPTION</span></span>
<span data-ttu-id="e6a0c-108">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="e6a0c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e6a0c-109">EXAMPLES</span></span>

### <span data-ttu-id="e6a0c-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e6a0c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e6a0c-111">구독 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="e6a0c-112">변수</span><span class="sxs-lookup"><span data-stu-id="e6a0c-112">PARAMETERS</span></span>

### <span data-ttu-id="e6a0c-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="e6a0c-113">-AcquisitionId</span></span>
<span data-ttu-id="e6a0c-114">계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="e6a0c-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e6a0c-115">-Force</span></span>
<span data-ttu-id="e6a0c-116">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e6a0c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6a0c-117">-ResourceId</span></span>
<span data-ttu-id="e6a0c-118">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-118">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0c-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6a0c-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="e6a0c-120">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e6a0c-121">-Confirm</span></span>
<span data-ttu-id="e6a0c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a0c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a0c-123">-WhatIf</span></span>
<span data-ttu-id="e6a0c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6a0c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a0c-126">CommonParameters</span></span>
<span data-ttu-id="e6a0c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6a0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a0c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a0c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a0c-129">입력</span><span class="sxs-lookup"><span data-stu-id="e6a0c-129">INPUTS</span></span>

## <span data-ttu-id="e6a0c-130">출력</span><span class="sxs-lookup"><span data-stu-id="e6a0c-130">OUTPUTS</span></span>

## <span data-ttu-id="e6a0c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e6a0c-131">NOTES</span></span>

## <span data-ttu-id="e6a0c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6a0c-132">RELATED LINKS</span></span>
