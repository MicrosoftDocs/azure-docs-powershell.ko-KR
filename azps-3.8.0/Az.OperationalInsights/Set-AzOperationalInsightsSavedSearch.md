---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 441e27692c0f61f040feb7ca01e7f2514fc72320
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047283"
---
# <span data-ttu-id="1be59-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="1be59-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="1be59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1be59-102">SYNOPSIS</span></span>
<span data-ttu-id="1be59-103">이미 존재 하는 저장 된 검색을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="1be59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1be59-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1be59-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1be59-105">DESCRIPTION</span></span>
<span data-ttu-id="1be59-106">**Set-AzOperationalInsightsSavedSearch** cmdlet은 이미 존재 하는 저장 된 검색을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="1be59-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1be59-107">EXAMPLES</span></span>

### <span data-ttu-id="1be59-108">예제 1: 업데이트 된 속성을 사용 하 여 저장 된 검색 설정</span><span class="sxs-lookup"><span data-stu-id="1be59-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="1be59-109">이 명령은 업데이트 된 속성을 사용 하 여 저장 한 검색을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="1be59-110">변수</span><span class="sxs-lookup"><span data-stu-id="1be59-110">PARAMETERS</span></span>

### <span data-ttu-id="1be59-111">-범주</span><span class="sxs-lookup"><span data-stu-id="1be59-111">-Category</span></span>
<span data-ttu-id="1be59-112">범주 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be59-113">-DefaultProfile</span></span>
<span data-ttu-id="1be59-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1be59-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1be59-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1be59-115">-DisplayName</span></span>
<span data-ttu-id="1be59-116">표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="1be59-117">-ETag</span></span>
<span data-ttu-id="1be59-118">ETag 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-119">-쿼리</span><span class="sxs-lookup"><span data-stu-id="1be59-119">-Query</span></span>
<span data-ttu-id="1be59-120">쿼리 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-120">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be59-121">-ResourceGroupName</span></span>
<span data-ttu-id="1be59-122">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="1be59-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1be59-123">-SavedSearchId</span></span>
<span data-ttu-id="1be59-124">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-124">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-125">태그</span><span class="sxs-lookup"><span data-stu-id="1be59-125">-Tag</span></span>
<span data-ttu-id="1be59-126">저장 된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-126">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-127">-버전</span><span class="sxs-lookup"><span data-stu-id="1be59-127">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1be59-128">-WorkspaceName</span></span>
<span data-ttu-id="1be59-129">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-129">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be59-130">CommonParameters</span></span>
<span data-ttu-id="1be59-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1be59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be59-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1be59-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be59-133">입력</span><span class="sxs-lookup"><span data-stu-id="1be59-133">INPUTS</span></span>

### <span data-ttu-id="1be59-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1be59-134">System.String</span></span>

### <span data-ttu-id="1be59-135">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1be59-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1be59-136">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="1be59-136">System.Int64</span></span>

## <span data-ttu-id="1be59-137">출력</span><span class="sxs-lookup"><span data-stu-id="1be59-137">OUTPUTS</span></span>

### <span data-ttu-id="1be59-138">System .Net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="1be59-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="1be59-139">상속자</span><span class="sxs-lookup"><span data-stu-id="1be59-139">NOTES</span></span>

## <span data-ttu-id="1be59-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1be59-140">RELATED LINKS</span></span>

[<span data-ttu-id="1be59-141">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1be59-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

