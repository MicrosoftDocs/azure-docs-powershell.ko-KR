---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218843"
---
# <span data-ttu-id="8c10d-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="8c10d-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="8c10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c10d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c10d-103">사용할 수 있는 Azure 방화벽 Fqdn 태그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c10d-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="8c10d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c10d-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c10d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8c10d-105">DESCRIPTION</span></span>
<span data-ttu-id="8c10d-106">**AzFirewallFqdnTag** Cmdlet은 Azure 방화벽 응용 프로그램 규칙에 사용할 수 있는 FQDN 태그 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8c10d-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="8c10d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8c10d-107">EXAMPLES</span></span>

### <span data-ttu-id="8c10d-108">1: 사용 가능한 모든 FQDN 태그 검색</span><span class="sxs-lookup"><span data-stu-id="8c10d-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="8c10d-109">이 예제에서는 사용 가능한 모든 FQDN 태그를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c10d-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="8c10d-110">2: 응용 프로그램 규칙에서 사용할 수 있는 첫 번째 FQDN 태그 사용</span><span class="sxs-lookup"><span data-stu-id="8c10d-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="8c10d-111">이 예제에서는 사용 가능한 첫 번째 FQDN 태그를 사용 하 여 방화벽 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c10d-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="8c10d-112">변수</span><span class="sxs-lookup"><span data-stu-id="8c10d-112">PARAMETERS</span></span>

### <span data-ttu-id="8c10d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c10d-113">-DefaultProfile</span></span>
<span data-ttu-id="8c10d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c10d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c10d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c10d-115">CommonParameters</span></span>
<span data-ttu-id="8c10d-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c10d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c10d-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8c10d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c10d-118">입력</span><span class="sxs-lookup"><span data-stu-id="8c10d-118">INPUTS</span></span>

### <span data-ttu-id="8c10d-119">않아야</span><span class="sxs-lookup"><span data-stu-id="8c10d-119">None</span></span>

## <span data-ttu-id="8c10d-120">출력</span><span class="sxs-lookup"><span data-stu-id="8c10d-120">OUTPUTS</span></span>

### <span data-ttu-id="8c10d-121">PSAzureFirewallFqdnTag에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8c10d-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="8c10d-122">System.webserver. t e 1 [[Microsoft PSAzureFirewallFqdnTag, Microsoft azure. e 1. \*. PowerShell, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8c10d-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8c10d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="8c10d-123">NOTES</span></span>

## <span data-ttu-id="8c10d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c10d-124">RELATED LINKS</span></span>

[<span data-ttu-id="8c10d-125">새로운 AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="8c10d-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="8c10d-126">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8c10d-126">New-AzFirewall</span></span>](./New-AzFirewall.md)