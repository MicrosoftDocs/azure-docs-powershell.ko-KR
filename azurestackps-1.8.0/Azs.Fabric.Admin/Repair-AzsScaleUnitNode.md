---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874647"
---
# <span data-ttu-id="063b6-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="063b6-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="063b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="063b6-102">SYNOPSIS</span></span>
<span data-ttu-id="063b6-103">클러스터의 노드를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="063b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="063b6-104">SYNTAX</span></span>

### <span data-ttu-id="063b6-105">복구 (기본값)</span><span class="sxs-lookup"><span data-stu-id="063b6-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="063b6-106">리소스</span><span class="sxs-lookup"><span data-stu-id="063b6-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="063b6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="063b6-107">DESCRIPTION</span></span>
<span data-ttu-id="063b6-108">클러스터의 노드를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="063b6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="063b6-109">EXAMPLES</span></span>

### <span data-ttu-id="063b6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="063b6-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="063b6-111">배율 단위 노드를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="063b6-112">변수</span><span class="sxs-lookup"><span data-stu-id="063b6-112">PARAMETERS</span></span>

### <span data-ttu-id="063b6-113">-이름</span><span class="sxs-lookup"><span data-stu-id="063b6-113">-Name</span></span>
<span data-ttu-id="063b6-114">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063b6-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="063b6-115">-BMCIPv4Address</span></span>
<span data-ttu-id="063b6-116">물리적 컴퓨터의 BMC 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063b6-117">-위치</span><span class="sxs-lookup"><span data-stu-id="063b6-117">-Location</span></span>
<span data-ttu-id="063b6-118">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="063b6-120">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063b6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="063b6-121">-ResourceId</span></span>
<span data-ttu-id="063b6-122">배율 단위 노드 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="063b6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="063b6-123">-AsJob</span></span>
<span data-ttu-id="063b6-124">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="063b6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="063b6-125">-Force</span></span>
<span data-ttu-id="063b6-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="063b6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="063b6-127">-WhatIf</span></span>
<span data-ttu-id="063b6-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="063b6-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="063b6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="063b6-130">-Confirm</span></span>
<span data-ttu-id="063b6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="063b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063b6-132">CommonParameters</span></span>
<span data-ttu-id="063b6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="063b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063b6-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="063b6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063b6-135">입력</span><span class="sxs-lookup"><span data-stu-id="063b6-135">INPUTS</span></span>

## <span data-ttu-id="063b6-136">출력</span><span class="sxs-lookup"><span data-stu-id="063b6-136">OUTPUTS</span></span>

## <span data-ttu-id="063b6-137">상속자</span><span class="sxs-lookup"><span data-stu-id="063b6-137">NOTES</span></span>

## <span data-ttu-id="063b6-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="063b6-138">RELATED LINKS</span></span>