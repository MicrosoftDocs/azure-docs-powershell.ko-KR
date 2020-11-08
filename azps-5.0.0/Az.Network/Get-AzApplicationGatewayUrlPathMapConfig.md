---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226693"
---
# <span data-ttu-id="7a030-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7a030-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7a030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a030-102">SYNOPSIS</span></span>
<span data-ttu-id="7a030-103">백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7a030-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a030-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a030-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a030-105">DESCRIPTION</span></span>
<span data-ttu-id="7a030-106">**AzApplicationGatewayURLPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7a030-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a030-107">EXAMPLES</span></span>

### <span data-ttu-id="7a030-108">예제 1: URL 경로 맵 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="7a030-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="7a030-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 있는 백 엔드 서버에서 URL 경로 맵 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="7a030-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a030-110">PARAMETERS</span></span>

### <span data-ttu-id="7a030-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a030-111">-ApplicationGateway</span></span>
<span data-ttu-id="7a030-112">이 cmdlet이 URL 경로 맵 구성을 가져오는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="7a030-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a030-113">-DefaultProfile</span></span>
<span data-ttu-id="7a030-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a030-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7a030-115">-Name</span></span>
<span data-ttu-id="7a030-116">이 cmdlet이 경로 맵 구성을 가져올 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="7a030-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a030-117">CommonParameters</span></span>
<span data-ttu-id="7a030-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a030-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a030-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a030-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a030-120">입력</span><span class="sxs-lookup"><span data-stu-id="7a030-120">INPUTS</span></span>

### <span data-ttu-id="7a030-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7a030-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7a030-122">출력</span><span class="sxs-lookup"><span data-stu-id="7a030-122">OUTPUTS</span></span>

### <span data-ttu-id="7a030-123">PSApplicationGatewayUrlPathMap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7a030-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="7a030-124">상속자</span><span class="sxs-lookup"><span data-stu-id="7a030-124">NOTES</span></span>

## <span data-ttu-id="7a030-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a030-125">RELATED LINKS</span></span>

[<span data-ttu-id="7a030-126">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7a030-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7a030-127">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7a030-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7a030-128">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7a030-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7a030-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7a030-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

