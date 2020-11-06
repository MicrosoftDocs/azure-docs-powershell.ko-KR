---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529167"
---
# <span data-ttu-id="bc6bd-101">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bc6bd-101">Find-AzureRmResourceGroup</span></span>

## <span data-ttu-id="bc6bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6bd-103">리소스 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-103">Searches for resource groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc6bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc6bd-104">SYNTAX</span></span>

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc6bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc6bd-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6bd-106">**Find-AzureRmResourceGroup** cmdlet은 지정 된 매개 변수를 사용 하 여 리소스 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-106">The **Find-AzureRmResourceGroup** cmdlet searches for resource groups using the specified parameters.</span></span>

## <span data-ttu-id="bc6bd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc6bd-107">EXAMPLES</span></span>

### <span data-ttu-id="bc6bd-108">예제 1: 모든 리소스 그룹 찾기</span><span class="sxs-lookup"><span data-stu-id="bc6bd-108">Example 1: Find all resource groups</span></span>
```
PS C:\>Find-AzureRmResourceGroup
```

<span data-ttu-id="bc6bd-109">이 명령은 모든 리소스 그룹을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-109">This command finds all resource groups.</span></span>

### <span data-ttu-id="bc6bd-110">예제 2: 태그별 이름으로 리소스 그룹 찾기</span><span class="sxs-lookup"><span data-stu-id="bc6bd-110">Example 2: Find resource groups by tag name</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

<span data-ttu-id="bc6bd-111">이 명령은 testtag 라는 태그가 있는 모든 리소스 그룹을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-111">This command finds all resource groups that have a tag named testtag.</span></span>

### <span data-ttu-id="bc6bd-112">예제 3: 태그 이름 및 값을 기준으로 리소스 그룹 찾기</span><span class="sxs-lookup"><span data-stu-id="bc6bd-112">Example 3: Find resource groups by tag name and value</span></span>
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

<span data-ttu-id="bc6bd-113">이 명령은 testtag 이라는 태그와 testtag 값이 있는 모든 리소스 그룹을 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-113">This command finds all resource groups that have a tag named testtag and the value testval.</span></span>

## <span data-ttu-id="bc6bd-114">변수</span><span class="sxs-lookup"><span data-stu-id="bc6bd-114">PARAMETERS</span></span>

### <span data-ttu-id="bc6bd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc6bd-115">-ApiVersion</span></span>
<span data-ttu-id="bc6bd-116">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-116">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="bc6bd-117">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bc6bd-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="bc6bd-118">-Pre</span></span>
<span data-ttu-id="bc6bd-119">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bc6bd-120">태그</span><span class="sxs-lookup"><span data-stu-id="bc6bd-120">-Tag</span></span>
<span data-ttu-id="bc6bd-121">결과를 필터링 하는 해시 테이블로 태그 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-121">Specifies tag information, as a hash table, to filter your results.</span></span> <span data-ttu-id="bc6bd-122">다음과 같은 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-122">Use the following formats:</span></span>

<span data-ttu-id="bc6bd-123">@ {tagName = $null} 또는 @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-123">@{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc6bd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6bd-124">-DefaultProfile</span></span>
<span data-ttu-id="bc6bd-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc6bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6bd-126">CommonParameters</span></span>
<span data-ttu-id="bc6bd-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc6bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6bd-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc6bd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6bd-129">입력</span><span class="sxs-lookup"><span data-stu-id="bc6bd-129">INPUTS</span></span>

## <span data-ttu-id="bc6bd-130">출력</span><span class="sxs-lookup"><span data-stu-id="bc6bd-130">OUTPUTS</span></span>

### <span data-ttu-id="bc6bd-131">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="bc6bd-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bc6bd-132">상속자</span><span class="sxs-lookup"><span data-stu-id="bc6bd-132">NOTES</span></span>

## <span data-ttu-id="bc6bd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc6bd-133">RELATED LINKS</span></span>
