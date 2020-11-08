---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045129"
---
# <span data-ttu-id="64b22-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="64b22-101">New-AzsPlan</span></span>

## <span data-ttu-id="64b22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b22-102">SYNOPSIS</span></span>
<span data-ttu-id="64b22-103">계획을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-103">Create or update the plan.</span></span>

## <span data-ttu-id="64b22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64b22-104">SYNTAX</span></span>

### <span data-ttu-id="64b22-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="64b22-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="64b22-106">만드는</span><span class="sxs-lookup"><span data-stu-id="64b22-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64b22-107">설명은</span><span class="sxs-lookup"><span data-stu-id="64b22-107">DESCRIPTION</span></span>
<span data-ttu-id="64b22-108">계획을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-108">Create or update the plan.</span></span>

## <span data-ttu-id="64b22-109">예제의</span><span class="sxs-lookup"><span data-stu-id="64b22-109">EXAMPLES</span></span>

### <span data-ttu-id="64b22-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="64b22-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="64b22-111">새 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="64b22-111">Creates a new plan</span></span>

## <span data-ttu-id="64b22-112">변수</span><span class="sxs-lookup"><span data-stu-id="64b22-112">PARAMETERS</span></span>

### <span data-ttu-id="64b22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b22-113">-DefaultProfile</span></span>
<span data-ttu-id="64b22-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b22-115">-설명</span><span class="sxs-lookup"><span data-stu-id="64b22-115">-Description</span></span>
<span data-ttu-id="64b22-116">계획에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-116">Description of the plan.</span></span>

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

### <span data-ttu-id="64b22-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64b22-117">-DisplayName</span></span>
<span data-ttu-id="64b22-118">표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-118">Display name.</span></span>

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

### <span data-ttu-id="64b22-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="64b22-119">-ExternalReferenceId</span></span>
<span data-ttu-id="64b22-120">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-120">External reference identifier.</span></span>

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

### <span data-ttu-id="64b22-121">-위치</span><span class="sxs-lookup"><span data-stu-id="64b22-121">-Location</span></span>
<span data-ttu-id="64b22-122">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="64b22-122">Location of the resource</span></span>

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

### <span data-ttu-id="64b22-123">-이름</span><span class="sxs-lookup"><span data-stu-id="64b22-123">-Name</span></span>
<span data-ttu-id="64b22-124">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-124">Name of the plan.</span></span>

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

### <span data-ttu-id="64b22-125">-계획 정의</span><span class="sxs-lookup"><span data-stu-id="64b22-125">-PlanDefinition</span></span>
<span data-ttu-id="64b22-126">계획은 테 넌 트를 제공 하는 할당량 및 용량 패키지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="64b22-127">테 넌 트가 기본 클라우드 서비스에 대 한 액세스를 업그레이드 하는 제안을 통해이 요금제를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="64b22-128">생성 하려면 계획 정의 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="64b22-129">-속성 이름</span><span class="sxs-lookup"><span data-stu-id="64b22-129">-PropertiesName</span></span>
<span data-ttu-id="64b22-130">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-130">Name of the plan.</span></span>

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

### <span data-ttu-id="64b22-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="64b22-131">-QuotaIds</span></span>
<span data-ttu-id="64b22-132">계획 아래에 할당량 식별자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64b22-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b22-133">-ResourceGroupName</span></span>
<span data-ttu-id="64b22-134">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="64b22-135">-(\) Uid</span><span class="sxs-lookup"><span data-stu-id="64b22-135">-SkuIds</span></span>
<span data-ttu-id="64b22-136">SKU 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64b22-137">-구독 카운트</span><span class="sxs-lookup"><span data-stu-id="64b22-137">-SubscriptionCount</span></span>
<span data-ttu-id="64b22-138">구독 수입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="64b22-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64b22-139">-SubscriptionId</span></span>
<span data-ttu-id="64b22-140">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64b22-141">-확인</span><span class="sxs-lookup"><span data-stu-id="64b22-141">-Confirm</span></span>
<span data-ttu-id="64b22-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b22-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b22-143">-WhatIf</span></span>
<span data-ttu-id="64b22-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b22-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b22-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b22-146">CommonParameters</span></span>
<span data-ttu-id="64b22-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b22-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="64b22-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b22-149">입력</span><span class="sxs-lookup"><span data-stu-id="64b22-149">INPUTS</span></span>

### <span data-ttu-id="64b22-150">SubscriptionsAdmin Api20151101. i a PowerShell. IPlan</span><span class="sxs-lookup"><span data-stu-id="64b22-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="64b22-151">출력</span><span class="sxs-lookup"><span data-stu-id="64b22-151">OUTPUTS</span></span>

### <span data-ttu-id="64b22-152">SubscriptionsAdmin Api20151101. i a PowerShell. IPlan</span><span class="sxs-lookup"><span data-stu-id="64b22-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="64b22-153">별칭과</span><span class="sxs-lookup"><span data-stu-id="64b22-153">ALIASES</span></span>

## <span data-ttu-id="64b22-154">상속자</span><span class="sxs-lookup"><span data-stu-id="64b22-154">NOTES</span></span>

<span data-ttu-id="64b22-155">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64b22-156">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="64b22-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="64b22-157">계획 정의 <IPlan> : 요금제는 테 넌 트를 제공 하는 할당량 및 용량 패키지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="64b22-158">테 넌 트가 기본 클라우드 서비스에 대 한 액세스를 업그레이드 하는 제안을 통해이 요금제를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="64b22-159">`[Location <String>]`: 리소스 위치</span><span class="sxs-lookup"><span data-stu-id="64b22-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="64b22-160">`[Description <String>]`: 계획에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="64b22-161">`[DisplayName <String>]`: 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="64b22-162">`[ExternalReferenceId <String>]`: 외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="64b22-163">`[PropertiesName <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="64b22-164">`[QuotaIds <String[]>]`: 계획 아래에 할당량 식별자가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64b22-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="64b22-165">`[SkuIds <String[]>]`: SKU 식별자.</span><span class="sxs-lookup"><span data-stu-id="64b22-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="64b22-166">`[SubscriptionCount <Int32?>]`: 구독 수.</span><span class="sxs-lookup"><span data-stu-id="64b22-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="64b22-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64b22-167">RELATED LINKS</span></span>
