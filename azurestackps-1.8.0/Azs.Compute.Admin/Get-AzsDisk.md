---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874717"
---
# <span data-ttu-id="0ab68-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="0ab68-101">Get-AzsDisk</span></span>

## <span data-ttu-id="0ab68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ab68-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab68-103">지정 된 공유에서 마이그레이션될 수 있는 관리 디스크의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="0ab68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ab68-104">SYNTAX</span></span>

### <span data-ttu-id="0ab68-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ab68-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="0ab68-106">리소스</span><span class="sxs-lookup"><span data-stu-id="0ab68-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="0ab68-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="0ab68-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="0ab68-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0ab68-108">DESCRIPTION</span></span>
<span data-ttu-id="0ab68-109">디스크 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-109">Returns a list of disks.</span></span>

## <span data-ttu-id="0ab68-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0ab68-110">EXAMPLES</span></span>

### <span data-ttu-id="0ab68-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ab68-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="0ab68-112">로컬 위치에 있는 관리 디스크의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="0ab68-113">기본적으로 첫 번째 100 디스크를 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="0ab68-114">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ab68-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="0ab68-115">특정 관리 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="0ab68-116">변수</span><span class="sxs-lookup"><span data-stu-id="0ab68-116">PARAMETERS</span></span>

### <span data-ttu-id="0ab68-117">-카운트</span><span class="sxs-lookup"><span data-stu-id="0ab68-117">-Count</span></span>
<span data-ttu-id="0ab68-118">반환할 최대 디스크 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab68-119">-위치</span><span class="sxs-lookup"><span data-stu-id="0ab68-119">-Location</span></span>
<span data-ttu-id="0ab68-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-120">Location of the resource.</span></span>

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

### <span data-ttu-id="0ab68-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0ab68-121">-Name</span></span>
<span data-ttu-id="0ab68-122">Id 인 디스크 guid입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab68-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ab68-123">-ResourceId</span></span>
<span data-ttu-id="0ab68-124">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ab68-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="0ab68-125">-SharePath</span></span>
<span data-ttu-id="0ab68-126">리소스가 속한 원본 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="0ab68-127">-시작</span><span class="sxs-lookup"><span data-stu-id="0ab68-127">-Start</span></span>
<span data-ttu-id="0ab68-128">Query의 디스크 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab68-129">-상태</span><span class="sxs-lookup"><span data-stu-id="0ab68-129">-Status</span></span>
<span data-ttu-id="0ab68-130">디스크 상태의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="0ab68-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ab68-131">-UserSubscriptionId</span></span>
<span data-ttu-id="0ab68-132">리소스가 속한 테 넌 트 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="0ab68-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab68-133">CommonParameters</span></span>
<span data-ttu-id="0ab68-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ab68-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab68-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab68-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab68-136">입력</span><span class="sxs-lookup"><span data-stu-id="0ab68-136">INPUTS</span></span>

## <span data-ttu-id="0ab68-137">출력</span><span class="sxs-lookup"><span data-stu-id="0ab68-137">OUTPUTS</span></span>

### <span data-ttu-id="0ab68-138">Microsoft AzureStack. 관리자. m a. 관리.</span><span class="sxs-lookup"><span data-stu-id="0ab68-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="0ab68-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0ab68-139">NOTES</span></span>

## <span data-ttu-id="0ab68-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ab68-140">RELATED LINKS</span></span>
