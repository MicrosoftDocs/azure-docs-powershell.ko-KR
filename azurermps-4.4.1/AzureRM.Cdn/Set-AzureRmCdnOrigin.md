---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: c554caf7230b54db3e1161a20e001f9873f6dfff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531171"
---
# <span data-ttu-id="7f0cc-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7f0cc-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="7f0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0cc-103">CDN 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0cc-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f0cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f0cc-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f0cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0cc-106">**AzureRmCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0cc-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="7f0cc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7f0cc-107">EXAMPLES</span></span>

## <span data-ttu-id="7f0cc-108">변수</span><span class="sxs-lookup"><span data-stu-id="7f0cc-108">PARAMETERS</span></span>

### <span data-ttu-id="7f0cc-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7f0cc-109">-CdnOrigin</span></span>
<span data-ttu-id="7f0cc-110">이 cmdlet이 업데이트 하는 원본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0cc-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f0cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0cc-111">-DefaultProfile</span></span>
<span data-ttu-id="7f0cc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f0cc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0cc-113">CommonParameters</span></span>
<span data-ttu-id="7f0cc-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0cc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0cc-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0cc-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0cc-116">입력</span><span class="sxs-lookup"><span data-stu-id="7f0cc-116">INPUTS</span></span>

### <span data-ttu-id="7f0cc-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="7f0cc-117">PSOrigin</span></span>
<span data-ttu-id="7f0cc-118">' CdnOrigin' 매개 변수는 파이프라인에서 ' PSOrigin' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0cc-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="7f0cc-119">출력</span><span class="sxs-lookup"><span data-stu-id="7f0cc-119">OUTPUTS</span></span>

### <span data-ttu-id="7f0cc-120">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="7f0cc-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="7f0cc-121">상속자</span><span class="sxs-lookup"><span data-stu-id="7f0cc-121">NOTES</span></span>

## <span data-ttu-id="7f0cc-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f0cc-122">RELATED LINKS</span></span>

[<span data-ttu-id="7f0cc-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="7f0cc-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)

