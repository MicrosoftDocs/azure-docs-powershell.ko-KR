---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043935"
---
# <span data-ttu-id="ed6e9-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed6e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6e9-103">가상 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="ed6e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed6e9-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6e9-106">가상 네트워크 게이트웨이를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="ed6e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ed6e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6e9-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="ed6e9-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="ed6e9-109">변수</span><span class="sxs-lookup"><span data-stu-id="ed6e9-109">PARAMETERS</span></span>

### <span data-ttu-id="ed6e9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed6e9-110">-AsJob</span></span>
<span data-ttu-id="ed6e9-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ed6e9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed6e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6e9-112">-DefaultProfile</span></span>
<span data-ttu-id="ed6e9-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed6e9-114">-게이트웨이 Vip</span><span class="sxs-lookup"><span data-stu-id="ed6e9-114">-GatewayVip</span></span>
<span data-ttu-id="ed6e9-115">특정 게이트웨이 인스턴스를 다시 설정 하기 위한 게이트웨이 vip (예: Active-Active 기능을 사용할 수 있는 게이트웨이를 사용 하는 경우) 값이 전달 되지 않으면 기본적으로 게이트웨이 기본 인스턴스가 다시 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6e9-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="ed6e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6e9-117">CommonParameters</span></span>
<span data-ttu-id="ed6e9-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6e9-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6e9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6e9-120">입력</span><span class="sxs-lookup"><span data-stu-id="ed6e9-120">INPUTS</span></span>

### <span data-ttu-id="ed6e9-121">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ed6e9-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ed6e9-122">System.String</span></span>

## <span data-ttu-id="ed6e9-123">출력</span><span class="sxs-lookup"><span data-stu-id="ed6e9-123">OUTPUTS</span></span>

### <span data-ttu-id="ed6e9-124">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed6e9-125">상속자</span><span class="sxs-lookup"><span data-stu-id="ed6e9-125">NOTES</span></span>

## <span data-ttu-id="ed6e9-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed6e9-126">RELATED LINKS</span></span>

[<span data-ttu-id="ed6e9-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed6e9-128">새로운 AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed6e9-129">제거-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed6e9-130">크기 조정-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed6e9-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed6e9-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)