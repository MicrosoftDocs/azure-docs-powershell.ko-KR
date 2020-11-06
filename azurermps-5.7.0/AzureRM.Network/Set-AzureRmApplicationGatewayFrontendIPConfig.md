---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C024C32-1B03-4BAA-AD31-4974D414C998
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 38a74e6f11516b3a873709dfec118ffd2a1ad6ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535940"
---
# <span data-ttu-id="1b231-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b231-101">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="1b231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b231-102">SYNOPSIS</span></span>
<span data-ttu-id="1b231-103">프런트 엔드 IP 주소 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-103">Modifies a front-end IP address configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b231-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1b231-104">SYNTAX</span></span>

### <span data-ttu-id="1b231-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b231-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-SubnetId <String>] [-PublicIPAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b231-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1b231-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-PrivateIPAddress <String>] [-Subnet <PSSubnet>] [-PublicIPAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b231-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1b231-107">DESCRIPTION</span></span>
<span data-ttu-id="1b231-108">**Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet은 프런트 엔드 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-108">The **Set-AzureRmApplicationGatewayFrontendIPConfig** cmdlet updates a front-end IP configuration.</span></span>

<span data-ttu-id="1b231-109">응용 프로그램 게이트웨이는 프런트 엔드 IP 주소를 두 가지 유형으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-109">An application gateway supports two types of front-end IP addresses:</span></span> 

- <span data-ttu-id="1b231-110">공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="1b231-110">Public IP addresses</span></span>
- <span data-ttu-id="1b231-111">구성이 내부 부하 분산을 사용 하는 개인 IP 주소 (ILB)</span><span class="sxs-lookup"><span data-stu-id="1b231-111">Private IP addresses for which the configuration uses Internal Load Balancing (ILB)</span></span>

<span data-ttu-id="1b231-112">응용 프로그램 게이트웨이에는 공용 IP 주소와 개인 IP 주소가 각각 하나씩 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-112">An application gateway can have at most one public IP address and one private IP address.</span></span>
<span data-ttu-id="1b231-113">공용 IP 주소와 개인 IP 주소는 프런트 엔드 IP 주소와 별도로 추가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-113">A public IP address and a private IP address should be added separately as front-end IP addresses.</span></span>

## <span data-ttu-id="1b231-114">예제의</span><span class="sxs-lookup"><span data-stu-id="1b231-114">EXAMPLES</span></span>

### <span data-ttu-id="1b231-115">예제 1: 공용 IP를 응용 프로그램 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="1b231-115">Example 1: Set a public IP as front-end IP of an application gateway</span></span>
```
PS C:\>$PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIp01" -location "West US" -AllocationMethod Dynamic
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIp01" -PublicIPAddress $PublicIp
```

<span data-ttu-id="1b231-116">첫 번째 명령은 공용 IP 주소 개체를 만들고이를 $PublicIp 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-116">The first command creates a public IP address object and stores it in the $PublicIp variable.</span></span>

<span data-ttu-id="1b231-117">두 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-117">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1b231-118">세 번째 명령은 $PublicIp에 저장 된 주소를 사용 하 여 $AppGw의 게이트웨이에 대 한 FrontEndIp01 라는 프런트 엔드 IP 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-118">The third command updates the front-end IP configuration named FrontEndIp01, for the gateway in $AppGw, using the address stored in $PublicIp.</span></span>

### <span data-ttu-id="1b231-119">예제 2: 정적 개인 IP를 응용 프로그램 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="1b231-119">Example 2: Set a static private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet -PrivateIPAddress 10.0.1.1
```

<span data-ttu-id="1b231-120">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-120">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="1b231-121">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-121">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="1b231-122">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-122">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1b231-123">네 번째 명령은 두번째 명령 및 개인 IP 주소 10.0.1.1에서 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-123">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command and the private IP address 10.0.1.1.</span></span>

### <span data-ttu-id="1b231-124">예제 3: 동적 개인 IP를 응용 프로그램 게이트웨이의 프런트 엔드 IP로 설정</span><span class="sxs-lookup"><span data-stu-id="1b231-124">Example 3: Set a dynamic private IP as the front-end IP of an application gateway</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontendIP02" -Subnet $Subnet
```

<span data-ttu-id="1b231-125">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 VNet01 이라는 가상 네트워크를 가져와 $VNet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-125">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01, and stores it in the $VNet variable.</span></span>

<span data-ttu-id="1b231-126">두 번째 명령은 첫 번째 명령의 $VNet를 사용 하 여 Subnet01 이라는 서브넷 구성을 가져와 $Subnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-126">The second command gets a subnet configuration named Subnet01 using $VNet from the first command and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="1b231-127">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-127">The third command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1b231-128">네 번째 명령은 $Subnet를 사용 하 여 FrontendIP02 라는 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-128">The fourth command adds a front-end IP configuration named FrontendIP02 using $Subnet from the second command.</span></span>

## <span data-ttu-id="1b231-129">변수</span><span class="sxs-lookup"><span data-stu-id="1b231-129">PARAMETERS</span></span>

### <span data-ttu-id="1b231-130">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b231-130">-ApplicationGateway</span></span>
<span data-ttu-id="1b231-131">프런트 엔드 IP 구성을 수정할 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-131">Specifies an application gateway object in which to modify the front-end IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b231-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b231-132">-DefaultProfile</span></span>
<span data-ttu-id="1b231-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b231-134">-이름</span><span class="sxs-lookup"><span data-stu-id="1b231-134">-Name</span></span>
<span data-ttu-id="1b231-135">이 cmdlet이 수정 하는 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-135">Specifies the name of the front-end IP configuration that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1b231-136">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="1b231-136">-PrivateIPAddress</span></span>
<span data-ttu-id="1b231-137">개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-137">Specifies the private IP address.</span></span>
<span data-ttu-id="1b231-138">지정 된 경우이 IP가 서브넷에서 정적으로 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-138">If specified, this IP is statically allocated from the subnet.</span></span>

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

### <span data-ttu-id="1b231-139">-PublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="1b231-139">-PublicIPAddress</span></span>
<span data-ttu-id="1b231-140">공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-140">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="1b231-141">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1b231-141">-PublicIPAddressId</span></span>
<span data-ttu-id="1b231-142">공용 IP 주소의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-142">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="1b231-143">-서브넷</span><span class="sxs-lookup"><span data-stu-id="1b231-143">-Subnet</span></span>
<span data-ttu-id="1b231-144">응용 프로그램 게이트웨이에서 사용 하는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-144">Specifies the subnet that the application gateway uses.</span></span>
<span data-ttu-id="1b231-145">게이트웨이에서 개인 IP 주소를 사용 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-145">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="1b231-146">*PrivateIPAddress* address가 지정 된 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-146">If the *PrivateIPAddress* address is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="1b231-147">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-147">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1b231-148">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1b231-148">-SubnetId</span></span>
<span data-ttu-id="1b231-149">서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-149">Specifies the subnet ID.</span></span>
<span data-ttu-id="1b231-150">게이트웨이에서 개인 IP 주소를 사용 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-150">Specify this parameter if the gateway uses a private IP address.</span></span>
<span data-ttu-id="1b231-151">*PrivateIPAddress* 매개 변수를 지정한 경우이 서브넷에 속해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-151">If the *PrivateIPAddress* parameter is specified, it should belong to this subnet.</span></span>
<span data-ttu-id="1b231-152">*PrivateIPAddress* 가 지정 되지 않은 경우이 서브넷의 ip 주소 중 하나가 동적으로 응용 프로그램 게이트웨이의 프런트 엔드 IP 주소로 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-152">If *PrivateIPAddress* is not specified, one of the IP addresses from this subnet is dynamically picked up as the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="1b231-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b231-153">CommonParameters</span></span>
<span data-ttu-id="1b231-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b231-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b231-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b231-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b231-156">입력</span><span class="sxs-lookup"><span data-stu-id="1b231-156">INPUTS</span></span>

### <span data-ttu-id="1b231-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1b231-157">System.String</span></span>

## <span data-ttu-id="1b231-158">출력</span><span class="sxs-lookup"><span data-stu-id="1b231-158">OUTPUTS</span></span>

### <span data-ttu-id="1b231-159">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1b231-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1b231-160">상속자</span><span class="sxs-lookup"><span data-stu-id="1b231-160">NOTES</span></span>

## <span data-ttu-id="1b231-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b231-161">RELATED LINKS</span></span>

[<span data-ttu-id="1b231-162">추가-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b231-162">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1b231-163">추가-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b231-163">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1b231-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b231-164">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1b231-165">새로운 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b231-165">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1b231-166">제거-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1b231-166">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

