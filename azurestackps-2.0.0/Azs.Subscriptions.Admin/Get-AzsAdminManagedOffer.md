---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/22/2020
ms.locfileid: "94045141"
---
# <span data-ttu-id="433dd-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="433dd-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="433dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433dd-102">SYNOPSIS</span></span>
<span data-ttu-id="433dd-103">지정 된 행사를 받으세요.</span><span class="sxs-lookup"><span data-stu-id="433dd-103">Get the specified offer.</span></span>

## <span data-ttu-id="433dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="433dd-104">SYNTAX</span></span>

### <span data-ttu-id="433dd-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="433dd-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="433dd-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="433dd-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="433dd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="433dd-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="433dd-108">List1</span><span class="sxs-lookup"><span data-stu-id="433dd-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="433dd-109">설명은</span><span class="sxs-lookup"><span data-stu-id="433dd-109">DESCRIPTION</span></span>
<span data-ttu-id="433dd-110">지정 된 행사를 받으세요.</span><span class="sxs-lookup"><span data-stu-id="433dd-110">Get the specified offer.</span></span>

## <span data-ttu-id="433dd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="433dd-111">EXAMPLES</span></span>

### <span data-ttu-id="433dd-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="433dd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="433dd-113">이름 및 ResourceGroupName를 통해 제안 받기</span><span class="sxs-lookup"><span data-stu-id="433dd-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="433dd-114">변수</span><span class="sxs-lookup"><span data-stu-id="433dd-114">PARAMETERS</span></span>

### <span data-ttu-id="433dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433dd-115">-DefaultProfile</span></span>
<span data-ttu-id="433dd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433dd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="433dd-117">-InputObject</span></span>
<span data-ttu-id="433dd-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="433dd-119">-이름</span><span class="sxs-lookup"><span data-stu-id="433dd-119">-Name</span></span>
<span data-ttu-id="433dd-120">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-120">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="433dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="433dd-122">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="433dd-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="433dd-123">-SubscriptionId</span></span>
<span data-ttu-id="433dd-124">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="433dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433dd-125">CommonParameters</span></span>
<span data-ttu-id="433dd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433dd-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="433dd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433dd-128">입력</span><span class="sxs-lookup"><span data-stu-id="433dd-128">INPUTS</span></span>

### <span data-ttu-id="433dd-129">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="433dd-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="433dd-130">출력</span><span class="sxs-lookup"><span data-stu-id="433dd-130">OUTPUTS</span></span>

### <span data-ttu-id="433dd-131">SubscriptionsAdmin. Api20151101. i a i.</span><span class="sxs-lookup"><span data-stu-id="433dd-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="433dd-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="433dd-132">ALIASES</span></span>

<span data-ttu-id="433dd-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="433dd-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="433dd-134">상속자</span><span class="sxs-lookup"><span data-stu-id="433dd-134">NOTES</span></span>

<span data-ttu-id="433dd-135">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="433dd-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="433dd-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="433dd-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="433dd-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="433dd-138">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="433dd-139">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="433dd-140">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="433dd-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="433dd-141">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="433dd-142">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="433dd-143">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="433dd-144">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="433dd-145">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="433dd-146">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="433dd-147">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="433dd-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="433dd-148">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="433dd-149">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="433dd-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="433dd-151">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="433dd-152">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="433dd-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="433dd-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="433dd-153">RELATED LINKS</span></span>
