---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AE8E26F2-CF8E-4340-936D-230731B5BA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: c1c2f9fc3cbe528687f0a276c1b5feed3bbdb4b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211591"
---
# <span data-ttu-id="51ae5-101">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="51ae5-101">New-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="51ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="51ae5-103">응용 프로그램 게이트웨이에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-103">Creates a front-end IP configuration for an application gateway.</span></span>

## <span data-ttu-id="51ae5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51ae5-104">SYNTAX</span></span>

### <span data-ttu-id="51ae5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51ae5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-SubnetId <String>]
 [-PublicIPAddressId <String>] [-PrivateLinkConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ae5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="51ae5-106">SetByResource</span></span>
```
New-AzApplicationGatewayFrontendIPConfig -Name <String> [-PrivateIPAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIPAddress <PSPublicIpAddress>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ae5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51ae5-107">DESCRIPTION</span></span>
<span data-ttu-id="51ae5-108">**AzApplicationGatewayFrontendIPConfig** Cmdlet은 Azure application gateway에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-108">The **New-AzApplicationGatewayFrontendIPConfig** cmdlet creates a front-end IP configuration for an Azure application gateway.</span></span>
<span data-ttu-id="51ae5-109">Application gateway는 두 가지 유형의 프런트 엔드 IP 구성을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-109">An application gateway supports two types of front-end IP configuration:</span></span> 
- <span data-ttu-id="51ae5-110">공용 IP 주소--내부 부하 분산 (ILB)을 사용 하는 개인 IP 주소.</span><span class="sxs-lookup"><span data-stu-id="51ae5-110">Public IP addresses -- Private IP addresses using internal load balancing (ILB).</span></span>
 <span data-ttu-id="51ae5-111">응용 프로그램 게이트웨이에는 공용 IP 주소와 개인 IP 주소가 각각 하나씩 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-111">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="51ae5-112">공용 IP 주소와 개인 IP 주소는 프런트 엔드 IP 주소와 별도로 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-112">The public IP address and private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="51ae5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="51ae5-113">EXAMPLES</span></span>

### <span data-ttu-id="51ae5-114">예제 1: 공용 IP 리소스 개체를 사용 하 여 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="51ae5-114">Example 1: Create a front-end IP configuration using a public IP resource object</span></span>
```
PS C:\>$PublicIP = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIP01" -location "West US" -AllocationMethod Dynamic
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -PublicIPAddress $PublicIP
```

<span data-ttu-id="51ae5-115">첫 번째 명령은 공용 IP 리소스 개체를 만들어 $PublicIP 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-115">The first command creates a public IP resource object and stores it in the $PublicIP variable.</span></span>
<span data-ttu-id="51ae5-116">두 번째 명령은 $PublicIP를 사용 하 여 FrontEndIP01 이라는 새 프런트 엔드 IP 구성을 만들고이를 $FrontEnd 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-116">The second command uses $PublicIP to create a new front-end IP configuration named FrontEndIP01 and stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="51ae5-117">예제 2: 프런트 엔드 IP 주소로 정적 개인 IP 만들기</span><span class="sxs-lookup"><span data-stu-id="51ae5-117">Example 2: Create a static private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="51ae5-118">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-118">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="51ae5-119">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-119">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="51ae5-120">셋째 명령은 두 번째 명령과 개인 IP 주소 10.0.1.1에서 $Subnet를 사용 하 여 FrontEndIP02 라는 프런트 엔드 IP 구성을 만든 다음 $FrontEnd 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-120">The third command creates a front-end IP configuration named FrontEndIP02 using $Subnet from the second command and the private IP address 10.0.1.1, and then stores it in the $FrontEnd variable.</span></span>

### <span data-ttu-id="51ae5-121">예제 3: 프런트 엔드 IP 주소로 동적 개인 IP 만들기</span><span class="sxs-lookup"><span data-stu-id="51ae5-121">Example 3: Create a dynamic private IP as the front-end IP address</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $FrontEnd = New-AzApplicationGatewayFrontendIPConfig -Name "FrontendIP03" -Subnet $Subnet
```

<span data-ttu-id="51ae5-122">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-122">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>
<span data-ttu-id="51ae5-123">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-123">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="51ae5-124">셋째 명령은 두 번째 명령의 $Subnet를 사용 하 여 FrontEndIP03 라는 프런트 엔드 IP 구성을 만들어 $FrontEnd 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-124">The third command creates a front-end IP configuration named FrontEndIP03 using $Subnet from the second command, and stores it in the $FrontEnd variable.</span></span>

## <span data-ttu-id="51ae5-125">변수</span><span class="sxs-lookup"><span data-stu-id="51ae5-125">PARAMETERS</span></span>

### <span data-ttu-id="51ae5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ae5-126">-DefaultProfile</span></span>
<span data-ttu-id="51ae5-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-128">-이름</span><span class="sxs-lookup"><span data-stu-id="51ae5-128">-Name</span></span>
<span data-ttu-id="51ae5-129">이 cmdlet이 만드는 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-129">Specifies the name of the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="51ae5-130">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="51ae5-130">-PrivateIPAddress</span></span>
<span data-ttu-id="51ae5-131">이 cmdlet이 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소와 연결 하는 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-131">Specifies the private IP address which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="51ae5-132">이는 서브넷이 지정 된 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-132">This can be specified only if a subnet is specified.</span></span>
<span data-ttu-id="51ae5-133">이 IP는 서브넷에서 정적으로 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-133">This IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="51ae5-134">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="51ae5-134">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="51ae5-135">PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="51ae5-135">PrivateLinkConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-136">-PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="51ae5-136">-PrivateLinkConfigurationId</span></span>
<span data-ttu-id="51ae5-137">PrivateLinkConfigurationId</span><span class="sxs-lookup"><span data-stu-id="51ae5-137">PrivateLinkConfigurationId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-138">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="51ae5-138">-PublicIPAddress</span></span>
<span data-ttu-id="51ae5-139">이 cmdlet이 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소와 연결 하는 공용 IP 주소 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-139">Specifies the public IP address object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-140">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="51ae5-140">-PublicIPAddressId</span></span>
<span data-ttu-id="51ae5-141">이 cmdlet이 응용 프로그램 게이트웨이의 프런트 엔드 IP와 연결 하는 공용 IP 주소 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-141">Specifies the public IP address ID which this cmdlet associates with the front-end IP of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-142">-서브넷</span><span class="sxs-lookup"><span data-stu-id="51ae5-142">-Subnet</span></span>
<span data-ttu-id="51ae5-143">이 cmdlet이 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소와 연결 하는 서브넷 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-143">Specifies the subnet object which this cmdlet associates with the front-end IP address of the application gateway.</span></span>
<span data-ttu-id="51ae5-144">이 매개 변수를 지정 하는 경우 게이트웨이에서 개인 IP 주소를 사용 한다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-144">If you specify this parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="51ae5-145">*PrivateIPAddress* 매개 변수를 지정한 경우이 매개 변수에서 지정한 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-145">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by this parameter.</span></span>
<span data-ttu-id="51ae5-146">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-146">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="51ae5-147">-SubnetId</span></span>
<span data-ttu-id="51ae5-148">이 cmdlet이 응용 프로그램 게이트웨이의 프런트 엔드 IP 구성과 연결 하는 서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-148">Specifies the subnet ID which this cmdlet associates with the front-end IP configuration of the application gateway.</span></span>
<span data-ttu-id="51ae5-149">*서브넷* 매개 변수를 지정 하는 경우 게이트웨이에서 개인 IP 주소를 사용 한다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-149">If you specify the *Subnet* parameter, it implies that the gateway uses a private IP address.</span></span>
<span data-ttu-id="51ae5-150">*PrivateIPAddress* 매개 변수를 지정한 경우 *서브넷* 으로 지정 된 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-150">If the *PrivateIPAddress* parameter is specified, it should belong to the subnet specified by *Subnet*.</span></span>
<span data-ttu-id="51ae5-151">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-151">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ae5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ae5-152">CommonParameters</span></span>
<span data-ttu-id="51ae5-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51ae5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ae5-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="51ae5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ae5-155">입력</span><span class="sxs-lookup"><span data-stu-id="51ae5-155">INPUTS</span></span>

### <span data-ttu-id="51ae5-156">않아야</span><span class="sxs-lookup"><span data-stu-id="51ae5-156">None</span></span>

## <span data-ttu-id="51ae5-157">출력</span><span class="sxs-lookup"><span data-stu-id="51ae5-157">OUTPUTS</span></span>

### <span data-ttu-id="51ae5-158">PSApplicationGatewayFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="51ae5-158">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="51ae5-159">상속자</span><span class="sxs-lookup"><span data-stu-id="51ae5-159">NOTES</span></span>

## <span data-ttu-id="51ae5-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51ae5-160">RELATED LINKS</span></span>

[<span data-ttu-id="51ae5-161">추가-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="51ae5-161">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="51ae5-162">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="51ae5-162">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="51ae5-163">제거-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="51ae5-163">Remove-AzApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="51ae5-164">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="51ae5-164">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)

