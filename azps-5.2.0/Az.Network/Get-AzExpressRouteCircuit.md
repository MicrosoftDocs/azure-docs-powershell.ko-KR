---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuit.md
ms.openlocfilehash: 7997949db725d50dd656479852b10d12094b8da7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323791"
---
# <span data-ttu-id="b7cdb-101">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7cdb-101">Get-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="b7cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cdb-103">Azure에서 Azure ExpressRoute 회로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

## <span data-ttu-id="b7cdb-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7cdb-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7cdb-105">설명</span><span class="sxs-lookup"><span data-stu-id="b7cdb-105">DESCRIPTION</span></span>
<span data-ttu-id="b7cdb-106">**Get-AzExpressRouteCircuit** cmdlet은 구독에서 ExpressRoute 회로 개체를 검색하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-106">The **Get-AzExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="b7cdb-107">반환된 회로 개체는 ExpressRoute 회로에서 작동하는 다른 cmdlet에 대한 입력으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="b7cdb-108">예제</span><span class="sxs-lookup"><span data-stu-id="b7cdb-108">EXAMPLES</span></span>

### <span data-ttu-id="b7cdb-109">예제 1: ExpressRoute 회로를 얻게</span><span class="sxs-lookup"><span data-stu-id="b7cdb-109">Example 1: Get the ExpressRoute circuit</span></span>
```
Get-AzExpressRouteCircuit -ResourceGroupName testrg -Name test

Name                             : test
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="b7cdb-110">이름 "testrg" 및 ResourceGroupName "test"를 사용하여 특정 ExpressRoute 회로를 구합니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-110">Get a specific ExpressRoute circuit with Name "testrg" and ResourceGroupName "test"</span></span>

### <span data-ttu-id="b7cdb-111">예제 2: 필터링을 사용하여 ExpressRoute 회로 나열</span><span class="sxs-lookup"><span data-stu-id="b7cdb-111">Example 2: List the ExpressRoute circuits using filtering</span></span>
```
Get-AzExpressRouteCircuit -Name test*

Name                             : test1
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test1
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :

Name                             : test2
ResourceGroupName                : testrg
Location                         : southcentralus
Id                               : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/pro
                                   viders/Microsoft.Network/expressRouteCircuits/test2
Etag                             : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState                : Succeeded
Sku                              : {
                                     "Name": "Standard_UnlimitedData",
                                     "Tier": "Standard",
                                     "Family": "UnlimitedData"
                                   }
CircuitProvisioningState         : Enabled
ServiceProviderProvisioningState : NotProvisioned
ServiceProviderNotes             :
ServiceProviderProperties        : {
                                     "ServiceProviderName": "AT&T",
                                     "PeeringLocation": "Silicon Valley",
                                     "BandwidthInMbps": 50
                                   }
ExpressRoutePort                 : null
BandwidthInGbps                  :
Stag                             :
ServiceKey                       : 00000000-0000-0000-0000-000000000000
Peerings                         : []
Authorizations                   : []
AllowClassicOperations           : False
GatewayManagerEtag               :
```

<span data-ttu-id="b7cdb-112">이름이 "test"로 시작하는 모든 ExpressRoute 회로를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-112">Get all ExpressRoute circuits whose name starts with "test".</span></span>

## <span data-ttu-id="b7cdb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7cdb-113">PARAMETERS</span></span>

### <span data-ttu-id="b7cdb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cdb-114">-DefaultProfile</span></span>
<span data-ttu-id="b7cdb-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7cdb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b7cdb-116">-Name</span></span>
<span data-ttu-id="b7cdb-117">ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-117">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7cdb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cdb-118">-ResourceGroupName</span></span>
<span data-ttu-id="b7cdb-119">ExpressRoute 회로를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-119">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7cdb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cdb-120">CommonParameters</span></span>
<span data-ttu-id="b7cdb-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cdb-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7cdb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cdb-123">입력</span><span class="sxs-lookup"><span data-stu-id="b7cdb-123">INPUTS</span></span>

### <span data-ttu-id="b7cdb-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b7cdb-124">System.String</span></span>

## <span data-ttu-id="b7cdb-125">출력</span><span class="sxs-lookup"><span data-stu-id="b7cdb-125">OUTPUTS</span></span>

### <span data-ttu-id="b7cdb-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7cdb-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b7cdb-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7cdb-127">NOTES</span></span>

## <span data-ttu-id="b7cdb-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7cdb-128">RELATED LINKS</span></span>

[<span data-ttu-id="b7cdb-129">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7cdb-129">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7cdb-130">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7cdb-130">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7cdb-131">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7cdb-131">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7cdb-132">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7cdb-132">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)