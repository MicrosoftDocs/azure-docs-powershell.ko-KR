---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874821"
---
# <span data-ttu-id="326b9-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="326b9-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="326b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="326b9-102">SYNOPSIS</span></span>
<span data-ttu-id="326b9-103">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="326b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="326b9-104">SYNTAX</span></span>

### <span data-ttu-id="326b9-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="326b9-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="326b9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="326b9-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="326b9-107">리소스</span><span class="sxs-lookup"><span data-stu-id="326b9-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="326b9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="326b9-108">DESCRIPTION</span></span>
<span data-ttu-id="326b9-109">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="326b9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="326b9-110">EXAMPLES</span></span>

### <span data-ttu-id="326b9-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="326b9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="326b9-112">현재 구독 및 지정 된 리소스 그룹 이름 아래에 있는 모든 디렉터리 테 넌 트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="326b9-113">변수</span><span class="sxs-lookup"><span data-stu-id="326b9-113">PARAMETERS</span></span>

### <span data-ttu-id="326b9-114">-이름</span><span class="sxs-lookup"><span data-stu-id="326b9-114">-Name</span></span>
<span data-ttu-id="326b9-115">디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-115">Directory tenant name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326b9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326b9-116">-ResourceGroupName</span></span>
<span data-ttu-id="326b9-117">{{Fill ResourceGroupName Description}}</span><span class="sxs-lookup"><span data-stu-id="326b9-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="326b9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="326b9-118">-ResourceId</span></span>
<span data-ttu-id="326b9-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-119">The resource id.</span></span>

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

### <span data-ttu-id="326b9-120">-생략</span><span class="sxs-lookup"><span data-stu-id="326b9-120">-Skip</span></span>
<span data-ttu-id="326b9-121">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="326b9-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="326b9-122">-Top</span></span>
<span data-ttu-id="326b9-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="326b9-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="326b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326b9-125">CommonParameters</span></span>
<span data-ttu-id="326b9-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="326b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326b9-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="326b9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326b9-128">입력</span><span class="sxs-lookup"><span data-stu-id="326b9-128">INPUTS</span></span>

## <span data-ttu-id="326b9-129">출력</span><span class="sxs-lookup"><span data-stu-id="326b9-129">OUTPUTS</span></span>

### <span data-ttu-id="326b9-130">Microsoft AzureStack. 관리. DirectoryTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="326b9-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="326b9-131">상속자</span><span class="sxs-lookup"><span data-stu-id="326b9-131">NOTES</span></span>

## <span data-ttu-id="326b9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="326b9-132">RELATED LINKS</span></span>
