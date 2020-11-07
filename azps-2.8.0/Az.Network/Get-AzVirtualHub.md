---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870614"
---
# <span data-ttu-id="f01a4-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f01a4-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="f01a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f01a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f01a4-103">이름별로 Azure VirtualHub를 가져옵니다. ResourceGroupName 또는 ResourceGroupName/구독으로 모든 가상 허브가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="f01a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f01a4-104">SYNTAX</span></span>

### <span data-ttu-id="f01a4-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="f01a4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f01a4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f01a4-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f01a4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f01a4-107">DESCRIPTION</span></span>
<span data-ttu-id="f01a4-108">이름별로 Azure VirtualHub를 가져옵니다. ResourceGroupName 또는 ResourceGroupName/구독으로 모든 가상 허브가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="f01a4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f01a4-109">EXAMPLES</span></span>

### <span data-ttu-id="f01a4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f01a4-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="f01a4-111">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="f01a4-112">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="f01a4-113">그런 다음 해당 ResourceGroupName 및 Context.resourcename을 사용 하 여 가상 허브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="f01a4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f01a4-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="f01a4-115">이 cmdlet은 필터링을 사용 하 여 가상 허브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="f01a4-116">변수</span><span class="sxs-lookup"><span data-stu-id="f01a4-116">PARAMETERS</span></span>

### <span data-ttu-id="f01a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01a4-117">-DefaultProfile</span></span>
<span data-ttu-id="f01a4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f01a4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f01a4-119">-Name</span></span>
<span data-ttu-id="f01a4-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f01a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f01a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="f01a4-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="f01a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01a4-123">CommonParameters</span></span>
<span data-ttu-id="f01a4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f01a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01a4-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f01a4-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01a4-126">입력</span><span class="sxs-lookup"><span data-stu-id="f01a4-126">INPUTS</span></span>

### <span data-ttu-id="f01a4-127">않아야</span><span class="sxs-lookup"><span data-stu-id="f01a4-127">None</span></span>

## <span data-ttu-id="f01a4-128">출력</span><span class="sxs-lookup"><span data-stu-id="f01a4-128">OUTPUTS</span></span>

### <span data-ttu-id="f01a4-129">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f01a4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="f01a4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f01a4-130">NOTES</span></span>

## <span data-ttu-id="f01a4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f01a4-131">RELATED LINKS</span></span>

[<span data-ttu-id="f01a4-132">새로운 AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f01a4-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="f01a4-133">제거-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f01a4-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="f01a4-134">업데이트-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f01a4-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)