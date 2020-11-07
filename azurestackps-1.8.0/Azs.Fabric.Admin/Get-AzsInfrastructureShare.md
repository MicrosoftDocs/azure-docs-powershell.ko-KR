---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874671"
---
# <span data-ttu-id="e3512-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="e3512-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="e3512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3512-102">SYNOPSIS</span></span>
<span data-ttu-id="e3512-103">특정 위치에 있는 모든 패브릭 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="e3512-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3512-104">SYNTAX</span></span>

### <span data-ttu-id="e3512-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3512-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3512-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e3512-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3512-107">리소스</span><span class="sxs-lookup"><span data-stu-id="e3512-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e3512-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3512-108">DESCRIPTION</span></span>
<span data-ttu-id="e3512-109">특정 위치에 있는 모든 패브릭 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="e3512-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3512-110">EXAMPLES</span></span>

### <span data-ttu-id="e3512-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3512-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="e3512-112">모든 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="e3512-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3512-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="e3512-114">이름을 기반으로 하는 파일 공유를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="e3512-115">변수</span><span class="sxs-lookup"><span data-stu-id="e3512-115">PARAMETERS</span></span>

### <span data-ttu-id="e3512-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e3512-116">-Name</span></span>
<span data-ttu-id="e3512-117">패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="e3512-118">-위치</span><span class="sxs-lookup"><span data-stu-id="e3512-118">-Location</span></span>
<span data-ttu-id="e3512-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e3512-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3512-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3512-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e3512-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3512-122">-ResourceId</span></span>
<span data-ttu-id="e3512-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-123">The resource id.</span></span>

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

### <span data-ttu-id="e3512-124">-필터</span><span class="sxs-lookup"><span data-stu-id="e3512-124">-Filter</span></span>
<span data-ttu-id="e3512-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="e3512-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3512-126">CommonParameters</span></span>
<span data-ttu-id="e3512-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3512-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3512-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3512-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3512-129">입력</span><span class="sxs-lookup"><span data-stu-id="e3512-129">INPUTS</span></span>

## <span data-ttu-id="e3512-130">출력</span><span class="sxs-lookup"><span data-stu-id="e3512-130">OUTPUTS</span></span>

### <span data-ttu-id="e3512-131">Microsoft AzureStack. 관리. a. 관리자. 공유 모델</span><span class="sxs-lookup"><span data-stu-id="e3512-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="e3512-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e3512-132">NOTES</span></span>

## <span data-ttu-id="e3512-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3512-133">RELATED LINKS</span></span>