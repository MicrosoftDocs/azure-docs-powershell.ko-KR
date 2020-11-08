---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043562"
---
# <span data-ttu-id="a58c1-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a58c1-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="a58c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a58c1-103">응용 프로그램 게이트웨이 방화벽 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="a58c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a58c1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58c1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a58c1-105">DESCRIPTION</span></span>
<span data-ttu-id="a58c1-106">**Get-AzApplicationGatewayFirewallPolicy** cmdlet은 응용 프로그램 게이트웨이 방화벽 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="a58c1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a58c1-107">EXAMPLES</span></span>

### <span data-ttu-id="a58c1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a58c1-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a58c1-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 FirewallPolicy1 라는 응용 프로그램 게이트웨이 방화벽 정책을 가져오고이를 $AppGwFirewallPolicy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="a58c1-110">변수</span><span class="sxs-lookup"><span data-stu-id="a58c1-110">PARAMETERS</span></span>

### <span data-ttu-id="a58c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58c1-111">-DefaultProfile</span></span>
<span data-ttu-id="a58c1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a58c1-113">-이름</span><span class="sxs-lookup"><span data-stu-id="a58c1-113">-Name</span></span>
<span data-ttu-id="a58c1-114">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-114">The resource name.</span></span>

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

### <span data-ttu-id="a58c1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58c1-115">-ResourceGroupName</span></span>
<span data-ttu-id="a58c1-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58c1-117">CommonParameters</span></span>
<span data-ttu-id="a58c1-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a58c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58c1-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a58c1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58c1-120">입력</span><span class="sxs-lookup"><span data-stu-id="a58c1-120">INPUTS</span></span>

### <span data-ttu-id="a58c1-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a58c1-121">System.String</span></span>

## <span data-ttu-id="a58c1-122">출력</span><span class="sxs-lookup"><span data-stu-id="a58c1-122">OUTPUTS</span></span>

### <span data-ttu-id="a58c1-123">PSApplicationGatewayWebApplicationFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a58c1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="a58c1-124">상속자</span><span class="sxs-lookup"><span data-stu-id="a58c1-124">NOTES</span></span>

## <span data-ttu-id="a58c1-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a58c1-125">RELATED LINKS</span></span>