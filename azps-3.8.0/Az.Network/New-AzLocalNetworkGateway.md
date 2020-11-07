---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: f355d011bbd810fa309cd8b7d64ed95090a00ea6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877462"
---
# <span data-ttu-id="3c96f-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c96f-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="3c96f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c96f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c96f-103">로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="3c96f-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="3c96f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c96f-104">SYNTAX</span></span>

### <span data-ttu-id="3c96f-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="3c96f-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c96f-106">Bylocalnetwork네트워크 Fqdn</span><span class="sxs-lookup"><span data-stu-id="3c96f-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c96f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3c96f-107">DESCRIPTION</span></span>
<span data-ttu-id="3c96f-108">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="3c96f-109">**AzLocalNetworkGateway** cmdlet은 게이트웨이의 이름, 리소스 그룹 이름, 위치, IP 주소, 그리고 Azure에 연결 되는 온-프레미스 네트워크의 주소 접두사에 따라 프레미스 게이트웨이를 나타내는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="3c96f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3c96f-110">EXAMPLES</span></span>

### <span data-ttu-id="3c96f-111">1: 로컬 네트워크 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="3c96f-111">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="3c96f-112">"서쪽 US"의 리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 만들고 IP 주소 "23.99.221.164" 및 주소 접두사 "10.5.51.0/24" 온-프레미스를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="3c96f-113">변수</span><span class="sxs-lookup"><span data-stu-id="3c96f-113">PARAMETERS</span></span>

### <span data-ttu-id="3c96f-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3c96f-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c96f-115">-AsJob</span></span>
<span data-ttu-id="3c96f-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3c96f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c96f-117">-Asn</span><span class="sxs-lookup"><span data-stu-id="3c96f-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="3c96f-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c96f-119">-DefaultProfile</span></span>
<span data-ttu-id="3c96f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c96f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3c96f-121">-Force</span></span>
<span data-ttu-id="3c96f-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c96f-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="3c96f-123">-Fqdn</span></span>
<span data-ttu-id="3c96f-124">로컬 네트워크 게이트웨이의 FQDN입니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-125">-게이트웨이 Ipaddress</span><span class="sxs-lookup"><span data-stu-id="3c96f-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-126">-위치</span><span class="sxs-lookup"><span data-stu-id="3c96f-126">-Location</span></span>
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

### <span data-ttu-id="3c96f-127">-이름</span><span class="sxs-lookup"><span data-stu-id="3c96f-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="3c96f-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c96f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c96f-130">로컬 네트워크 게이트웨이가 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="3c96f-131">태그</span><span class="sxs-lookup"><span data-stu-id="3c96f-131">-Tag</span></span>
<span data-ttu-id="3c96f-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3c96f-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3c96f-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3c96f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="3c96f-134">-Confirm</span></span>
<span data-ttu-id="3c96f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c96f-136">-WhatIf</span></span>
<span data-ttu-id="3c96f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c96f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c96f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c96f-139">CommonParameters</span></span>
<span data-ttu-id="3c96f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c96f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c96f-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3c96f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c96f-142">입력</span><span class="sxs-lookup"><span data-stu-id="3c96f-142">INPUTS</span></span>

### <span data-ttu-id="3c96f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c96f-143">System.String</span></span>

### <span data-ttu-id="3c96f-144">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="3c96f-144">System.String[]</span></span>

### <span data-ttu-id="3c96f-145">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="3c96f-145">System.UInt32</span></span>

### <span data-ttu-id="3c96f-146">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="3c96f-146">System.Int32</span></span>

### <span data-ttu-id="3c96f-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="3c96f-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3c96f-148">출력</span><span class="sxs-lookup"><span data-stu-id="3c96f-148">OUTPUTS</span></span>

### <span data-ttu-id="3c96f-149">Microsoft. 네트워크. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c96f-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="3c96f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="3c96f-150">NOTES</span></span>

## <span data-ttu-id="3c96f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c96f-151">RELATED LINKS</span></span>

[<span data-ttu-id="3c96f-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c96f-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="3c96f-153">제거-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c96f-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="3c96f-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3c96f-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)