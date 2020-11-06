---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 0987823d2658778266f861a5115962d6cf8c4830
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532133"
---
# <span data-ttu-id="1f71d-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1f71d-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="1f71d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f71d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f71d-103">가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f71d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f71d-104">SYNTAX</span></span>

### <span data-ttu-id="1f71d-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f71d-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f71d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f71d-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f71d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f71d-107">DESCRIPTION</span></span>
<span data-ttu-id="1f71d-108">**Add-AzureRmVirtualNetworkSubnetConfig** cmdlet은 기존 Azure 가상 네트워크에 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="1f71d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1f71d-109">EXAMPLES</span></span>

### <span data-ttu-id="1f71d-110">1: 기존 가상 네트워크에 서브넷 추가</span><span class="sxs-lookup"><span data-stu-id="1f71d-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="1f71d-111">이 예제에서는 먼저 만들려는 리소스의 컨테이너로 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="1f71d-112">그런 다음 서브넷 구성을 만들고이를 사용 하 여 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="1f71d-113">그런 다음 Add-AzureRmVirtualNetworkSubnetConfig를 사용 하 여 가상 네트워크의 메모리 내 표현에 서브넷을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1f71d-114">Set-AzureRmVirtualNetwork 명령은 새 서브넷으로 기존 가상 네트워크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="1f71d-115">변수</span><span class="sxs-lookup"><span data-stu-id="1f71d-115">PARAMETERS</span></span>

### <span data-ttu-id="1f71d-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1f71d-116">-AddressPrefix</span></span>
<span data-ttu-id="1f71d-117">서브넷 구성에 대 한 IP 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="1f71d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f71d-118">-DefaultProfile</span></span>
<span data-ttu-id="1f71d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f71d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1f71d-120">-Name</span></span>
<span data-ttu-id="1f71d-121">추가할 서브넷 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="1f71d-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1f71d-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1f71d-123">**Networksecuritygroup** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="1f71d-124">이 cmdlet은이 매개 변수에서 지정 하는 개체에 가상 네트워크 서브넷 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71d-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="1f71d-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="1f71d-126">네트워크 보안 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-126">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71d-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1f71d-127">-RouteTable</span></span>
```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71d-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="1f71d-128">-RouteTableId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71d-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f71d-129">-ServiceEndpoint</span></span>
<span data-ttu-id="1f71d-130">서비스 끝점 값</span><span class="sxs-lookup"><span data-stu-id="1f71d-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="1f71d-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f71d-131">-VirtualNetwork</span></span>
<span data-ttu-id="1f71d-132">서브넷 구성을 추가할 **VirtualNetwork** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f71d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f71d-133">CommonParameters</span></span>
<span data-ttu-id="1f71d-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f71d-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f71d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f71d-136">입력</span><span class="sxs-lookup"><span data-stu-id="1f71d-136">INPUTS</span></span>

### <span data-ttu-id="1f71d-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f71d-137">PSVirtualNetwork</span></span>
<span data-ttu-id="1f71d-138">' VirtualNetwork ' 매개 변수는 파이프라인에서 ' PSVirtualNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f71d-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1f71d-139">출력</span><span class="sxs-lookup"><span data-stu-id="1f71d-139">OUTPUTS</span></span>

### <span data-ttu-id="1f71d-140">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1f71d-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="1f71d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1f71d-141">NOTES</span></span>

## <span data-ttu-id="1f71d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f71d-142">RELATED LINKS</span></span>

[<span data-ttu-id="1f71d-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1f71d-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1f71d-144">새로운 AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1f71d-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1f71d-145">제거-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1f71d-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1f71d-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1f71d-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)

