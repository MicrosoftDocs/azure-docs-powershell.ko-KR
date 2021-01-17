---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/confirm-azcdnendpointprobeurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Confirm-AzCdnEndpointProbeURL.md
ms.openlocfilehash: dcd45719754cc8bbb3ef45d8aa9927ae30156937
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345554"
---
# <span data-ttu-id="903f3-101">Confirm-AzCdnEndpointProbeURL</span><span class="sxs-lookup"><span data-stu-id="903f3-101">Confirm-AzCdnEndpointProbeURL</span></span>

## <span data-ttu-id="903f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="903f3-102">SYNOPSIS</span></span>
<span data-ttu-id="903f3-103">프로브 URL의 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="903f3-103">Validates a probe URL.</span></span>

## <span data-ttu-id="903f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="903f3-104">SYNTAX</span></span>

```
Confirm-AzCdnEndpointProbeURL -ProbeUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="903f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="903f3-105">DESCRIPTION</span></span>
<span data-ttu-id="903f3-106">**Confirm-AzCdnEndpointProbeURL** cmdlet은 제공된 프로브 URL을 동적 사이트 가속에 사용할 수 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="903f3-106">The **Confirm-AzCdnEndpointProbeURL** cmdlet confirms if the probe URL provided can be used for dynamic site acceleration.</span></span>

## <span data-ttu-id="903f3-107">예제</span><span class="sxs-lookup"><span data-stu-id="903f3-107">EXAMPLES</span></span>

### <span data-ttu-id="903f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="903f3-108">Example 1</span></span>
```powershell
PS C:\> Confirm-AzCdnEndpointProbeURL -ProbeUrl "http://www.bing.com/images"
IsValid: true
ErrorCode: None
Message:
```

<span data-ttu-id="903f3-109">프로브 URL " "의 http://www.bing.com/images 유효성을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="903f3-109">Validates the probe url "http://www.bing.com/images"</span></span>

## <span data-ttu-id="903f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="903f3-110">PARAMETERS</span></span>

### <span data-ttu-id="903f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903f3-111">-DefaultProfile</span></span>
<span data-ttu-id="903f3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="903f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="903f3-113">-ProbeUrl</span><span class="sxs-lookup"><span data-stu-id="903f3-113">-ProbeUrl</span></span>
<span data-ttu-id="903f3-114">유효성을 검사할 제안된 프로브 URL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="903f3-114">Proposed probe URL name to validate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903f3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903f3-115">CommonParameters</span></span>
<span data-ttu-id="903f3-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="903f3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903f3-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="903f3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903f3-118">입력</span><span class="sxs-lookup"><span data-stu-id="903f3-118">INPUTS</span></span>

### <span data-ttu-id="903f3-119">없음</span><span class="sxs-lookup"><span data-stu-id="903f3-119">None</span></span>

## <span data-ttu-id="903f3-120">출력</span><span class="sxs-lookup"><span data-stu-id="903f3-120">OUTPUTS</span></span>

### <span data-ttu-id="903f3-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span><span class="sxs-lookup"><span data-stu-id="903f3-121">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateProbeOutput</span></span>

## <span data-ttu-id="903f3-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="903f3-122">NOTES</span></span>

## <span data-ttu-id="903f3-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="903f3-123">RELATED LINKS</span></span>