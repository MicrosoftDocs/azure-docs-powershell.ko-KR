---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873964"
---
# <span data-ttu-id="78e8e-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="78e8e-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="78e8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="78e8e-103">관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="78e8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78e8e-104">SYNTAX</span></span>

### <span data-ttu-id="78e8e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="78e8e-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="78e8e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="78e8e-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="78e8e-107">가져오기</span><span class="sxs-lookup"><span data-stu-id="78e8e-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="78e8e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="78e8e-108">DESCRIPTION</span></span>
<span data-ttu-id="78e8e-109">디스크 마이그레이션 작업 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="78e8e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="78e8e-110">EXAMPLES</span></span>

### <span data-ttu-id="78e8e-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="78e8e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="78e8e-112">특정 관리 디스크 마이그레이션 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="78e8e-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="78e8e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="78e8e-114">로컬 위치에서 관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="78e8e-115">변수</span><span class="sxs-lookup"><span data-stu-id="78e8e-115">PARAMETERS</span></span>

### <span data-ttu-id="78e8e-116">-위치</span><span class="sxs-lookup"><span data-stu-id="78e8e-116">-Location</span></span>
<span data-ttu-id="78e8e-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-117">Location of the resource.</span></span>

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

### <span data-ttu-id="78e8e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="78e8e-118">-Name</span></span>
<span data-ttu-id="78e8e-119">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78e8e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78e8e-120">-ResourceId</span></span>
<span data-ttu-id="78e8e-121">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-121">The resource id.</span></span>

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

### <span data-ttu-id="78e8e-122">-상태</span><span class="sxs-lookup"><span data-stu-id="78e8e-122">-Status</span></span>
<span data-ttu-id="78e8e-123">디스크 마이그레이션 작업 상태의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="78e8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e8e-124">CommonParameters</span></span>
<span data-ttu-id="78e8e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78e8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e8e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78e8e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e8e-127">입력</span><span class="sxs-lookup"><span data-stu-id="78e8e-127">INPUTS</span></span>

## <span data-ttu-id="78e8e-128">출력</span><span class="sxs-lookup"><span data-stu-id="78e8e-128">OUTPUTS</span></span>

### <span data-ttu-id="78e8e-129">DiskMigrationJob의. 관리자. 관리.</span><span class="sxs-lookup"><span data-stu-id="78e8e-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="78e8e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="78e8e-130">NOTES</span></span>

## <span data-ttu-id="78e8e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78e8e-131">RELATED LINKS</span></span>
