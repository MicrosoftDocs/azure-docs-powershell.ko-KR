---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: 650ffdfd557780727a4f3bc4c69a7be6f2783cb3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216215"
---
# <span data-ttu-id="01b93-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="01b93-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="01b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b93-102">SYNOPSIS</span></span>
<span data-ttu-id="01b93-103">리소스 그룹에서 이름 또는 NatGateway Id 또는 리소스 그룹의 모든 Nat 게이트웨이 리소스를 기준으로 Nat 게이트웨이 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01b93-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="01b93-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01b93-104">SYNTAX</span></span>

### <span data-ttu-id="01b93-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="01b93-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01b93-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b93-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01b93-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b93-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01b93-108">설명은</span><span class="sxs-lookup"><span data-stu-id="01b93-108">DESCRIPTION</span></span>
<span data-ttu-id="01b93-109">리소스 그룹에서 이름 또는 NatGateway Id 또는 리소스 그룹의 모든 Nat 게이트웨이 리소스를 기준으로 Nat 게이트웨이 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01b93-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="01b93-110">예제의</span><span class="sxs-lookup"><span data-stu-id="01b93-110">EXAMPLES</span></span>

### <span data-ttu-id="01b93-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="01b93-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="01b93-112">변수</span><span class="sxs-lookup"><span data-stu-id="01b93-112">PARAMETERS</span></span>

### <span data-ttu-id="01b93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b93-113">-DefaultProfile</span></span>
<span data-ttu-id="01b93-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01b93-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b93-115">-이름</span><span class="sxs-lookup"><span data-stu-id="01b93-115">-Name</span></span>
<span data-ttu-id="01b93-116">Nat 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01b93-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b93-117">-ResourceGroupName</span></span>
<span data-ttu-id="01b93-118">Nat 게이트웨이의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01b93-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b93-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01b93-119">-ResourceId</span></span>
<span data-ttu-id="01b93-120">Nat 게이트웨이 Id</span><span class="sxs-lookup"><span data-stu-id="01b93-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01b93-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b93-121">CommonParameters</span></span>
<span data-ttu-id="01b93-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01b93-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b93-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="01b93-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b93-124">입력</span><span class="sxs-lookup"><span data-stu-id="01b93-124">INPUTS</span></span>

### <span data-ttu-id="01b93-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01b93-125">System.String</span></span>

## <span data-ttu-id="01b93-126">출력</span><span class="sxs-lookup"><span data-stu-id="01b93-126">OUTPUTS</span></span>

### <span data-ttu-id="01b93-127">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="01b93-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="01b93-128">상속자</span><span class="sxs-lookup"><span data-stu-id="01b93-128">NOTES</span></span>

## <span data-ttu-id="01b93-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01b93-129">RELATED LINKS</span></span>