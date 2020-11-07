---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 2e85cc87f0f0b1fb0451e3697f6ffef3b317124b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872357"
---
# <span data-ttu-id="fe3b2-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="fe3b2-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="fe3b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3b2-103">새 피어 링 서비스 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="fe3b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe3b2-104">SYNTAX</span></span>

### <span data-ttu-id="fe3b2-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fe3b2-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe3b2-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3b2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fe3b2-108">DESCRIPTION</span></span>
<span data-ttu-id="fe3b2-109">피어 링 서비스 개체와 연결 된 피어 링 서비스 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="fe3b2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fe3b2-110">EXAMPLES</span></span>

### <span data-ttu-id="fe3b2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fe3b2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="fe3b2-112">피어 링 서비스 개체에서 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="fe3b2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fe3b2-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="fe3b2-114">피어 링 서비스 리소스 id에서 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="fe3b2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="fe3b2-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="fe3b2-116">피어 링 서비스 리소스 그룹 이름 및 이름에서 접두사를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="fe3b2-117">변수</span><span class="sxs-lookup"><span data-stu-id="fe3b2-117">PARAMETERS</span></span>

### <span data-ttu-id="fe3b2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe3b2-118">-AsJob</span></span>
<span data-ttu-id="fe3b2-119">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-119">Run in the background.</span></span>

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

### <span data-ttu-id="fe3b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3b2-120">-DefaultProfile</span></span>
<span data-ttu-id="fe3b2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3b2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fe3b2-122">-Name</span></span>
<span data-ttu-id="fe3b2-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="fe3b2-124">-PeeringServiceId</span></span>
<span data-ttu-id="fe3b2-125">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-126">-PeeringServiceName</span></span>
<span data-ttu-id="fe3b2-127">피어 링 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-127">The peering service name.</span></span>
<span data-ttu-id="fe3b2-128">새 피어 링 서비스 또는 목록 Get-AzPeeringService에 대해 New-AzPeeringService cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="fe3b2-129">-PeeringServiceObject</span></span>
<span data-ttu-id="fe3b2-130">Get-AzPeeringService 사용</span><span class="sxs-lookup"><span data-stu-id="fe3b2-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-131">-접두사</span><span class="sxs-lookup"><span data-stu-id="fe3b2-131">-Prefix</span></span>
<span data-ttu-id="fe3b2-132">세션 IPv4 접두사</span><span class="sxs-lookup"><span data-stu-id="fe3b2-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="fe3b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="fe3b2-134">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-135">-확인</span><span class="sxs-lookup"><span data-stu-id="fe3b2-135">-Confirm</span></span>
<span data-ttu-id="fe3b2-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3b2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3b2-137">-WhatIf</span></span>
<span data-ttu-id="fe3b2-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3b2-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3b2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3b2-140">CommonParameters</span></span>
<span data-ttu-id="fe3b2-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3b2-142">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3b2-143">입력</span><span class="sxs-lookup"><span data-stu-id="fe3b2-143">INPUTS</span></span>

### <span data-ttu-id="fe3b2-144">PSPeeringService (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="fe3b2-145">출력</span><span class="sxs-lookup"><span data-stu-id="fe3b2-145">OUTPUTS</span></span>

### <span data-ttu-id="fe3b2-146">PSPeeringServicePrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe3b2-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="fe3b2-147">상속자</span><span class="sxs-lookup"><span data-stu-id="fe3b2-147">NOTES</span></span>

## <span data-ttu-id="fe3b2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe3b2-148">RELATED LINKS</span></span>