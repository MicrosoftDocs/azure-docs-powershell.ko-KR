---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046694"
---
# <span data-ttu-id="fb172-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="fb172-101">New-OfferObject</span></span>

## <span data-ttu-id="fb172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb172-102">SYNOPSIS</span></span>
<span data-ttu-id="fb172-103">구독을 만들 수 있는 서비스를 제공 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="fb172-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb172-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="fb172-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb172-105">DESCRIPTION</span></span>
<span data-ttu-id="fb172-106">구독을 만들 수 있는 서비스를 제공 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="fb172-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb172-107">EXAMPLES</span></span>

### <span data-ttu-id="fb172-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb172-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fb172-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="fb172-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fb172-110">변수</span><span class="sxs-lookup"><span data-stu-id="fb172-110">PARAMETERS</span></span>

### <span data-ttu-id="fb172-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="fb172-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="fb172-112">테 넌 트가 제공의 일부로 선택적으로 얻을 수 있는 추가 기능 계획에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-113">-Base계획 Id</span><span class="sxs-lookup"><span data-stu-id="fb172-113">-BasePlanIds</span></span>
<span data-ttu-id="fb172-114">테 넌 트가 제안에 구독 하는 즉시 테 넌 트에 사용할 수 있는 기본 계획의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-115">-설명</span><span class="sxs-lookup"><span data-stu-id="fb172-115">-Description</span></span>
<span data-ttu-id="fb172-116">제안에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-116">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fb172-117">-DisplayName</span></span>
<span data-ttu-id="fb172-118">제공의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-118">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="fb172-119">-ExternalReferenceId</span></span>
<span data-ttu-id="fb172-120">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-121">-Id</span><span class="sxs-lookup"><span data-stu-id="fb172-121">-Id</span></span>
<span data-ttu-id="fb172-122">리소스의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-122">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-123">-위치</span><span class="sxs-lookup"><span data-stu-id="fb172-123">-Location</span></span>
<span data-ttu-id="fb172-124">리소스가 위치 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-124">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="fb172-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="fb172-126">계정 당 최대 구독 수.</span><span class="sxs-lookup"><span data-stu-id="fb172-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-127">-이름</span><span class="sxs-lookup"><span data-stu-id="fb172-127">-Name</span></span>
<span data-ttu-id="fb172-128">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-128">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-129">-상태</span><span class="sxs-lookup"><span data-stu-id="fb172-129">-State</span></span>
<span data-ttu-id="fb172-130">접근성 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-130">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-131">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="fb172-131">-SubscriptionCount</span></span>
<span data-ttu-id="fb172-132">현재 구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-133">태그</span><span class="sxs-lookup"><span data-stu-id="fb172-133">-Tags</span></span>
<span data-ttu-id="fb172-134">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-135">-Type</span><span class="sxs-lookup"><span data-stu-id="fb172-135">-Type</span></span>
<span data-ttu-id="fb172-136">리소스의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-136">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb172-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb172-137">CommonParameters</span></span>
<span data-ttu-id="fb172-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb172-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb172-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb172-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb172-140">입력</span><span class="sxs-lookup"><span data-stu-id="fb172-140">INPUTS</span></span>

## <span data-ttu-id="fb172-141">출력</span><span class="sxs-lookup"><span data-stu-id="fb172-141">OUTPUTS</span></span>

## <span data-ttu-id="fb172-142">상속자</span><span class="sxs-lookup"><span data-stu-id="fb172-142">NOTES</span></span>

## <span data-ttu-id="fb172-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb172-143">RELATED LINKS</span></span>
