---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 245129e314bc5fd9cfe81d6d9f218a011ffef55d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527883"
---
# <span data-ttu-id="c59a4-101">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c59a4-101">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="c59a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c59a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c59a4-103">부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-103">Adds a front-end IP configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c59a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c59a4-104">SYNTAX</span></span>

### <span data-ttu-id="c59a4-105">SetByResourceSubnet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c59a4-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59a4-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="c59a4-106">SetByResourceIdSubnet</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59a4-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c59a4-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59a4-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c59a4-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c59a4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c59a4-109">DESCRIPTION</span></span>
<span data-ttu-id="c59a4-110">**Add-AzureRmLoadBalancerFrontendIpConifg** Cmdlet은 Azure 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-110">The **Add-AzureRmLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c59a4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c59a4-111">EXAMPLES</span></span>

### <span data-ttu-id="c59a4-112">예제 1 동적 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="c59a4-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c59a4-113">첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzureRmVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="c59a4-114">그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="c59a4-115">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzureRmLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $MySubnet 이라는 변수에 저장 된 서브넷의 동적 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="c59a4-116">예제 2 고정 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="c59a4-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzureRmVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c59a4-117">첫 번째 명령은 MyVnet 이라는 Azure 가상 네트워크를 가져오고 파이프라인을 사용 하 여 **AzureRmVirtualNetworkSubnetConfig** cmdlet에 대 한 결과를 전달 하 여 myvnet 이라는 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="c59a4-118">그런 다음 명령을 $Subnet 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="c59a4-119">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 **AzureRmLoadBalancerFrontendIpConfig** cmdlet에 전달 하며,이는 $Subnet 이라는 변수에 저장 된 서브넷의 고정 개인 ip 주소를 사용 하 여 로드 균형 조정기에 프런트 엔드 ip 구성을 추가 하는 것을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="c59a4-120">예제 3 공용 IP 주소를 사용 하 여 프런트 엔드 IP 구성 추가</span><span class="sxs-lookup"><span data-stu-id="c59a4-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzureRmPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzureRmLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c59a4-121">첫 번째 명령은 MyPub 이라는 Azure 공개 IP 주소를 가져온 다음 그 결과를 $PublicIp 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="c59a4-122">두 번째 명령은 MyLB 라는 부하 분산 장치를 가져와 AzureRmLoadBalancerFrontendIpConfig cmdlet에 전달 하 고 공용 IP 주소가 $PublicIp 라는 변수에 저장 된 부하 분산에 프런트 엔드 IP 구성을 추가 하는 결과를 **추가** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzureRmLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="c59a4-123">변수</span><span class="sxs-lookup"><span data-stu-id="c59a4-123">PARAMETERS</span></span>

### <span data-ttu-id="c59a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59a4-124">-DefaultProfile</span></span>
<span data-ttu-id="c59a4-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c59a4-126">-LoadBalancer</span></span>
<span data-ttu-id="c59a4-127">**LoadBalancer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c59a4-128">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 프런트 엔드 IP 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-129">-이름</span><span class="sxs-lookup"><span data-stu-id="c59a4-129">-Name</span></span>
<span data-ttu-id="c59a4-130">추가할 프런트 엔드 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="c59a4-131">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c59a4-131">-PrivateIpAddress</span></span>
<span data-ttu-id="c59a4-132">프런트 엔드 IP 구성에 연결할 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c59a4-133">-PublicIpAddress</span></span>
<span data-ttu-id="c59a4-134">프런트 엔드 IP 구성과 연결할 공용 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-135">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c59a4-135">-PublicIpAddressId</span></span>
<span data-ttu-id="c59a4-136">프런트 엔드 IP 구성을 추가할 공용 IP 주소의 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-137">-서브넷</span><span class="sxs-lookup"><span data-stu-id="c59a4-137">-Subnet</span></span>
<span data-ttu-id="c59a4-138">프런트 엔드 IP 구성을 추가할 서브넷 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c59a4-139">-SubnetId</span></span>
<span data-ttu-id="c59a4-140">프런트 엔드 IP 구성을 추가할 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-141">-Zone</span><span class="sxs-lookup"><span data-stu-id="c59a4-141">-Zone</span></span>
<span data-ttu-id="c59a4-142">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c59a4-143">-확인</span><span class="sxs-lookup"><span data-stu-id="c59a4-143">-Confirm</span></span>
<span data-ttu-id="c59a4-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59a4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59a4-145">-WhatIf</span></span>
<span data-ttu-id="c59a4-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c59a4-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59a4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59a4-148">CommonParameters</span></span>
<span data-ttu-id="c59a4-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59a4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59a4-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59a4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59a4-151">입력</span><span class="sxs-lookup"><span data-stu-id="c59a4-151">INPUTS</span></span>

### <span data-ttu-id="c59a4-152">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c59a4-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c59a4-153">매개 변수: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c59a4-153">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="c59a4-154">System.webserver. 목록 \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c59a4-154">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c59a4-155">출력</span><span class="sxs-lookup"><span data-stu-id="c59a4-155">OUTPUTS</span></span>

### <span data-ttu-id="c59a4-156">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c59a4-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c59a4-157">상속자</span><span class="sxs-lookup"><span data-stu-id="c59a4-157">NOTES</span></span>

## <span data-ttu-id="c59a4-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c59a4-158">RELATED LINKS</span></span>

[<span data-ttu-id="c59a4-159">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c59a4-159">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c59a4-160">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c59a4-160">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c59a4-161">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c59a4-161">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="c59a4-162">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c59a4-162">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c59a4-163">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c59a4-163">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c59a4-164">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c59a4-164">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)

