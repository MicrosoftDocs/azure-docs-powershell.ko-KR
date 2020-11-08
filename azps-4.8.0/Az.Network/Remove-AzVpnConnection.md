---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnConnection.md
ms.openlocfilehash: 825090358ea94223d483fe418d06896f1f741045
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203900"
---
# <span data-ttu-id="a54ca-101">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a54ca-101">Remove-AzVpnConnection</span></span>

## <span data-ttu-id="a54ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a54ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a54ca-103">VpnConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-103">Removes a VpnConnection.</span></span>

## <span data-ttu-id="a54ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a54ca-104">SYNTAX</span></span>

### <span data-ttu-id="a54ca-105">ByVpnConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a54ca-105">ByVpnConnectionName (Default)</span></span>
```
Remove-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a54ca-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="a54ca-106">ByVpnConnectionResourceId</span></span>
```
Remove-AzVpnConnection -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a54ca-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a54ca-107">ByVpnConnectionObject</span></span>
```
Remove-AzVpnConnection -InputObject <PSVpnConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a54ca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a54ca-108">DESCRIPTION</span></span>
<span data-ttu-id="a54ca-109">VpnConnection를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-109">Removes a VpnConnection.</span></span>

## <span data-ttu-id="a54ca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a54ca-110">EXAMPLES</span></span>

### <span data-ttu-id="a54ca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a54ca-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Remove-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"
```

<span data-ttu-id="a54ca-112">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a54ca-113">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a54ca-114">게이트웨이가 만들어지면 New-AzVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="a54ca-115">그런 다음 연결 이름을 사용 하 여 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="a54ca-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="a54ca-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" | Remove-AzVpnConnection
```

<span data-ttu-id="a54ca-117">예제 1과 동일 하지만 이제 AzVpnConnection에서 파이핑 된 개체를 사용 하 여 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-117">Same as example 1, but it now removes the connection using the piped object from Get-AzVpnConnection.</span></span>

## <span data-ttu-id="a54ca-118">변수</span><span class="sxs-lookup"><span data-stu-id="a54ca-118">PARAMETERS</span></span>

### <span data-ttu-id="a54ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54ca-119">-DefaultProfile</span></span>
<span data-ttu-id="a54ca-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54ca-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a54ca-121">-Force</span></span>
<span data-ttu-id="a54ca-122">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="a54ca-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a54ca-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a54ca-123">-InputObject</span></span>
<span data-ttu-id="a54ca-124">업데이트할 VpnConnection 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-124">The VpnConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a54ca-125">-이름</span><span class="sxs-lookup"><span data-stu-id="a54ca-125">-Name</span></span>
<span data-ttu-id="a54ca-126">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54ca-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="a54ca-127">-ParentResourceName</span></span>
<span data-ttu-id="a54ca-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54ca-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a54ca-129">-PassThru</span></span>
<span data-ttu-id="a54ca-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a54ca-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a54ca-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a54ca-132">-ResourceGroupName</span></span>
<span data-ttu-id="a54ca-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54ca-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a54ca-134">-ResourceId</span></span>
<span data-ttu-id="a54ca-135">삭제할 VpnConnection 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-135">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a54ca-136">-확인</span><span class="sxs-lookup"><span data-stu-id="a54ca-136">-Confirm</span></span>
<span data-ttu-id="a54ca-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a54ca-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a54ca-138">-WhatIf</span></span>
<span data-ttu-id="a54ca-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a54ca-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a54ca-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54ca-141">CommonParameters</span></span>
<span data-ttu-id="a54ca-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a54ca-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54ca-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a54ca-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54ca-144">입력</span><span class="sxs-lookup"><span data-stu-id="a54ca-144">INPUTS</span></span>

### <span data-ttu-id="a54ca-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a54ca-145">System.String</span></span>

### <span data-ttu-id="a54ca-146">PSVpnConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a54ca-146">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="a54ca-147">출력</span><span class="sxs-lookup"><span data-stu-id="a54ca-147">OUTPUTS</span></span>

### <span data-ttu-id="a54ca-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a54ca-148">System.Boolean</span></span>

## <span data-ttu-id="a54ca-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a54ca-149">NOTES</span></span>

## <span data-ttu-id="a54ca-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a54ca-150">RELATED LINKS</span></span>

[<span data-ttu-id="a54ca-151">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a54ca-151">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="a54ca-152">새로운 AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a54ca-152">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="a54ca-153">업데이트-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="a54ca-153">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)