---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043583"
---
# <span data-ttu-id="4fa9a-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="4fa9a-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="4fa9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fa9a-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa9a-103">응용 프로그램 게이트웨이의 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="4fa9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fa9a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fa9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fa9a-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa9a-106">**AzApplicationGatewayAvailableSslOption** cmdlet은 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4fa9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4fa9a-107">EXAMPLES</span></span>

### <span data-ttu-id="4fa9a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4fa9a-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="4fa9a-109">이 명령은 ssl 정책에 대해 사용 가능한 모든 ssl 옵션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4fa9a-110">변수</span><span class="sxs-lookup"><span data-stu-id="4fa9a-110">PARAMETERS</span></span>

### <span data-ttu-id="4fa9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa9a-111">-DefaultProfile</span></span>
<span data-ttu-id="4fa9a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa9a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa9a-113">CommonParameters</span></span>
<span data-ttu-id="4fa9a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa9a-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa9a-116">입력</span><span class="sxs-lookup"><span data-stu-id="4fa9a-116">INPUTS</span></span>

### <span data-ttu-id="4fa9a-117">않아야</span><span class="sxs-lookup"><span data-stu-id="4fa9a-117">None</span></span>

## <span data-ttu-id="4fa9a-118">출력</span><span class="sxs-lookup"><span data-stu-id="4fa9a-118">OUTPUTS</span></span>

### <span data-ttu-id="4fa9a-119">PSApplicationGatewayAvailableSslOptions에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4fa9a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4fa9a-120">상속자</span><span class="sxs-lookup"><span data-stu-id="4fa9a-120">NOTES</span></span>

## <span data-ttu-id="4fa9a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fa9a-121">RELATED LINKS</span></span>