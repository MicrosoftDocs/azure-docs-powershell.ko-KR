---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046605"
---
# <span data-ttu-id="3053e-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="3053e-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="3053e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3053e-102">SYNOPSIS</span></span>
<span data-ttu-id="3053e-103">위치에 있는 모든 논리 네트워크의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="3053e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3053e-104">SYNTAX</span></span>

### <span data-ttu-id="3053e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3053e-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3053e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="3053e-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3053e-107">리소스</span><span class="sxs-lookup"><span data-stu-id="3053e-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3053e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3053e-108">DESCRIPTION</span></span>
<span data-ttu-id="3053e-109">위치에 있는 모든 논리 네트워크의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="3053e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3053e-110">EXAMPLES</span></span>

### <span data-ttu-id="3053e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3053e-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="3053e-112">위치에 있는 모든 논리 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="3053e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3053e-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="3053e-114">이름을 기반으로 특정 논리 네트워크 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="3053e-115">변수</span><span class="sxs-lookup"><span data-stu-id="3053e-115">PARAMETERS</span></span>

### <span data-ttu-id="3053e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="3053e-116">-Name</span></span>
<span data-ttu-id="3053e-117">논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-117">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-118">-위치</span><span class="sxs-lookup"><span data-stu-id="3053e-118">-Location</span></span>
<span data-ttu-id="3053e-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3053e-120">-ResourceGroupName</span></span>
<span data-ttu-id="3053e-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-121">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3053e-122">-ResourceId</span></span>
<span data-ttu-id="3053e-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-124">-필터</span><span class="sxs-lookup"><span data-stu-id="3053e-124">-Filter</span></span>
<span data-ttu-id="3053e-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-126">-생략</span><span class="sxs-lookup"><span data-stu-id="3053e-126">-Skip</span></span>
<span data-ttu-id="3053e-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="3053e-128">-Top</span></span>
<span data-ttu-id="3053e-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3053e-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3053e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3053e-131">CommonParameters</span></span>
<span data-ttu-id="3053e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3053e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3053e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3053e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3053e-134">입력</span><span class="sxs-lookup"><span data-stu-id="3053e-134">INPUTS</span></span>

## <span data-ttu-id="3053e-135">출력</span><span class="sxs-lookup"><span data-stu-id="3053e-135">OUTPUTS</span></span>

### <span data-ttu-id="3053e-136">LogicalNetwork. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="3053e-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="3053e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="3053e-137">NOTES</span></span>

## <span data-ttu-id="3053e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3053e-138">RELATED LINKS</span></span>