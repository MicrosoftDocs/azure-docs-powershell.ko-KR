---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212899"
---
# <span data-ttu-id="6a567-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="6a567-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="6a567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a567-102">SYNOPSIS</span></span>
<span data-ttu-id="6a567-103">사용자 지정 도메인 HTTPS (사용 되지 않음)를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="6a567-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a567-104">SYNTAX</span></span>

### <span data-ttu-id="6a567-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a567-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a567-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a567-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a567-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6a567-107">DESCRIPTION</span></span>
<span data-ttu-id="6a567-108">AzCdnCustomDomain cmdlet을 **사용** 하면 CDN 사용자 지정 도메인의 보안 HTTPS 배달을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="6a567-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6a567-109">EXAMPLES</span></span>

### <span data-ttu-id="6a567-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a567-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="6a567-111">사용자 지정 도메인의 https 배달을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="6a567-112">변수</span><span class="sxs-lookup"><span data-stu-id="6a567-112">PARAMETERS</span></span>

### <span data-ttu-id="6a567-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="6a567-113">-CustomDomainName</span></span>
<span data-ttu-id="6a567-114">Azure CDN 사용자 지정 도메인 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="6a567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a567-115">-DefaultProfile</span></span>
<span data-ttu-id="6a567-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a567-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6a567-117">-EndpointName</span></span>
<span data-ttu-id="6a567-118">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6a567-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a567-119">-InputObject</span></span>
<span data-ttu-id="6a567-120">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a567-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a567-121">-PassThru</span></span>
<span data-ttu-id="6a567-122">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a567-123">-/Profile</span><span class="sxs-lookup"><span data-stu-id="6a567-123">-ProfileName</span></span>
<span data-ttu-id="6a567-124">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="6a567-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a567-125">-ResourceGroupName</span></span>
<span data-ttu-id="6a567-126">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="6a567-127">-확인</span><span class="sxs-lookup"><span data-stu-id="6a567-127">-Confirm</span></span>
<span data-ttu-id="6a567-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a567-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a567-129">-WhatIf</span></span>
<span data-ttu-id="6a567-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a567-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a567-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a567-132">CommonParameters</span></span>
<span data-ttu-id="6a567-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a567-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a567-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a567-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a567-135">입력</span><span class="sxs-lookup"><span data-stu-id="6a567-135">INPUTS</span></span>

### <span data-ttu-id="6a567-136">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="6a567-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="6a567-137">출력</span><span class="sxs-lookup"><span data-stu-id="6a567-137">OUTPUTS</span></span>

### <span data-ttu-id="6a567-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6a567-138">System.Boolean</span></span>

## <span data-ttu-id="6a567-139">상속자</span><span class="sxs-lookup"><span data-stu-id="6a567-139">NOTES</span></span>

## <span data-ttu-id="6a567-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a567-140">RELATED LINKS</span></span>