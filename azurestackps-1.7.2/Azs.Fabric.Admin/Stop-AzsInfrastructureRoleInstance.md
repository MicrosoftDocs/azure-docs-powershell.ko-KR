---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5a63ccb6706f4d43e890b8805af0d00aff350bc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874499"
---
# <span data-ttu-id="27592-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="27592-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="27592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27592-102">SYNOPSIS</span></span>
<span data-ttu-id="27592-103">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27592-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="27592-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27592-104">SYNTAX</span></span>

### <span data-ttu-id="27592-105">PowerOff (기본값)</span><span class="sxs-lookup"><span data-stu-id="27592-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27592-106">리소스</span><span class="sxs-lookup"><span data-stu-id="27592-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27592-107">설명은</span><span class="sxs-lookup"><span data-stu-id="27592-107">DESCRIPTION</span></span>
<span data-ttu-id="27592-108">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27592-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="27592-109">예제의</span><span class="sxs-lookup"><span data-stu-id="27592-109">EXAMPLES</span></span>

### <span data-ttu-id="27592-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27592-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="27592-111">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27592-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="27592-112">변수</span><span class="sxs-lookup"><span data-stu-id="27592-112">PARAMETERS</span></span>

### <span data-ttu-id="27592-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27592-113">-AsJob</span></span>
<span data-ttu-id="27592-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="27592-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="27592-115">-Force</span><span class="sxs-lookup"><span data-stu-id="27592-115">-Force</span></span>
<span data-ttu-id="27592-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27592-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="27592-117">-위치</span><span class="sxs-lookup"><span data-stu-id="27592-117">-Location</span></span>
<span data-ttu-id="27592-118">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="27592-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27592-119">-이름</span><span class="sxs-lookup"><span data-stu-id="27592-119">-Name</span></span>
<span data-ttu-id="27592-120">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27592-120">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27592-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27592-121">-ResourceGroupName</span></span>
<span data-ttu-id="27592-122">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="27592-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27592-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27592-123">-ResourceId</span></span>
<span data-ttu-id="27592-124">인프라 역할 인스턴스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="27592-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="27592-125">-확인</span><span class="sxs-lookup"><span data-stu-id="27592-125">-Confirm</span></span>
<span data-ttu-id="27592-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27592-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27592-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27592-127">-WhatIf</span></span>
<span data-ttu-id="27592-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27592-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27592-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27592-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27592-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27592-130">CommonParameters</span></span>
<span data-ttu-id="27592-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27592-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27592-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27592-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27592-133">입력</span><span class="sxs-lookup"><span data-stu-id="27592-133">INPUTS</span></span>

## <span data-ttu-id="27592-134">출력</span><span class="sxs-lookup"><span data-stu-id="27592-134">OUTPUTS</span></span>

## <span data-ttu-id="27592-135">상속자</span><span class="sxs-lookup"><span data-stu-id="27592-135">NOTES</span></span>

## <span data-ttu-id="27592-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27592-136">RELATED LINKS</span></span>
