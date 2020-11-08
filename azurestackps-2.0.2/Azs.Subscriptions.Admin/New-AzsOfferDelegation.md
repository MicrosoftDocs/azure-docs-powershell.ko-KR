---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047143"
---
# <span data-ttu-id="5ff47-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5ff47-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="5ff47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff47-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff47-103">제공 위임을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="5ff47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ff47-104">SYNTAX</span></span>

### <span data-ttu-id="5ff47-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ff47-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ff47-106">만드는</span><span class="sxs-lookup"><span data-stu-id="5ff47-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ff47-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5ff47-107">DESCRIPTION</span></span>
<span data-ttu-id="5ff47-108">제공 위임을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="5ff47-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5ff47-109">EXAMPLES</span></span>

### <span data-ttu-id="5ff47-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ff47-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="5ff47-111">새 제공 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="5ff47-112">변수</span><span class="sxs-lookup"><span data-stu-id="5ff47-112">PARAMETERS</span></span>

### <span data-ttu-id="5ff47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff47-113">-DefaultProfile</span></span>
<span data-ttu-id="5ff47-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ff47-115">-위치</span><span class="sxs-lookup"><span data-stu-id="5ff47-115">-Location</span></span>
<span data-ttu-id="5ff47-116">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5ff47-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ff47-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5ff47-117">-Name</span></span>
<span data-ttu-id="5ff47-118">제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="5ff47-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="5ff47-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="5ff47-120">위임을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-120">Offer delegation.</span></span>
<span data-ttu-id="5ff47-121">생성 하려면 OFFERDELEGATIONDEFINITION 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5ff47-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="5ff47-122">-OfferName</span></span>
<span data-ttu-id="5ff47-123">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-123">Name of an offer.</span></span>

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

### <span data-ttu-id="5ff47-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff47-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ff47-125">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="5ff47-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ff47-126">-SubscriptionId</span></span>
<span data-ttu-id="5ff47-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ff47-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ff47-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="5ff47-129">위임 된 제안을 받는 구독의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-129">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5ff47-130">-확인</span><span class="sxs-lookup"><span data-stu-id="5ff47-130">-Confirm</span></span>
<span data-ttu-id="5ff47-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff47-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff47-132">-WhatIf</span></span>
<span data-ttu-id="5ff47-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff47-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff47-135">CommonParameters</span></span>
<span data-ttu-id="5ff47-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff47-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5ff47-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff47-138">입력</span><span class="sxs-lookup"><span data-stu-id="5ff47-138">INPUTS</span></span>

### <span data-ttu-id="5ff47-139">SubscriptionsAdmin. Api20151101. IOfferDelegation에 대 한</span><span class="sxs-lookup"><span data-stu-id="5ff47-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="5ff47-140">출력</span><span class="sxs-lookup"><span data-stu-id="5ff47-140">OUTPUTS</span></span>

### <span data-ttu-id="5ff47-141">SubscriptionsAdmin. Api20151101. IOfferDelegation에 대 한</span><span class="sxs-lookup"><span data-stu-id="5ff47-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="5ff47-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="5ff47-142">ALIASES</span></span>

## <span data-ttu-id="5ff47-143">상속자</span><span class="sxs-lookup"><span data-stu-id="5ff47-143">NOTES</span></span>

<span data-ttu-id="5ff47-144">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ff47-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="5ff47-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5ff47-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : 위임을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="5ff47-147">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="5ff47-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="5ff47-148">`[SubscriptionId <String>]`: 위임 된 제안을 받는 구독의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5ff47-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="5ff47-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ff47-149">RELATED LINKS</span></span>
