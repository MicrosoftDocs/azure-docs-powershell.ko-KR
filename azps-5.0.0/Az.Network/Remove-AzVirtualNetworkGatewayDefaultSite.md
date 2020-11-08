---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218301"
---
# <span data-ttu-id="e1d9a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e1d9a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="e1d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d9a-103">가상 네트워크 게이트웨이에서 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="e1d9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1d9a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e1d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d9a-106">**AzVirtualNetworkGatewayDefaultSite** cmdlet은 가상 네트워크 게이트웨이에서 강제 터널링 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="e1d9a-107">강제 터널링은 Azure 가상 컴퓨터에서 온-프레미스 네트워크로 인터넷에 바인딩된 트래픽을 리디렉션할 수 있는 방법을 제공 합니다. 이렇게 하면 트래픽을 해제 하기 전에 검사 하 고 감사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="e1d9a-108">강제 터널링은 VPN (가상 사설망) 터널을 사용 하 여 수행 됩니다. 이 터널에는 모든 Azure 인터넷 바인딩 트래픽이 리디렉션되는 기본 사이트 (로컬 게이트웨이)가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="e1d9a-109">**제거-AzVirtualNetworkGatewayDefaultSite** 는 게이트웨이에 할당 된 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="e1d9a-110">이렇게 하는 경우 게이트웨이를 강제 터널링에 사용할 수 있으려면 먼저 Set-AzVirtualNetworkGatewayDefaultSite를 사용 하 여 새 기본 사이트를 할당 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="e1d9a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e1d9a-111">EXAMPLES</span></span>

### <span data-ttu-id="e1d9a-112">예제 1: 가상 네트워크 게이트웨이에 할당 된 기본 사이트 제거</span><span class="sxs-lookup"><span data-stu-id="e1d9a-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="e1d9a-113">이 예제에서는 ContosoVirtualGateway 라는 가상 네트워크 게이트웨이에 현재 할당 된 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="e1d9a-114">첫 번째 명령은 **Get-AzVirtualNetworkGateway** 를 사용 하 여 게이트웨이에 대 한 개체 참조를 만듭니다. 이 개체 참조는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="e1d9a-115">그런 다음 두 번째 명령은 **remove-AzVirtualNetworkGatewayDefaultSite** 를 사용 하 여 해당 게이트웨이에 할당 된 기본 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="e1d9a-116">변수</span><span class="sxs-lookup"><span data-stu-id="e1d9a-116">PARAMETERS</span></span>

### <span data-ttu-id="e1d9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d9a-117">-DefaultProfile</span></span>
<span data-ttu-id="e1d9a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d9a-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1d9a-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="e1d9a-120">제거할 기본 사이트를 포함 하는 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="e1d9a-121">Get-AzVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d9a-122">CommonParameters</span></span>
<span data-ttu-id="e1d9a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d9a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d9a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d9a-125">입력</span><span class="sxs-lookup"><span data-stu-id="e1d9a-125">INPUTS</span></span>

### <span data-ttu-id="e1d9a-126">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e1d9a-127">출력</span><span class="sxs-lookup"><span data-stu-id="e1d9a-127">OUTPUTS</span></span>

### <span data-ttu-id="e1d9a-128">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e1d9a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e1d9a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e1d9a-129">NOTES</span></span>

## <span data-ttu-id="e1d9a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1d9a-130">RELATED LINKS</span></span>

[<span data-ttu-id="e1d9a-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e1d9a-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="e1d9a-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="e1d9a-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)

