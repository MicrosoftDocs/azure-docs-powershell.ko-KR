---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874756"
---
# <span data-ttu-id="f8f99-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f8f99-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="f8f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f99-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f99-103">인프라 역할 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="f8f99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8f99-104">SYNTAX</span></span>

### <span data-ttu-id="f8f99-105">시스템 종료 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8f99-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8f99-106">리소스</span><span class="sxs-lookup"><span data-stu-id="f8f99-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8f99-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f8f99-107">DESCRIPTION</span></span>
<span data-ttu-id="f8f99-108">인프라 역할 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="f8f99-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f8f99-109">EXAMPLES</span></span>

### <span data-ttu-id="f8f99-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8f99-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="f8f99-111">인프라 역할 인스턴스를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="f8f99-112">오류가 발생 하면 예외가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="f8f99-113">변수</span><span class="sxs-lookup"><span data-stu-id="f8f99-113">PARAMETERS</span></span>

### <span data-ttu-id="f8f99-114">-이름</span><span class="sxs-lookup"><span data-stu-id="f8f99-114">-Name</span></span>
<span data-ttu-id="f8f99-115">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f99-116">-위치</span><span class="sxs-lookup"><span data-stu-id="f8f99-116">-Location</span></span>
<span data-ttu-id="f8f99-117">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f99-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f99-118">-ResourceGroupName</span></span>
<span data-ttu-id="f8f99-119">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f99-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8f99-120">-ResourceId</span></span>
<span data-ttu-id="f8f99-121">인프라 역할 인스턴스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="f8f99-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8f99-122">-AsJob</span></span>
<span data-ttu-id="f8f99-123">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f8f99-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f8f99-124">-Force</span></span>
<span data-ttu-id="f8f99-125">확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="f8f99-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="f8f99-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8f99-126">-WhatIf</span></span>
<span data-ttu-id="f8f99-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8f99-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8f99-129">-확인</span><span class="sxs-lookup"><span data-stu-id="f8f99-129">-Confirm</span></span>
<span data-ttu-id="f8f99-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8f99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f99-131">CommonParameters</span></span>
<span data-ttu-id="f8f99-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f99-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f99-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f99-134">입력</span><span class="sxs-lookup"><span data-stu-id="f8f99-134">INPUTS</span></span>

## <span data-ttu-id="f8f99-135">출력</span><span class="sxs-lookup"><span data-stu-id="f8f99-135">OUTPUTS</span></span>

## <span data-ttu-id="f8f99-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f8f99-136">NOTES</span></span>

## <span data-ttu-id="f8f99-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8f99-137">RELATED LINKS</span></span>