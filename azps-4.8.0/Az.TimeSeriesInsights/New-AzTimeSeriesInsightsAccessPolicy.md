---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213444"
---
# <span data-ttu-id="f263d-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f263d-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="f263d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f263d-102">SYNOPSIS</span></span>
<span data-ttu-id="f263d-103">지정 된 환경에서 액세스 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="f263d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f263d-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f263d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f263d-105">DESCRIPTION</span></span>
<span data-ttu-id="f263d-106">지정 된 환경에서 액세스 정책을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="f263d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f263d-107">EXAMPLES</span></span>

### <span data-ttu-id="f263d-108">예제 1: 지정 된 환경에 대 한 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="f263d-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="f263d-109">이 명령은 지정 된 환경에 대 한 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="f263d-110">변수</span><span class="sxs-lookup"><span data-stu-id="f263d-110">PARAMETERS</span></span>

### <span data-ttu-id="f263d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f263d-111">-DefaultProfile</span></span>
<span data-ttu-id="f263d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f263d-113">-설명</span><span class="sxs-lookup"><span data-stu-id="f263d-113">-Description</span></span>
<span data-ttu-id="f263d-114">액세스 정책에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-114">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f263d-115">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="f263d-115">-EnvironmentName</span></span>
<span data-ttu-id="f263d-116">지정 된 리소스 그룹과 연결 된 시계열 Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="f263d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f263d-117">-Name</span></span>
<span data-ttu-id="f263d-118">액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f263d-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="f263d-119">-PrincipalObjectId</span></span>
<span data-ttu-id="f263d-120">Azure Active Directory의 사용자에 대 한 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-120">The objectId of the principal in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f263d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f263d-121">-ResourceGroupName</span></span>
<span data-ttu-id="f263d-122">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f263d-123">-역할</span><span class="sxs-lookup"><span data-stu-id="f263d-123">-Role</span></span>
<span data-ttu-id="f263d-124">환경에서 주체가 할당 되는 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f263d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f263d-125">-SubscriptionId</span></span>
<span data-ttu-id="f263d-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f263d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f263d-127">-Confirm</span></span>
<span data-ttu-id="f263d-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f263d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f263d-129">-WhatIf</span></span>
<span data-ttu-id="f263d-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f263d-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f263d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f263d-132">CommonParameters</span></span>
<span data-ttu-id="f263d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f263d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f263d-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f263d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f263d-135">입력</span><span class="sxs-lookup"><span data-stu-id="f263d-135">INPUTS</span></span>

## <span data-ttu-id="f263d-136">출력</span><span class="sxs-lookup"><span data-stu-id="f263d-136">OUTPUTS</span></span>

### <span data-ttu-id="f263d-137">Api20200515. IAccessPolicyResource에 대 한 정보를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="f263d-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="f263d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f263d-138">NOTES</span></span>

<span data-ttu-id="f263d-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="f263d-139">ALIASES</span></span>

## <span data-ttu-id="f263d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f263d-140">RELATED LINKS</span></span>
