---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328222"
---
# <span data-ttu-id="b7344-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="b7344-101">New-AzHpcCache</span></span>

## <span data-ttu-id="b7344-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7344-102">SYNOPSIS</span></span>
<span data-ttu-id="b7344-103">HPC 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="b7344-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7344-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7344-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7344-105">DESCRIPTION</span></span>
<span data-ttu-id="b7344-106">**New-AzHpcCache** cmdlet은 Azure HPC 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="b7344-107">예제</span><span class="sxs-lookup"><span data-stu-id="b7344-107">EXAMPLES</span></span>

### <span data-ttu-id="b7344-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7344-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="b7344-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7344-109">PARAMETERS</span></span>

### <span data-ttu-id="b7344-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7344-110">-AsJob</span></span>
<span data-ttu-id="b7344-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b7344-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7344-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="b7344-112">-CacheSize</span></span>
<span data-ttu-id="b7344-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="b7344-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7344-114">-DefaultProfile</span></span>
<span data-ttu-id="b7344-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-116">-Location</span><span class="sxs-lookup"><span data-stu-id="b7344-116">-Location</span></span>
<span data-ttu-id="b7344-117">위치.</span><span class="sxs-lookup"><span data-stu-id="b7344-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b7344-118">-Name</span></span>
<span data-ttu-id="b7344-119">캐시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7344-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7344-121">캐시를 만들 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="b7344-122">-Sku</span></span>
<span data-ttu-id="b7344-123">SKU.</span><span class="sxs-lookup"><span data-stu-id="b7344-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="b7344-124">-SubnetUri</span></span>
<span data-ttu-id="b7344-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="b7344-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7344-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7344-126">-Tag</span></span>
<span data-ttu-id="b7344-127">HPC 캐시와 연결하기 위해 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="b7344-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7344-128">-Confirm</span></span>
<span data-ttu-id="b7344-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7344-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7344-130">-WhatIf</span></span>
<span data-ttu-id="b7344-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b7344-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7344-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7344-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7344-133">CommonParameters</span></span>
<span data-ttu-id="b7344-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7344-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7344-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7344-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7344-136">입력</span><span class="sxs-lookup"><span data-stu-id="b7344-136">INPUTS</span></span>

### <span data-ttu-id="b7344-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b7344-137">System.String</span></span>

### <span data-ttu-id="b7344-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b7344-138">System.Int32</span></span>

## <span data-ttu-id="b7344-139">출력</span><span class="sxs-lookup"><span data-stu-id="b7344-139">OUTPUTS</span></span>

### <span data-ttu-id="b7344-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="b7344-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="b7344-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7344-141">NOTES</span></span>

## <span data-ttu-id="b7344-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7344-142">RELATED LINKS</span></span>