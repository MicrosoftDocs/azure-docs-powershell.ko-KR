---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 9f40d9ce99db8640fcf98d48f8dc3920a8517b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870645"
---
# <span data-ttu-id="fea28-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="fea28-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="fea28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fea28-102">SYNOPSIS</span></span>
<span data-ttu-id="fea28-103">개인 링크 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-103">Gets private link service</span></span>

## <span data-ttu-id="fea28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fea28-104">SYNTAX</span></span>

### <span data-ttu-id="fea28-105">NoExpand (기본값)</span><span class="sxs-lookup"><span data-stu-id="fea28-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fea28-106">확장</span><span class="sxs-lookup"><span data-stu-id="fea28-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fea28-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fea28-107">DESCRIPTION</span></span>
<span data-ttu-id="fea28-108">**AzPrivateLinkService** cmdlet은 하나 이상의 개인 링크 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="fea28-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fea28-109">EXAMPLES</span></span>

### <span data-ttu-id="fea28-110">예</span><span class="sxs-lookup"><span data-stu-id="fea28-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="fea28-111">이 작업은 리소스 그룹의 개인 링크 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="fea28-112">변수</span><span class="sxs-lookup"><span data-stu-id="fea28-112">PARAMETERS</span></span>

### <span data-ttu-id="fea28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea28-113">-DefaultProfile</span></span>
<span data-ttu-id="fea28-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fea28-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="fea28-115">-ExpandResource</span></span>
<span data-ttu-id="fea28-116">확장할 리소스 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea28-117">-이름</span><span class="sxs-lookup"><span data-stu-id="fea28-117">-Name</span></span>
<span data-ttu-id="fea28-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea28-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea28-119">-ResourceGroupName</span></span>
<span data-ttu-id="fea28-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea28-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea28-121">CommonParameters</span></span>
<span data-ttu-id="fea28-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fea28-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea28-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fea28-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea28-124">입력</span><span class="sxs-lookup"><span data-stu-id="fea28-124">INPUTS</span></span>

### <span data-ttu-id="fea28-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fea28-125">System.String</span></span>

## <span data-ttu-id="fea28-126">출력</span><span class="sxs-lookup"><span data-stu-id="fea28-126">OUTPUTS</span></span>

### <span data-ttu-id="fea28-127">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fea28-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="fea28-128">상속자</span><span class="sxs-lookup"><span data-stu-id="fea28-128">NOTES</span></span>

## <span data-ttu-id="fea28-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fea28-129">RELATED LINKS</span></span>