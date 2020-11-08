---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047071"
---
# <span data-ttu-id="10aaf-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="10aaf-101">Set-AzsOffer</span></span>

## <span data-ttu-id="10aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="10aaf-103">제안을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-103">Update the offer.</span></span>

## <span data-ttu-id="10aaf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10aaf-104">SYNTAX</span></span>

### <span data-ttu-id="10aaf-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="10aaf-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10aaf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="10aaf-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10aaf-107">리소스</span><span class="sxs-lookup"><span data-stu-id="10aaf-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10aaf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="10aaf-108">DESCRIPTION</span></span>
<span data-ttu-id="10aaf-109">제안을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-109">Update the offer.</span></span>

## <span data-ttu-id="10aaf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="10aaf-110">EXAMPLES</span></span>

### <span data-ttu-id="10aaf-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="10aaf-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="10aaf-112">제안을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-112">Update the offer.</span></span>

## <span data-ttu-id="10aaf-113">변수</span><span class="sxs-lookup"><span data-stu-id="10aaf-113">PARAMETERS</span></span>

### <span data-ttu-id="10aaf-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="10aaf-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="10aaf-115">테 넌 트가 제공의 일부로 선택적으로 얻을 수 있는 추가 기능 계획에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-116">-Base계획 Id</span><span class="sxs-lookup"><span data-stu-id="10aaf-116">-BasePlanIds</span></span>
<span data-ttu-id="10aaf-117">테 넌 트가 제안에 구독 하는 즉시 테 넌 트에 사용할 수 있는 기본 계획의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-118">-설명</span><span class="sxs-lookup"><span data-stu-id="10aaf-118">-Description</span></span>
<span data-ttu-id="10aaf-119">제안에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="10aaf-120">-DisplayName</span></span>
<span data-ttu-id="10aaf-121">제공의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="10aaf-122">-ExternalReferenceId</span></span>
<span data-ttu-id="10aaf-123">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10aaf-124">-InputObject</span></span>
<span data-ttu-id="10aaf-125">' AzureStack i a i.. i a i. 관리.</span><span class="sxs-lookup"><span data-stu-id="10aaf-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-126">-위치</span><span class="sxs-lookup"><span data-stu-id="10aaf-126">-Location</span></span>
<span data-ttu-id="10aaf-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="10aaf-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="10aaf-129">계정 당 최대 구독 수.</span><span class="sxs-lookup"><span data-stu-id="10aaf-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-130">-이름</span><span class="sxs-lookup"><span data-stu-id="10aaf-130">-Name</span></span>
<span data-ttu-id="10aaf-131">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10aaf-132">-ResourceGroupName</span></span>
<span data-ttu-id="10aaf-133">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10aaf-134">-ResourceId</span></span>
<span data-ttu-id="10aaf-135">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-136">-상태</span><span class="sxs-lookup"><span data-stu-id="10aaf-136">-State</span></span>
<span data-ttu-id="10aaf-137">접근성 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-138">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="10aaf-138">-SubscriptionCount</span></span>
<span data-ttu-id="10aaf-139">현재 구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10aaf-140">-확인</span><span class="sxs-lookup"><span data-stu-id="10aaf-140">-Confirm</span></span>
<span data-ttu-id="10aaf-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10aaf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10aaf-142">-WhatIf</span></span>
<span data-ttu-id="10aaf-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10aaf-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10aaf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10aaf-145">CommonParameters</span></span>
<span data-ttu-id="10aaf-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10aaf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10aaf-147">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10aaf-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10aaf-148">입력</span><span class="sxs-lookup"><span data-stu-id="10aaf-148">INPUTS</span></span>

## <span data-ttu-id="10aaf-149">출력</span><span class="sxs-lookup"><span data-stu-id="10aaf-149">OUTPUTS</span></span>

### <span data-ttu-id="10aaf-150">Microsoft AzureStack. 관리. 관리자. 제공</span><span class="sxs-lookup"><span data-stu-id="10aaf-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="10aaf-151">상속자</span><span class="sxs-lookup"><span data-stu-id="10aaf-151">NOTES</span></span>

## <span data-ttu-id="10aaf-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10aaf-152">RELATED LINKS</span></span>
