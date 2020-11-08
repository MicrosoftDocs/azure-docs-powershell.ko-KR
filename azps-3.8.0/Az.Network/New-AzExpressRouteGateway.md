---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteGateway.md
ms.openlocfilehash: 5fe97366784b3513515ee90ce70fe518c36a8585
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042070"
---
# <span data-ttu-id="b844a-101">New-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="b844a-101">New-AzExpressRouteGateway</span></span>

## <span data-ttu-id="b844a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b844a-102">SYNOPSIS</span></span>
<span data-ttu-id="b844a-103">확장 가능한 Express 가능 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-103">Creates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="b844a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b844a-104">SYNTAX</span></span>

### <span data-ttu-id="b844a-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b844a-105">ByVirtualHubName (Default)</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubName <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b844a-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b844a-106">ByVirtualHubObject</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHub <PSVirtualHub> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b844a-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b844a-107">ByVirtualHubResourceId</span></span>
```
New-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 [-MaxScaleUnits <UInt32>] -VirtualHubId <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b844a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b844a-108">DESCRIPTION</span></span>

<span data-ttu-id="b844a-109">New-AzExpressRouteGateway는 확장 가능 하는 Express 경로 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-109">New-AzExpressRouteGateway creates a scalable ExpressRoute Gateway.</span></span> <span data-ttu-id="b844a-110">이는 VirtualHub 내에서 온-프레미스에서 Azure로의 소프트웨어 정의 된 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-110">This is software defined connectivity for on premise to Azure inside the VirtualHub.</span></span> 

<span data-ttu-id="b844a-111">이 게이트웨이에는이 게이트웨이 또는 Set-AzExpressRouteGateway cmdlet에 지정 된 배율 단위를 기준으로 크기를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-111">This gateway can be scaled based on the scale unit specified in this or the Set-AzExpressRouteGateway cmdlet.</span></span> 

<span data-ttu-id="b844a-112">온-프레미스 Express 경로 회로에서 확장 가능한 게이트웨이로의 연결이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-112">A connection is set up from a on-premise ExpressRoute circuit to the scalable gateway.</span></span>

<span data-ttu-id="b844a-113">ExpressRouteGateway는 참조 되는 VirtualHub와 같은 위치에 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-113">The ExpressRouteGateway will be in the same location as the referenced VirtualHub.</span></span>

## <span data-ttu-id="b844a-114">예제의</span><span class="sxs-lookup"><span data-stu-id="b844a-114">EXAMPLES</span></span>

### <span data-ttu-id="b844a-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="b844a-115">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 2
VirtualHub          : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
BgpSettings         : {}
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="b844a-116">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="b844a-117">1 개의 배율 단위를 사용 하 여 가상 허브에서 Express 경로 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-117">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

## <span data-ttu-id="b844a-118">변수</span><span class="sxs-lookup"><span data-stu-id="b844a-118">PARAMETERS</span></span>

### <span data-ttu-id="b844a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b844a-119">-AsJob</span></span>
<span data-ttu-id="b844a-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b844a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b844a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b844a-121">-DefaultProfile</span></span>
<span data-ttu-id="b844a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b844a-123">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="b844a-123">-MaxScaleUnits</span></span>
<span data-ttu-id="b844a-124">이 ExpressRouteGateway의 최대 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-124">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="b844a-125">유효 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="b844a-125">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b844a-126">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="b844a-126">-MinScaleUnits</span></span>
<span data-ttu-id="b844a-127">이 ExpressRouteGateway의 최소 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-127">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="b844a-128">유효 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="b844a-128">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b844a-129">-이름</span><span class="sxs-lookup"><span data-stu-id="b844a-129">-Name</span></span>
<span data-ttu-id="b844a-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b844a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b844a-131">-ResourceGroupName</span></span>
<span data-ttu-id="b844a-132">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-132">The resource name.</span></span>

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

### <span data-ttu-id="b844a-133">태그</span><span class="sxs-lookup"><span data-stu-id="b844a-133">-Tag</span></span>
<span data-ttu-id="b844a-134">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b844a-135">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="b844a-135">-VirtualHub</span></span>
<span data-ttu-id="b844a-136">이 VpnGateway 연결 해야 하는 VirtualHub입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-136">The VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b844a-137">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="b844a-137">-VirtualHubId</span></span>
<span data-ttu-id="b844a-138">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-138">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b844a-139">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="b844a-139">-VirtualHubName</span></span>
<span data-ttu-id="b844a-140">이 VpnGateway와 연결 되어야 하는 VirtualHub의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-140">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b844a-141">-확인</span><span class="sxs-lookup"><span data-stu-id="b844a-141">-Confirm</span></span>
<span data-ttu-id="b844a-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b844a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b844a-143">-WhatIf</span></span>
<span data-ttu-id="b844a-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b844a-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b844a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b844a-146">CommonParameters</span></span>
<span data-ttu-id="b844a-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b844a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b844a-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b844a-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b844a-149">입력</span><span class="sxs-lookup"><span data-stu-id="b844a-149">INPUTS</span></span>

### <span data-ttu-id="b844a-150">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b844a-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="b844a-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b844a-151">System.String</span></span>

## <span data-ttu-id="b844a-152">출력</span><span class="sxs-lookup"><span data-stu-id="b844a-152">OUTPUTS</span></span>

### <span data-ttu-id="b844a-153">PSExpressRouteGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b844a-153">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="b844a-154">상속자</span><span class="sxs-lookup"><span data-stu-id="b844a-154">NOTES</span></span>

## <span data-ttu-id="b844a-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b844a-155">RELATED LINKS</span></span>