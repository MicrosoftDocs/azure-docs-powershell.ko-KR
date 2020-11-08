---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204490"
---
# <span data-ttu-id="ad59e-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ad59e-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ad59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad59e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad59e-103">연결에 사용 된 공유 키를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59e-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="ad59e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad59e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad59e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad59e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad59e-106">연결에 사용 된 공유 키를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59e-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="ad59e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad59e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad59e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad59e-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="ad59e-109">변수</span><span class="sxs-lookup"><span data-stu-id="ad59e-109">PARAMETERS</span></span>

### <span data-ttu-id="ad59e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad59e-110">-DefaultProfile</span></span>
<span data-ttu-id="ad59e-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad59e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad59e-112">-이름</span><span class="sxs-lookup"><span data-stu-id="ad59e-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad59e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad59e-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad59e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad59e-114">CommonParameters</span></span>
<span data-ttu-id="ad59e-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad59e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad59e-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad59e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad59e-117">입력</span><span class="sxs-lookup"><span data-stu-id="ad59e-117">INPUTS</span></span>

### <span data-ttu-id="ad59e-118">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad59e-118">System.String</span></span>

## <span data-ttu-id="ad59e-119">출력</span><span class="sxs-lookup"><span data-stu-id="ad59e-119">OUTPUTS</span></span>

### <span data-ttu-id="ad59e-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad59e-120">System.String</span></span>

## <span data-ttu-id="ad59e-121">상속자</span><span class="sxs-lookup"><span data-stu-id="ad59e-121">NOTES</span></span>

## <span data-ttu-id="ad59e-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad59e-122">RELATED LINKS</span></span>

[<span data-ttu-id="ad59e-123">다시 설정-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ad59e-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ad59e-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ad59e-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)