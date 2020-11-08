---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 8a54a0e909cd2fdfa31051c8b06f8f6414b310ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043213"
---
# <span data-ttu-id="e7387-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="e7387-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="e7387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7387-102">SYNOPSIS</span></span>
<span data-ttu-id="e7387-103">사용자는이 명령을 사용 하 여 VPN 게이트웨이에서 설정 되는 Ipsec ipsec 정책 개체를 만들어 (IkeEncryption Encryption, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등의 값을 하나 또는 모두 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="e7387-104">이 명령은 output 개체를 사용 하 여 새/기존 게이트웨이 모두에 대 한 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="e7387-105">구문과</span><span class="sxs-lookup"><span data-stu-id="e7387-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7387-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e7387-106">DESCRIPTION</span></span>
<span data-ttu-id="e7387-107">사용자는이 명령을 사용 하 여 VPN 게이트웨이에서 설정 되는 Ipsec ipsec 정책 개체를 만들어 (IkeEncryption Encryption, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등의 값을 하나 또는 모두 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="e7387-108">이 명령은 output 개체를 사용 하 여 새/기존 게이트웨이 모두에 대 한 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="e7387-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7387-109">EXAMPLES</span></span>

### <span data-ttu-id="e7387-110">Vpn ipsec 정책 개체 정의:</span><span class="sxs-lookup"><span data-stu-id="e7387-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="e7387-111">이 cmdlet은 전달 된 하나 또는 모든 매개 변수를 사용 하 여 vpn ipsec 정책 개체를 생성 하는 데 사용 됩니다. VpnClientIpsecPolicy 명령: p r o m a t:에 New-AzVirtualNetworkGateway (새 VPN 게이트웨이 만들기)/Set-AzVirtualNetworkGateway (기존 VPN 게이트웨이 업데이트) ResourceGroup의 리소스 수:</span><span class="sxs-lookup"><span data-stu-id="e7387-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="e7387-112">Vpn 사용자 지정 ipsec 정책 설정을 사용 하 여 새 가상 네트워크 게이트웨이 만들기:</span><span class="sxs-lookup"><span data-stu-id="e7387-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="e7387-113">이 cmdlet은 생성 후 가상 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="e7387-114">기존 가상 네트워크 게이트웨이에서 vpn 사용자 지정 ipsec 정책 설정:</span><span class="sxs-lookup"><span data-stu-id="e7387-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="e7387-115">이 cmdlet은 vpn 사용자 지정 ipsec 정책을 설정한 후 가상 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="e7387-116">Vpn 사용자 지정 정책이 올바르게 설정 되어 있는지 확인 하려면 가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="e7387-117">이 cmdlet은 가상 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="e7387-118">변수</span><span class="sxs-lookup"><span data-stu-id="e7387-118">PARAMETERS</span></span>

### <span data-ttu-id="e7387-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7387-119">-DefaultProfile</span></span>
<span data-ttu-id="e7387-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7387-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="e7387-121">-DhGroup</span></span>
<span data-ttu-id="e7387-122">초기 SA에 대 한 IKE 단계 1에 사용 되는 VpnClient DH 그룹</span><span class="sxs-lookup"><span data-stu-id="e7387-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="e7387-123">-IkeEncryption</span></span>
<span data-ttu-id="e7387-124">VpnClient IKE 암호화 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="e7387-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="e7387-125">-IkeIntegrity</span></span>
<span data-ttu-id="e7387-126">VpnClient IKE 무결성 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="e7387-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-127">-암호 암호화</span><span class="sxs-lookup"><span data-stu-id="e7387-127">-IpsecEncryption</span></span>
<span data-ttu-id="e7387-128">VpnClient IPSec 암호화 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="e7387-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-129">-계층 무결성</span><span class="sxs-lookup"><span data-stu-id="e7387-129">-IpsecIntegrity</span></span>
<span data-ttu-id="e7387-130">VpnClient IPSec 무결성 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="e7387-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="e7387-131">-PfsGroup</span></span>
<span data-ttu-id="e7387-132">새 자식 SA에 대 한 IKE 단계 2에 사용 되는 VpnClient PFS 그룹</span><span class="sxs-lookup"><span data-stu-id="e7387-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="e7387-133">-SADataSize</span></span>
<span data-ttu-id="e7387-134">VpnClient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 페이로드 크기 (KB)</span><span class="sxs-lookup"><span data-stu-id="e7387-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="e7387-135">-SALifeTime</span></span>
<span data-ttu-id="e7387-136">VpnClient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 수명이 초 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7387-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7387-137">CommonParameters</span></span>
<span data-ttu-id="e7387-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7387-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7387-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7387-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7387-140">입력</span><span class="sxs-lookup"><span data-stu-id="e7387-140">INPUTS</span></span>

### <span data-ttu-id="e7387-141">않아야</span><span class="sxs-lookup"><span data-stu-id="e7387-141">None</span></span>

## <span data-ttu-id="e7387-142">출력</span><span class="sxs-lookup"><span data-stu-id="e7387-142">OUTPUTS</span></span>

### <span data-ttu-id="e7387-143">PSIpsecPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e7387-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="e7387-144">상속자</span><span class="sxs-lookup"><span data-stu-id="e7387-144">NOTES</span></span>

## <span data-ttu-id="e7387-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7387-145">RELATED LINKS</span></span>