---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364253"
---
# <span data-ttu-id="f1783-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="f1783-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="f1783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1783-102">SYNOPSIS</span></span>
<span data-ttu-id="f1783-103">지역별로 구독에 대한 할당량 반환</span><span class="sxs-lookup"><span data-stu-id="f1783-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="f1783-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1783-104">SYNTAX</span></span>

### <span data-ttu-id="f1783-105">확인(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1783-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f1783-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1783-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1783-107">설명</span><span class="sxs-lookup"><span data-stu-id="f1783-107">DESCRIPTION</span></span>
<span data-ttu-id="f1783-108">지역별로 구독에 대한 할당량 반환</span><span class="sxs-lookup"><span data-stu-id="f1783-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="f1783-109">예제</span><span class="sxs-lookup"><span data-stu-id="f1783-109">EXAMPLES</span></span>

### <span data-ttu-id="f1783-110">예제 1: 할당량 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="f1783-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="f1783-111">할당량 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="f1783-111">Check quota availability</span></span>

## <span data-ttu-id="f1783-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1783-112">PARAMETERS</span></span>

### <span data-ttu-id="f1783-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1783-113">-DefaultProfile</span></span>
<span data-ttu-id="f1783-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1783-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1783-115">-InputObject</span></span>
<span data-ttu-id="f1783-116">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f1783-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1783-117">-Location</span><span class="sxs-lookup"><span data-stu-id="f1783-117">-Location</span></span>
<span data-ttu-id="f1783-118">Azure 지역</span><span class="sxs-lookup"><span data-stu-id="f1783-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1783-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1783-119">-SubscriptionId</span></span>
<span data-ttu-id="f1783-120">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1783-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1783-121">-Confirm</span></span>
<span data-ttu-id="f1783-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1783-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1783-123">-WhatIf</span></span>
<span data-ttu-id="f1783-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f1783-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1783-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1783-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1783-126">CommonParameters</span></span>
<span data-ttu-id="f1783-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1783-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f1783-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1783-129">입력</span><span class="sxs-lookup"><span data-stu-id="f1783-129">INPUTS</span></span>

### <span data-ttu-id="f1783-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="f1783-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="f1783-131">출력</span><span class="sxs-lookup"><span data-stu-id="f1783-131">OUTPUTS</span></span>

### <span data-ttu-id="f1783-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="f1783-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="f1783-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1783-133">NOTES</span></span>

<span data-ttu-id="f1783-134">별칭</span><span class="sxs-lookup"><span data-stu-id="f1783-134">ALIASES</span></span>

<span data-ttu-id="f1783-135">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f1783-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1783-136">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1783-137">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f1783-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1783-138">INPUTOBJECT: <IVMWareIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1783-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1783-139">`[AuthorizationName <String>]`: 사설 클라우드에서 ExpressRoute 회로 권한 부여의 이름</span><span class="sxs-lookup"><span data-stu-id="f1783-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="f1783-140">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="f1783-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="f1783-141">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="f1783-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="f1783-142">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f1783-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1783-143">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="f1783-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="f1783-144">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="f1783-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="f1783-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f1783-146">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="f1783-147">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1783-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="f1783-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1783-148">RELATED LINKS</span></span>
