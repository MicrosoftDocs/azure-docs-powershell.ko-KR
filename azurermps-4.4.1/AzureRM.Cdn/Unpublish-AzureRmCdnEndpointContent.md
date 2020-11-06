---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a774aec8114883d3ba2a5edf189f115f99d3eb4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531158"
---
# <span data-ttu-id="0f0d5-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="0f0d5-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="0f0d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f0d5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0d5-103">CDN 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f0d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f0d5-104">SYNTAX</span></span>

### <span data-ttu-id="0f0d5-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0f0d5-105">Parameter Set for fields parameters (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f0d5-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0f0d5-106">Parameter Set for object parameters</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f0d5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0f0d5-107">DESCRIPTION</span></span>
<span data-ttu-id="0f0d5-108">**AzureRmCdnEndpointContent** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점에서 콘텐츠를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0f0d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0f0d5-109">EXAMPLES</span></span>

## <span data-ttu-id="0f0d5-110">변수</span><span class="sxs-lookup"><span data-stu-id="0f0d5-110">PARAMETERS</span></span>

### <span data-ttu-id="0f0d5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f0d5-111">-CdnEndpoint</span></span>
<span data-ttu-id="0f0d5-112">이 cmdlet이 제거 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0d5-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0f0d5-113">-EndpointName</span></span>
<span data-ttu-id="0f0d5-114">이 cmdlet이 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-114">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0d5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f0d5-115">-PassThru</span></span>
<span data-ttu-id="0f0d5-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f0d5-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f0d5-118">-/Profile</span><span class="sxs-lookup"><span data-stu-id="0f0d5-118">-ProfileName</span></span>
<span data-ttu-id="0f0d5-119">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0d5-120">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="0f0d5-120">-PurgeContent</span></span>
<span data-ttu-id="0f0d5-121">이 cmdlet이 제거 하는 원본 서버의 콘텐츠에 대 한 상대 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-121">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="0f0d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f0d5-123">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0d5-124">-확인</span><span class="sxs-lookup"><span data-stu-id="0f0d5-124">-Confirm</span></span>
<span data-ttu-id="0f0d5-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0d5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f0d5-126">-WhatIf</span></span>
<span data-ttu-id="0f0d5-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f0d5-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0d5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0d5-129">-DefaultProfile</span></span>
<span data-ttu-id="0f0d5-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f0d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0d5-131">CommonParameters</span></span>
<span data-ttu-id="0f0d5-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0d5-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f0d5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0d5-134">입력</span><span class="sxs-lookup"><span data-stu-id="0f0d5-134">INPUTS</span></span>

### <span data-ttu-id="0f0d5-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f0d5-135">PSEndpoint</span></span>
<span data-ttu-id="0f0d5-136">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f0d5-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="0f0d5-137">출력</span><span class="sxs-lookup"><span data-stu-id="0f0d5-137">OUTPUTS</span></span>

### <span data-ttu-id="0f0d5-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0f0d5-138">System.Boolean</span></span>

## <span data-ttu-id="0f0d5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0f0d5-139">NOTES</span></span>

## <span data-ttu-id="0f0d5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f0d5-140">RELATED LINKS</span></span>

[<span data-ttu-id="0f0d5-141">게시-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="0f0d5-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)

