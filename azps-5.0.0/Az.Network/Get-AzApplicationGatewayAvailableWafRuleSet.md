---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218358"
---
# <span data-ttu-id="40116-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="40116-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="40116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40116-102">SYNOPSIS</span></span>
<span data-ttu-id="40116-103">사용할 수 있는 모든 웹 응용 프로그램 방화벽 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40116-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="40116-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40116-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40116-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40116-105">DESCRIPTION</span></span>
<span data-ttu-id="40116-106">**AzApplicationGatewayAvailableWafRuleSet** cmdlet은 사용 가능한 모든 웹 응용 프로그램 방화벽 규칙 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40116-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="40116-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40116-107">EXAMPLES</span></span>

### <span data-ttu-id="40116-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="40116-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="40116-109">이 명령은 사용 가능한 모든 웹 응용 프로그램 방화벽 규칙 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="40116-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="40116-110">변수</span><span class="sxs-lookup"><span data-stu-id="40116-110">PARAMETERS</span></span>

### <span data-ttu-id="40116-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40116-111">-DefaultProfile</span></span>
<span data-ttu-id="40116-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40116-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40116-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40116-113">CommonParameters</span></span>
<span data-ttu-id="40116-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40116-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40116-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40116-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40116-116">입력</span><span class="sxs-lookup"><span data-stu-id="40116-116">INPUTS</span></span>

### <span data-ttu-id="40116-117">않아야</span><span class="sxs-lookup"><span data-stu-id="40116-117">None</span></span>

## <span data-ttu-id="40116-118">출력</span><span class="sxs-lookup"><span data-stu-id="40116-118">OUTPUTS</span></span>

### <span data-ttu-id="40116-119">PSApplicationGatewayAvailableWafRuleSetsResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="40116-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="40116-120">상속자</span><span class="sxs-lookup"><span data-stu-id="40116-120">NOTES</span></span>
<span data-ttu-id="40116-121">**List-AzApplicationGatewayAvailableWafRuleSets** 는 **AzApplicationGatewayAvailableWafRuleSet** cmdlet에 대 한 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="40116-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="40116-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40116-122">RELATED LINKS</span></span>