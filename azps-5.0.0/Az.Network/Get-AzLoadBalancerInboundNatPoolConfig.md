---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216226"
---
# <span data-ttu-id="1d335-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1d335-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="1d335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d335-102">SYNOPSIS</span></span>
<span data-ttu-id="1d335-103">부하 분산 장치에서 하나 이상의 인바운드 NAT 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d335-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="1d335-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d335-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d335-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d335-105">DESCRIPTION</span></span>
<span data-ttu-id="1d335-106">**Get-AzLoadBalancerInboundNatPoolConfig** cmdlet은 부하 분산 장치에서 하나 이상의 인바운드 NAT 풀 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d335-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="1d335-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d335-107">EXAMPLES</span></span>

### <span data-ttu-id="1d335-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="1d335-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="1d335-109">변수</span><span class="sxs-lookup"><span data-stu-id="1d335-109">PARAMETERS</span></span>

### <span data-ttu-id="1d335-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d335-110">-DefaultProfile</span></span>
<span data-ttu-id="1d335-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d335-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d335-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d335-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="1d335-113">-이름</span><span class="sxs-lookup"><span data-stu-id="1d335-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d335-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d335-114">CommonParameters</span></span>
<span data-ttu-id="1d335-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d335-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d335-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1d335-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d335-117">입력</span><span class="sxs-lookup"><span data-stu-id="1d335-117">INPUTS</span></span>

### <span data-ttu-id="1d335-118">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d335-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1d335-119">출력</span><span class="sxs-lookup"><span data-stu-id="1d335-119">OUTPUTS</span></span>

### <span data-ttu-id="1d335-120">PSInboundNatPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1d335-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="1d335-121">상속자</span><span class="sxs-lookup"><span data-stu-id="1d335-121">NOTES</span></span>

## <span data-ttu-id="1d335-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d335-122">RELATED LINKS</span></span>

[<span data-ttu-id="1d335-123">추가-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1d335-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="1d335-124">새로운 AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1d335-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="1d335-125">제거-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1d335-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="1d335-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1d335-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)