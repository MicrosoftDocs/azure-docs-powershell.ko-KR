---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878130"
---
# <span data-ttu-id="bc39f-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc39f-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="bc39f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc39f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc39f-103">Azure ExpressRoutePort를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="bc39f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc39f-104">SYNTAX</span></span>

### <span data-ttu-id="bc39f-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc39f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc39f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc39f-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc39f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bc39f-107">DESCRIPTION</span></span>
<span data-ttu-id="bc39f-108">**AzExpressRoutePort** Cmdlet은 Azure ExpressRoutePort를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="bc39f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bc39f-109">EXAMPLES</span></span>

### <span data-ttu-id="bc39f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc39f-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="bc39f-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="bc39f-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="bc39f-112">변수</span><span class="sxs-lookup"><span data-stu-id="bc39f-112">PARAMETERS</span></span>

### <span data-ttu-id="bc39f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc39f-113">-AsJob</span></span>
<span data-ttu-id="bc39f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="bc39f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc39f-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="bc39f-115">-BandwidthInGbps</span></span>
<span data-ttu-id="bc39f-116">Gbps의 확보 포트 대역폭</span><span class="sxs-lookup"><span data-stu-id="bc39f-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="bc39f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc39f-117">-DefaultProfile</span></span>
<span data-ttu-id="bc39f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc39f-119">-캡슐화</span><span class="sxs-lookup"><span data-stu-id="bc39f-119">-Encapsulation</span></span>
<span data-ttu-id="bc39f-120">실제 포트의 캡슐화 방법</span><span class="sxs-lookup"><span data-stu-id="bc39f-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="bc39f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bc39f-121">-Force</span></span>
<span data-ttu-id="bc39f-122">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="bc39f-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bc39f-123">-Id</span><span class="sxs-lookup"><span data-stu-id="bc39f-123">-Identity</span></span>
<span data-ttu-id="bc39f-124">사용자가 지정 하는 Id (MacSec 구성 읽기)</span><span class="sxs-lookup"><span data-stu-id="bc39f-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc39f-125">-링크</span><span class="sxs-lookup"><span data-stu-id="bc39f-125">-Link</span></span>
<span data-ttu-id="bc39f-126">ExpressRoutePort 리소스의 실제 링크 집합</span><span class="sxs-lookup"><span data-stu-id="bc39f-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc39f-127">-위치</span><span class="sxs-lookup"><span data-stu-id="bc39f-127">-Location</span></span>
<span data-ttu-id="bc39f-128">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-128">The location.</span></span>

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

### <span data-ttu-id="bc39f-129">-이름</span><span class="sxs-lookup"><span data-stu-id="bc39f-129">-Name</span></span>
<span data-ttu-id="bc39f-130">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-130">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc39f-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="bc39f-131">-PeeringLocation</span></span>
<span data-ttu-id="bc39f-132">ExpressRoutePort가 물리적으로 매핑된 피어 링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="bc39f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc39f-133">-ResourceGroupName</span></span>
<span data-ttu-id="bc39f-134">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-134">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc39f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc39f-135">-ResourceId</span></span>
<span data-ttu-id="bc39f-136">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-136">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc39f-137">태그</span><span class="sxs-lookup"><span data-stu-id="bc39f-137">-Tag</span></span>
<span data-ttu-id="bc39f-138">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc39f-139">-확인</span><span class="sxs-lookup"><span data-stu-id="bc39f-139">-Confirm</span></span>
<span data-ttu-id="bc39f-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc39f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc39f-141">-WhatIf</span></span>
<span data-ttu-id="bc39f-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc39f-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc39f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc39f-144">CommonParameters</span></span>
<span data-ttu-id="bc39f-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc39f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc39f-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc39f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc39f-147">입력</span><span class="sxs-lookup"><span data-stu-id="bc39f-147">INPUTS</span></span>

### <span data-ttu-id="bc39f-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc39f-148">System.String</span></span>

### <span data-ttu-id="bc39f-149">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="bc39f-149">System.Int32</span></span>

### <span data-ttu-id="bc39f-150">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="bc39f-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc39f-151">PSExpressRouteLink [] (으)로</span><span class="sxs-lookup"><span data-stu-id="bc39f-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="bc39f-152">출력</span><span class="sxs-lookup"><span data-stu-id="bc39f-152">OUTPUTS</span></span>

### <span data-ttu-id="bc39f-153">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="bc39f-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="bc39f-154">상속자</span><span class="sxs-lookup"><span data-stu-id="bc39f-154">NOTES</span></span>

## <span data-ttu-id="bc39f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc39f-155">RELATED LINKS</span></span>

[<span data-ttu-id="bc39f-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc39f-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="bc39f-157">제거-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc39f-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="bc39f-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="bc39f-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)