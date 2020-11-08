---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204657"
---
# <span data-ttu-id="3e05b-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="3e05b-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="3e05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e05b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e05b-103">VMImage Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="3e05b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e05b-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e05b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e05b-105">DESCRIPTION</span></span>
<span data-ttu-id="3e05b-106">**Get-AzVMImageSku** Cmdlet은 VMImage sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="3e05b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3e05b-107">EXAMPLES</span></span>

### <span data-ttu-id="3e05b-108">예제 1: VMImage Sku 가져오기</span><span class="sxs-lookup"><span data-stu-id="3e05b-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="3e05b-109">이 명령은 지정 된 게시자 및 제안에 대 한 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="3e05b-110">변수</span><span class="sxs-lookup"><span data-stu-id="3e05b-110">PARAMETERS</span></span>

### <span data-ttu-id="3e05b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e05b-111">-DefaultProfile</span></span>
<span data-ttu-id="3e05b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e05b-113">-위치</span><span class="sxs-lookup"><span data-stu-id="3e05b-113">-Location</span></span>
<span data-ttu-id="3e05b-114">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="3e05b-115">-제공</span><span class="sxs-lookup"><span data-stu-id="3e05b-115">-Offer</span></span>
<span data-ttu-id="3e05b-116">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="3e05b-117">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="3e05b-117">-PublisherName</span></span>
<span data-ttu-id="3e05b-118">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="3e05b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e05b-119">CommonParameters</span></span>
<span data-ttu-id="3e05b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e05b-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3e05b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e05b-122">입력</span><span class="sxs-lookup"><span data-stu-id="3e05b-122">INPUTS</span></span>

### <span data-ttu-id="3e05b-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3e05b-123">System.String</span></span>

## <span data-ttu-id="3e05b-124">출력</span><span class="sxs-lookup"><span data-stu-id="3e05b-124">OUTPUTS</span></span>

### <span data-ttu-id="3e05b-125">PSVirtualMachineImageSku를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e05b-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="3e05b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3e05b-126">NOTES</span></span>

## <span data-ttu-id="3e05b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e05b-127">RELATED LINKS</span></span>

[<span data-ttu-id="3e05b-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3e05b-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="3e05b-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="3e05b-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="3e05b-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="3e05b-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="3e05b-131">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3e05b-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

