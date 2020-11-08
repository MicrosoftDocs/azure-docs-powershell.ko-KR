---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047152"
---
# <span data-ttu-id="e0472-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="e0472-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="e0472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0472-102">SYNOPSIS</span></span>
<span data-ttu-id="e0472-103">지정 된 행사를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-103">Delete the specified offer.</span></span>

## <span data-ttu-id="e0472-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0472-104">SYNTAX</span></span>

### <span data-ttu-id="e0472-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0472-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0472-106">리소스</span><span class="sxs-lookup"><span data-stu-id="e0472-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0472-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e0472-107">DESCRIPTION</span></span>
<span data-ttu-id="e0472-108">지정 된 행사를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-108">Delete the specified offer.</span></span>

## <span data-ttu-id="e0472-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e0472-109">EXAMPLES</span></span>

### <span data-ttu-id="e0472-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0472-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="e0472-111">지정 된 행사를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-111">Delete the specified offer.</span></span>

## <span data-ttu-id="e0472-112">변수</span><span class="sxs-lookup"><span data-stu-id="e0472-112">PARAMETERS</span></span>

### <span data-ttu-id="e0472-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e0472-113">-Force</span></span>
<span data-ttu-id="e0472-114">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-114">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0472-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e0472-115">-Name</span></span>
<span data-ttu-id="e0472-116">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0472-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0472-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0472-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0472-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0472-119">-ResourceId</span></span>
<span data-ttu-id="e0472-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-120">The resource id.</span></span>

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

### <span data-ttu-id="e0472-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e0472-121">-Confirm</span></span>
<span data-ttu-id="e0472-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0472-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0472-123">-WhatIf</span></span>
<span data-ttu-id="e0472-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0472-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0472-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0472-126">CommonParameters</span></span>
<span data-ttu-id="e0472-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0472-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0472-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0472-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0472-129">입력</span><span class="sxs-lookup"><span data-stu-id="e0472-129">INPUTS</span></span>

## <span data-ttu-id="e0472-130">출력</span><span class="sxs-lookup"><span data-stu-id="e0472-130">OUTPUTS</span></span>

## <span data-ttu-id="e0472-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e0472-131">NOTES</span></span>

## <span data-ttu-id="e0472-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0472-132">RELATED LINKS</span></span>
