---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 79bf22b5da9426ccb895b42faaeb4b01036828aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870101"
---
# <span data-ttu-id="9eccc-101">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9eccc-101">Get-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="9eccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eccc-102">SYNOPSIS</span></span>
<span data-ttu-id="9eccc-103">가상 허브에서 가상 네트워크 연결을 가져오거나 가상 허브의 모든 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="9eccc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9eccc-104">SYNTAX</span></span>

### <span data-ttu-id="9eccc-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9eccc-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eccc-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="9eccc-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eccc-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="9eccc-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eccc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9eccc-108">DESCRIPTION</span></span>
<span data-ttu-id="9eccc-109">가상 허브에서 가상 네트워크 연결을 가져오거나 가상 허브의 모든 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="9eccc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9eccc-110">EXAMPLES</span></span>

### <span data-ttu-id="9eccc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9eccc-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="9eccc-112">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="9eccc-113">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="9eccc-114">허브 가상 네트워크 연결을 만든 후에는 해당 리소스 그룹 이름, 허브 이름 및 연결 이름을 사용 하 여 허브 가상 네트워크 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="9eccc-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9eccc-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="9eccc-116">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="9eccc-117">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="9eccc-118">허브 가상 네트워크 연결을 만든 후에는 해당 리소스 그룹 이름과 허브 이름을 사용 하 여 모든 허브 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

### <span data-ttu-id="9eccc-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="9eccc-119">Example 3</span></span>

```powershell
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name test*

Name                 : testvnetconnection1
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection1
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded

Name                 : testvnetconnection2
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection2
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="9eccc-120">이 cmdlet은 리소스 그룹 이름 및 허브 이름을 사용 하 여 "test"로 시작 하는 모든 허브 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-120">This cmdlet lists all the hub virtual network connections starting with "test" using its resource group name and the hub name.</span></span>

## <span data-ttu-id="9eccc-121">변수</span><span class="sxs-lookup"><span data-stu-id="9eccc-121">PARAMETERS</span></span>

### <span data-ttu-id="9eccc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eccc-122">-DefaultProfile</span></span>
<span data-ttu-id="9eccc-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eccc-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9eccc-124">-Name</span></span>
<span data-ttu-id="9eccc-125">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9eccc-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9eccc-126">-ParentObject</span></span>
<span data-ttu-id="9eccc-127">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-127">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eccc-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9eccc-128">-ParentResourceId</span></span>
<span data-ttu-id="9eccc-129">부모 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-129">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eccc-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9eccc-130">-ParentResourceName</span></span>
<span data-ttu-id="9eccc-131">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eccc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eccc-132">-ResourceGroupName</span></span>
<span data-ttu-id="9eccc-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-133">The resource group name.</span></span>

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

### <span data-ttu-id="9eccc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eccc-134">CommonParameters</span></span>
<span data-ttu-id="9eccc-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eccc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eccc-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9eccc-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eccc-137">입력</span><span class="sxs-lookup"><span data-stu-id="9eccc-137">INPUTS</span></span>

### <span data-ttu-id="9eccc-138">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9eccc-138">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="9eccc-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9eccc-139">System.String</span></span>

## <span data-ttu-id="9eccc-140">출력</span><span class="sxs-lookup"><span data-stu-id="9eccc-140">OUTPUTS</span></span>

### <span data-ttu-id="9eccc-141">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9eccc-141">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="9eccc-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9eccc-142">NOTES</span></span>

## <span data-ttu-id="9eccc-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9eccc-143">RELATED LINKS</span></span>

[<span data-ttu-id="9eccc-144">새로운 AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9eccc-144">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="9eccc-145">제거-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="9eccc-145">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)