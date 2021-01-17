---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340857"
---
# <span data-ttu-id="709b6-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="709b6-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="709b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="709b6-102">SYNOPSIS</span></span>
<span data-ttu-id="709b6-103">함수 앱 서비스 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="709b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="709b6-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="709b6-105">설명</span><span class="sxs-lookup"><span data-stu-id="709b6-105">DESCRIPTION</span></span>
<span data-ttu-id="709b6-106">함수 앱 서비스 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="709b6-107">예제</span><span class="sxs-lookup"><span data-stu-id="709b6-107">EXAMPLES</span></span>

### <span data-ttu-id="709b6-108">예제 1: 최대 10개 인스턴스의 버스트 기능을 사용하여 유럽 서부에서 Windows 프리미엄 앱 계획을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="709b6-109">이 명령은 최대 10개 인스턴스의 버스트 기능을 사용하여 유럽 서부에 Windows 프리미엄 앱 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="709b6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="709b6-110">PARAMETERS</span></span>

### <span data-ttu-id="709b6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="709b6-111">-AsJob</span></span>
<span data-ttu-id="709b6-112">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-112">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="709b6-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="709b6-114">-Location</span><span class="sxs-lookup"><span data-stu-id="709b6-114">-Location</span></span>
<span data-ttu-id="709b6-115">소비 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="709b6-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="709b6-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="709b6-117">App Service 계획에 대한 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709b6-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="709b6-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="709b6-119">App Service 계획에 대한 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709b6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="709b6-120">-Name</span></span>
<span data-ttu-id="709b6-121">App Service 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="709b6-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="709b6-122">-NoWait</span></span>
<span data-ttu-id="709b6-123">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="709b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="709b6-125">리소스가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="709b6-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="709b6-126">-Sku</span></span>
<span data-ttu-id="709b6-127">계획 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-127">The plan sku.</span></span>
<span data-ttu-id="709b6-128">유효한 입력은 EP1, EP2, EP3입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="709b6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="709b6-129">-SubscriptionId</span></span>
<span data-ttu-id="709b6-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="709b6-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="709b6-131">-Tag</span></span>
<span data-ttu-id="709b6-132">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="709b6-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="709b6-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="709b6-133">-WorkerType</span></span>
<span data-ttu-id="709b6-134">계획의 작업자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-134">The worker type for the plan.</span></span>
<span data-ttu-id="709b6-135">유효한 입력은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="709b6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="709b6-136">-Confirm</span></span>
<span data-ttu-id="709b6-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="709b6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="709b6-138">-WhatIf</span></span>
<span data-ttu-id="709b6-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="709b6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="709b6-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="709b6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="709b6-141">CommonParameters</span></span>
<span data-ttu-id="709b6-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="709b6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="709b6-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="709b6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="709b6-144">입력</span><span class="sxs-lookup"><span data-stu-id="709b6-144">INPUTS</span></span>

## <span data-ttu-id="709b6-145">출력</span><span class="sxs-lookup"><span data-stu-id="709b6-145">OUTPUTS</span></span>

### <span data-ttu-id="709b6-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="709b6-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="709b6-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="709b6-147">NOTES</span></span>

<span data-ttu-id="709b6-148">별칭</span><span class="sxs-lookup"><span data-stu-id="709b6-148">ALIASES</span></span>

## <span data-ttu-id="709b6-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="709b6-149">RELATED LINKS</span></span>
