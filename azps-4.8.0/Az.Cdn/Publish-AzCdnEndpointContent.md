---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049141"
---
# <span data-ttu-id="26f30-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="26f30-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="26f30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f30-102">SYNOPSIS</span></span>
<span data-ttu-id="26f30-103">끝점에 콘텐츠를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="26f30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26f30-104">SYNTAX</span></span>

### <span data-ttu-id="26f30-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="26f30-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26f30-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f30-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26f30-107">설명은</span><span class="sxs-lookup"><span data-stu-id="26f30-107">DESCRIPTION</span></span>
<span data-ttu-id="26f30-108">**AzCdnEndpointContent** CMDLET은 CDN (콘텐츠 배달 네트워크) 끝점에 대 한 원본 서버에서 콘텐츠를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="26f30-109">예제의</span><span class="sxs-lookup"><span data-stu-id="26f30-109">EXAMPLES</span></span>

## <span data-ttu-id="26f30-110">변수</span><span class="sxs-lookup"><span data-stu-id="26f30-110">PARAMETERS</span></span>

### <span data-ttu-id="26f30-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="26f30-111">-CdnEndpoint</span></span>
<span data-ttu-id="26f30-112">CDN 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-112">Specifies the CDN endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26f30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f30-113">-DefaultProfile</span></span>
<span data-ttu-id="26f30-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26f30-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26f30-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="26f30-115">-EndpointName</span></span>
<span data-ttu-id="26f30-116">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-116">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f30-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="26f30-117">-LoadContent</span></span>
<span data-ttu-id="26f30-118">이 cmdlet이 게시 하는 원본 서버의 콘텐츠에 대 한 상대 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f30-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26f30-119">-PassThru</span></span>
<span data-ttu-id="26f30-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26f30-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26f30-122">-/Profile</span><span class="sxs-lookup"><span data-stu-id="26f30-122">-ProfileName</span></span>
<span data-ttu-id="26f30-123">원본 서버가 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-123">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f30-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f30-124">-ResourceGroupName</span></span>
<span data-ttu-id="26f30-125">원본 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f30-126">CommonParameters</span></span>
<span data-ttu-id="26f30-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f30-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26f30-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f30-129">입력</span><span class="sxs-lookup"><span data-stu-id="26f30-129">INPUTS</span></span>

### <span data-ttu-id="26f30-130">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="26f30-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="26f30-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="26f30-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26f30-132">출력</span><span class="sxs-lookup"><span data-stu-id="26f30-132">OUTPUTS</span></span>

### <span data-ttu-id="26f30-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="26f30-133">System.Boolean</span></span>

## <span data-ttu-id="26f30-134">상속자</span><span class="sxs-lookup"><span data-stu-id="26f30-134">NOTES</span></span>

## <span data-ttu-id="26f30-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26f30-135">RELATED LINKS</span></span>

[<span data-ttu-id="26f30-136">게시 취소-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="26f30-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)

