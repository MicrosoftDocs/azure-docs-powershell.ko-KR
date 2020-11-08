---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryPolicy.md
ms.openlocfilehash: a00e8d11868ae487357f1105d2bc2ae3934a9db9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211775"
---
# <span data-ttu-id="57d65-101">New-AzCdnDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="57d65-101">New-AzCdnDeliveryPolicy</span></span>

## <span data-ttu-id="57d65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d65-102">SYNOPSIS</span></span>
<span data-ttu-id="57d65-103">배달 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d65-103">Creates a delivery policy.</span></span>

## <span data-ttu-id="57d65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57d65-104">SYNTAX</span></span>

```
New-AzCdnDeliveryPolicy [-Description <String>] -Rule <PSDeliveryRule[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57d65-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57d65-105">DESCRIPTION</span></span>
<span data-ttu-id="57d65-106">**AzCdnDeliveryPolicy** CMDLET은 CDN 끝점 만들기에 대 한 배달 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57d65-106">The **New-AzCdnDeliveryPolicy** cmdlet creates a delivery policy for CDN endpoint creation.</span></span>

## <span data-ttu-id="57d65-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57d65-107">EXAMPLES</span></span>

### <span data-ttu-id="57d65-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="57d65-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryPolicy -Description "Sample Policy" -Rule $rule

Description   Rules
-----------   -----
Sample Policy {rule1}
```

<span data-ttu-id="57d65-109">예제 전달 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="57d65-109">Create a sample delivery policy</span></span>

## <span data-ttu-id="57d65-110">변수</span><span class="sxs-lookup"><span data-stu-id="57d65-110">PARAMETERS</span></span>

### <span data-ttu-id="57d65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d65-111">-DefaultProfile</span></span>
<span data-ttu-id="57d65-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57d65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57d65-113">-설명</span><span class="sxs-lookup"><span data-stu-id="57d65-113">-Description</span></span>
<span data-ttu-id="57d65-114">정책 설명</span><span class="sxs-lookup"><span data-stu-id="57d65-114">Description of the policy</span></span>

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

### <span data-ttu-id="57d65-115">-규칙</span><span class="sxs-lookup"><span data-stu-id="57d65-115">-Rule</span></span>
<span data-ttu-id="57d65-116">DeliveryRules의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="57d65-116">A list of deliveryRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d65-117">CommonParameters</span></span>
<span data-ttu-id="57d65-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57d65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d65-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57d65-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d65-120">입력</span><span class="sxs-lookup"><span data-stu-id="57d65-120">INPUTS</span></span>

### <span data-ttu-id="57d65-121">않아야</span><span class="sxs-lookup"><span data-stu-id="57d65-121">None</span></span>

## <span data-ttu-id="57d65-122">출력</span><span class="sxs-lookup"><span data-stu-id="57d65-122">OUTPUTS</span></span>

### <span data-ttu-id="57d65-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="57d65-123">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy</span></span>

## <span data-ttu-id="57d65-124">상속자</span><span class="sxs-lookup"><span data-stu-id="57d65-124">NOTES</span></span>

## <span data-ttu-id="57d65-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57d65-125">RELATED LINKS</span></span>