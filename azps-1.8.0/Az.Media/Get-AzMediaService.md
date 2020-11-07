---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: a6d1ff6d169fab90fa866e94577ce9b3f9580a4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867422"
---
# <span data-ttu-id="5d3dd-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5d3dd-101">Get-AzMediaService</span></span>

## <span data-ttu-id="5d3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3dd-103">미디어 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-103">Gets information about a media service.</span></span>

## <span data-ttu-id="5d3dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d3dd-104">SYNTAX</span></span>

### <span data-ttu-id="5d3dd-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3dd-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d3dd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d3dd-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d3dd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5d3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="5d3dd-108">**AzMediaService** cmdlet은 미디어 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="5d3dd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5d3dd-109">EXAMPLES</span></span>

### <span data-ttu-id="5d3dd-110">예제 1: 리소스 그룹의 모든 미디어 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3dd-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="5d3dd-111">이 명령은 ResourceGroup001 이라는 리소스 그룹의 모든 미디어 서비스에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="5d3dd-112">예제 2: 미디어 서비스 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d3dd-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="5d3dd-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 MediaService1 이라는 미디어 서비스의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="5d3dd-114">변수</span><span class="sxs-lookup"><span data-stu-id="5d3dd-114">PARAMETERS</span></span>

### <span data-ttu-id="5d3dd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d3dd-115">-AccountName</span></span>
<span data-ttu-id="5d3dd-116">이 cmdlet이 가져오는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3dd-117">-DefaultProfile</span></span>
<span data-ttu-id="5d3dd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d3dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d3dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d3dd-120">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3dd-121">CommonParameters</span></span>
<span data-ttu-id="5d3dd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3dd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3dd-124">입력</span><span class="sxs-lookup"><span data-stu-id="5d3dd-124">INPUTS</span></span>

### <span data-ttu-id="5d3dd-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d3dd-125">System.String</span></span>

## <span data-ttu-id="5d3dd-126">출력</span><span class="sxs-lookup"><span data-stu-id="5d3dd-126">OUTPUTS</span></span>

### <span data-ttu-id="5d3dd-127">PSMediaService (\*).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="5d3dd-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5d3dd-128">NOTES</span></span>

## <span data-ttu-id="5d3dd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d3dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="5d3dd-130">새로운 AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5d3dd-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="5d3dd-131">제거-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5d3dd-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="5d3dd-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5d3dd-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

