---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 15f1c71e313cfd684c384446f0ffd2913c69143c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531139"
---
# <span data-ttu-id="e6649-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="e6649-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="e6649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6649-102">SYNOPSIS</span></span>
<span data-ttu-id="e6649-103">위치에 사용할 수 있는 끝점 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6649-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6649-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6649-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6649-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6649-105">DESCRIPTION</span></span>
<span data-ttu-id="e6649-106">Get-AzureRmVirtualNetworkAvailableEndpointService는 지정 된 위치에서 사용할 수 있는 끝점 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6649-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="e6649-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6649-107">EXAMPLES</span></span>

### <span data-ttu-id="e6649-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6649-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="e6649-109">Westus 지역에서 사용할 수 있는 끝점 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6649-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="e6649-110">변수</span><span class="sxs-lookup"><span data-stu-id="e6649-110">PARAMETERS</span></span>

### <span data-ttu-id="e6649-111">-위치</span><span class="sxs-lookup"><span data-stu-id="e6649-111">-Location</span></span>
<span data-ttu-id="e6649-112">끝점 서비스를 검색할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e6649-112">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="e6649-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6649-113">-DefaultProfile</span></span>
<span data-ttu-id="e6649-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6649-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6649-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6649-115">CommonParameters</span></span>
<span data-ttu-id="e6649-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6649-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6649-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6649-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6649-118">입력</span><span class="sxs-lookup"><span data-stu-id="e6649-118">INPUTS</span></span>

### <span data-ttu-id="e6649-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6649-119">System.String</span></span>

## <span data-ttu-id="e6649-120">출력</span><span class="sxs-lookup"><span data-stu-id="e6649-120">OUTPUTS</span></span>

### <span data-ttu-id="e6649-121">System.webserver. List ' 1 [[PSEndpointServiceResult, Microsoft azure. 4.2.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e6649-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e6649-122">상속자</span><span class="sxs-lookup"><span data-stu-id="e6649-122">NOTES</span></span>

## <span data-ttu-id="e6649-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6649-123">RELATED LINKS</span></span>
