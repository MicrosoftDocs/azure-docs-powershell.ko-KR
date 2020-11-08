---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056232"
---
# <span data-ttu-id="63814-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63814-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="63814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63814-102">SYNOPSIS</span></span>
<span data-ttu-id="63814-103">Application Gateway의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63814-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="63814-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63814-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63814-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63814-105">DESCRIPTION</span></span>
<span data-ttu-id="63814-106">**AzApplicationGatewayAutoscaleConfiguration** Cmdlet은 Application Gateway의 자동 크기 조정 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="63814-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="63814-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63814-107">EXAMPLES</span></span>

### <span data-ttu-id="63814-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="63814-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="63814-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63814-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="63814-110">두 번째 명령은 응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 추출 합니다.</span><span class="sxs-lookup"><span data-stu-id="63814-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="63814-111">변수</span><span class="sxs-lookup"><span data-stu-id="63814-111">PARAMETERS</span></span>

### <span data-ttu-id="63814-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63814-112">-ApplicationGateway</span></span>
<span data-ttu-id="63814-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63814-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63814-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63814-114">-DefaultProfile</span></span>
<span data-ttu-id="63814-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63814-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63814-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63814-116">CommonParameters</span></span>
<span data-ttu-id="63814-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63814-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63814-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63814-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63814-119">입력</span><span class="sxs-lookup"><span data-stu-id="63814-119">INPUTS</span></span>

### <span data-ttu-id="63814-120">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63814-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63814-121">출력</span><span class="sxs-lookup"><span data-stu-id="63814-121">OUTPUTS</span></span>

### <span data-ttu-id="63814-122">PSApplicationGatewayAutoscaleConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63814-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="63814-123">상속자</span><span class="sxs-lookup"><span data-stu-id="63814-123">NOTES</span></span>

## <span data-ttu-id="63814-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63814-124">RELATED LINKS</span></span>

[<span data-ttu-id="63814-125">새로운 AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63814-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="63814-126">제거-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63814-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="63814-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="63814-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)