---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875146"
---
# <span data-ttu-id="a02ed-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="a02ed-101">Close-AzsAlert</span></span>

## <span data-ttu-id="a02ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a02ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a02ed-103">지정 된 알림을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-103">Closes the given alert.</span></span>

## <span data-ttu-id="a02ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a02ed-104">SYNTAX</span></span>

### <span data-ttu-id="a02ed-105">닫기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a02ed-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a02ed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a02ed-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a02ed-107">리소스</span><span class="sxs-lookup"><span data-stu-id="a02ed-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a02ed-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a02ed-108">DESCRIPTION</span></span>
<span data-ttu-id="a02ed-109">지정 된 알림을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-109">Closes the given alert.</span></span>

## <span data-ttu-id="a02ed-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a02ed-110">EXAMPLES</span></span>

### <span data-ttu-id="a02ed-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a02ed-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="a02ed-112">이름으로 알림을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-112">Close an alert by Name.</span></span>

### <span data-ttu-id="a02ed-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a02ed-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="a02ed-114">파이핑을 통해 경고를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-114">Close an alert through piping.</span></span>

## <span data-ttu-id="a02ed-115">변수</span><span class="sxs-lookup"><span data-stu-id="a02ed-115">PARAMETERS</span></span>

### <span data-ttu-id="a02ed-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a02ed-116">-Name</span></span>
<span data-ttu-id="a02ed-117">경고 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02ed-118">-위치</span><span class="sxs-lookup"><span data-stu-id="a02ed-118">-Location</span></span>
<span data-ttu-id="a02ed-119">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-119">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="a02ed-121">경고의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-121">Resource group name of the alert.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02ed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a02ed-122">-InputObject</span></span>
<span data-ttu-id="a02ed-123">Get-AzsAlert에서 반환 된 알림</span><span class="sxs-lookup"><span data-stu-id="a02ed-123">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a02ed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a02ed-124">-ResourceId</span></span>
<span data-ttu-id="a02ed-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a02ed-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a02ed-126">-Force</span></span>
<span data-ttu-id="a02ed-127">확인을 묻지 않도록 매개 변수를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="a02ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a02ed-128">-WhatIf</span></span>
<span data-ttu-id="a02ed-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a02ed-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a02ed-131">-확인</span><span class="sxs-lookup"><span data-stu-id="a02ed-131">-Confirm</span></span>
<span data-ttu-id="a02ed-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a02ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02ed-133">CommonParameters</span></span>
<span data-ttu-id="a02ed-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a02ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02ed-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a02ed-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02ed-136">입력</span><span class="sxs-lookup"><span data-stu-id="a02ed-136">INPUTS</span></span>

## <span data-ttu-id="a02ed-137">출력</span><span class="sxs-lookup"><span data-stu-id="a02ed-137">OUTPUTS</span></span>

### <span data-ttu-id="a02ed-138">InfrastructureInsights. Alert (관리자 용)</span><span class="sxs-lookup"><span data-stu-id="a02ed-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="a02ed-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a02ed-139">NOTES</span></span>

## <span data-ttu-id="a02ed-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a02ed-140">RELATED LINKS</span></span>