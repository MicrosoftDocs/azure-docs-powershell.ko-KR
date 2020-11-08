---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047060"
---
# <span data-ttu-id="75b8f-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="75b8f-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="75b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="75b8f-103">위치에 있는 모든 눈금 단위 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="75b8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75b8f-104">SYNTAX</span></span>

### <span data-ttu-id="75b8f-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="75b8f-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="75b8f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="75b8f-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="75b8f-107">리소스</span><span class="sxs-lookup"><span data-stu-id="75b8f-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="75b8f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="75b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="75b8f-109">위치에 있는 모든 눈금 단위 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="75b8f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="75b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="75b8f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="75b8f-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="75b8f-112">배율 단위에 대 한 정보 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="75b8f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="75b8f-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="75b8f-114">특정 배율 단위에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="75b8f-115">변수</span><span class="sxs-lookup"><span data-stu-id="75b8f-115">PARAMETERS</span></span>

### <span data-ttu-id="75b8f-116">-이름</span><span class="sxs-lookup"><span data-stu-id="75b8f-116">-Name</span></span>
<span data-ttu-id="75b8f-117">눈금 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="75b8f-118">-위치</span><span class="sxs-lookup"><span data-stu-id="75b8f-118">-Location</span></span>
<span data-ttu-id="75b8f-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="75b8f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b8f-120">-ResourceGroupName</span></span>
<span data-ttu-id="75b8f-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="75b8f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75b8f-122">-ResourceId</span></span>
<span data-ttu-id="75b8f-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-123">The resource id.</span></span>

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

### <span data-ttu-id="75b8f-124">-필터</span><span class="sxs-lookup"><span data-stu-id="75b8f-124">-Filter</span></span>
<span data-ttu-id="75b8f-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="75b8f-126">-생략</span><span class="sxs-lookup"><span data-stu-id="75b8f-126">-Skip</span></span>
<span data-ttu-id="75b8f-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="75b8f-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="75b8f-128">-Top</span></span>
<span data-ttu-id="75b8f-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="75b8f-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="75b8f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b8f-131">CommonParameters</span></span>
<span data-ttu-id="75b8f-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75b8f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b8f-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b8f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b8f-134">입력</span><span class="sxs-lookup"><span data-stu-id="75b8f-134">INPUTS</span></span>

## <span data-ttu-id="75b8f-135">출력</span><span class="sxs-lookup"><span data-stu-id="75b8f-135">OUTPUTS</span></span>

### <span data-ttu-id="75b8f-136">ScaleUnit. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="75b8f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="75b8f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="75b8f-137">NOTES</span></span>

## <span data-ttu-id="75b8f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75b8f-138">RELATED LINKS</span></span>