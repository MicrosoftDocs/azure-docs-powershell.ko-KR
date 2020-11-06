---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: aef46264bc13b7136f9f999b2a97b3dd0951fbe8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530467"
---
# <span data-ttu-id="8b13d-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8b13d-101">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="8b13d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b13d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b13d-103">Express 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-103">Adds a peering configuration to an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b13d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b13d-104">SYNTAX</span></span>

### <span data-ttu-id="8b13d-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b13d-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b13d-106">MicrosoftPeeringConfigRoutFilterId</span><span class="sxs-lookup"><span data-stu-id="8b13d-106">MicrosoftPeeringConfigRoutFilterId</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>] -RouteFilterId <String>
 [-PeerAddressType <String>] [-LegacyMode <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b13d-107">MicrosoftPeeringConfigRoutFilter</span><span class="sxs-lookup"><span data-stu-id="8b13d-107">MicrosoftPeeringConfigRoutFilter</span></span>
```
Add-AzureRmExpressRouteCircuitPeeringConfig -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 -PeeringType <String> -PeerASN <UInt32> -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String>
 -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefixes <System.Collections.Generic.List`1[System.String]>]
 [-MicrosoftConfigCustomerAsn <Int32>] [-MicrosoftConfigRoutingRegistryName <String>]
 -RouteFilter <PSRouteFilter> [-PeerAddressType <String>] [-LegacyMode <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b13d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8b13d-108">DESCRIPTION</span></span>
<span data-ttu-id="8b13d-109">**AzureRmExpressRouteCircuitPeeringConfig** cmdlet은 대상 경로 회로에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-109">The **Add-AzureRmExpressRouteCircuitPeeringConfig** cmdlet adds a peering configuration to an ExpressRoute circuit.</span></span> <span data-ttu-id="8b13d-110">Express 경로 회로는 공용 인터넷 대신 연결 공급자를 사용 하 여 온-프레미스 네트워크를 Microsoft 클라우드에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-110">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="8b13d-111">**Add-AzureRmExpressRouteCircuitPeeringConfig** 을 실행 한 후에는 Set-AzureRmExpressRouteCircuit cmdlet을 호출 하 여 구성을 활성화 해야 한다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b13d-111">Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="8b13d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8b13d-112">EXAMPLES</span></span>

### <span data-ttu-id="8b13d-113">예제 1: 기존 Express 대상 회로에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="8b13d-113">Example 1: Add a peer to an existing ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    Circuit = $circuit
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzureRmExpressRouteCircuitPeeringConfig @parameters
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="8b13d-114">변수</span><span class="sxs-lookup"><span data-stu-id="8b13d-114">PARAMETERS</span></span>

### <span data-ttu-id="8b13d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b13d-115">-DefaultProfile</span></span>
<span data-ttu-id="8b13d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-117">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8b13d-117">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8b13d-118">수정 되는 Express 경로 회로입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-118">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="8b13d-119">**AzureRmExpressRouteCircuit** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-119">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-120">-LegacyMode</span><span class="sxs-lookup"><span data-stu-id="8b13d-120">-LegacyMode</span></span>
<span data-ttu-id="8b13d-121">피어 링의 레거시 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-121">The legacy mode of the Peering</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-122">-MicrosoftConfigAdvertisedPublicPrefixes</span><span class="sxs-lookup"><span data-stu-id="8b13d-122">-MicrosoftConfigAdvertisedPublicPrefixes</span></span>
<span data-ttu-id="8b13d-123">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-123">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="8b13d-124">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-124">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="8b13d-125">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-125">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="8b13d-126">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-126">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-127">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="8b13d-127">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="8b13d-128">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-128">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-129">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="8b13d-129">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="8b13d-130">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-130">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-131">-이름</span><span class="sxs-lookup"><span data-stu-id="8b13d-131">-Name</span></span>
<span data-ttu-id="8b13d-132">추가할 피어 링 관계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-132">The name of the peering relationship to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-133">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8b13d-133">-PeerAddressType</span></span>
<span data-ttu-id="8b13d-134">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="8b13d-134">PeerAddressType</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-135">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="8b13d-135">-PeerASN</span></span>
<span data-ttu-id="8b13d-136">Express 경로 회로의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-136">The AS number of your ExpressRoute circuit.</span></span> <span data-ttu-id="8b13d-137">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-137">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-138">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8b13d-138">-PeeringType</span></span>
<span data-ttu-id="8b13d-139">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8b13d-139">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-140">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b13d-140">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="8b13d-141">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-141">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="8b13d-142">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-142">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8b13d-143">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-143">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8b13d-144">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-144">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-145">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8b13d-145">-RouteFilter</span></span>
<span data-ttu-id="8b13d-146">기존 RouteFilter 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-146">This is an existing RouteFilter object.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: MicrosoftPeeringConfigRoutFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-147">-RouteFilterId</span><span class="sxs-lookup"><span data-stu-id="8b13d-147">-RouteFilterId</span></span>
<span data-ttu-id="8b13d-148">기존 RouteFilter 개체의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-148">This is the resource Id of an existing RouteFilter object.</span></span>

```yaml
Type: String
Parameter Sets: MicrosoftPeeringConfigRoutFilterId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-149">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8b13d-149">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="8b13d-150">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-150">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="8b13d-151">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-151">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="8b13d-152">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-152">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="8b13d-153">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-153">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-154">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="8b13d-154">-SharedKey</span></span>
<span data-ttu-id="8b13d-155">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-155">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-156">-VlanId</span><span class="sxs-lookup"><span data-stu-id="8b13d-156">-VlanId</span></span>
<span data-ttu-id="8b13d-157">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-157">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b13d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b13d-158">CommonParameters</span></span>
<span data-ttu-id="8b13d-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b13d-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b13d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b13d-161">입력</span><span class="sxs-lookup"><span data-stu-id="8b13d-161">INPUTS</span></span>

### <span data-ttu-id="8b13d-162">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8b13d-162">PSExpressRouteCircuit</span></span>
<span data-ttu-id="8b13d-163">' ExpressRouteCircuit ' 매개 변수는 파이프라인에서 ' PSExpressRouteCircuit ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b13d-163">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="8b13d-164">출력</span><span class="sxs-lookup"><span data-stu-id="8b13d-164">OUTPUTS</span></span>

### <span data-ttu-id="8b13d-165">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8b13d-165">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8b13d-166">상속자</span><span class="sxs-lookup"><span data-stu-id="8b13d-166">NOTES</span></span>

## <span data-ttu-id="8b13d-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b13d-167">RELATED LINKS</span></span>

[<span data-ttu-id="8b13d-168">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8b13d-168">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8b13d-169">새로운 AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8b13d-169">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8b13d-170">제거-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8b13d-170">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8b13d-171">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8b13d-171">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)