---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 1345978ac502d0c7d576b56f720bd16ca704e062
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873419"
---
# <span data-ttu-id="d7580-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d7580-101">Split-AzReservation</span></span>

## <span data-ttu-id="d7580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7580-102">SYNOPSIS</span></span>
<span data-ttu-id="d7580-103">분할 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d7580-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="d7580-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7580-104">SYNTAX</span></span>

### <span data-ttu-id="d7580-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d7580-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7580-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d7580-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7580-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d7580-107">DESCRIPTION</span></span>
<span data-ttu-id="d7580-108">지정 된 `Reservation` `Reservation` 수량 분포를 사용 하 여 a를 2 개의 s로 나눕니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="d7580-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d7580-109">EXAMPLES</span></span>

### <span data-ttu-id="d7580-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7580-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="d7580-111">지정 된을 `Reservation` 해당 수량의 2 s로 나눕니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d7580-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="d7580-112">변수</span><span class="sxs-lookup"><span data-stu-id="d7580-112">PARAMETERS</span></span>

### <span data-ttu-id="d7580-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7580-113">-DefaultProfile</span></span>
<span data-ttu-id="d7580-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-115">-수량</span><span class="sxs-lookup"><span data-stu-id="d7580-115">-Quantity</span></span>
<span data-ttu-id="d7580-116">2 s의 수량 필드에 대해 쉼표로 구분 된 정수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d7580-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-117">-예약</span><span class="sxs-lookup"><span data-stu-id="d7580-117">-Reservation</span></span>
<span data-ttu-id="d7580-118">파이프 개체 매개 변수 `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d7580-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d7580-119">-ReservationId</span></span>
<span data-ttu-id="d7580-120">분할할의 Id입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d7580-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d7580-121">-ReservationOrderId</span></span>
<span data-ttu-id="d7580-122">`ReservationOrder` `Reservation` 해당 사용자에 게 나누려는의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-123">-확인</span><span class="sxs-lookup"><span data-stu-id="d7580-123">-Confirm</span></span>
<span data-ttu-id="d7580-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7580-125">-WhatIf</span></span>
<span data-ttu-id="d7580-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7580-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7580-128">CommonParameters</span></span>
<span data-ttu-id="d7580-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7580-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7580-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7580-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7580-131">입력</span><span class="sxs-lookup"><span data-stu-id="d7580-131">INPUTS</span></span>

### <span data-ttu-id="d7580-132">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d7580-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d7580-133">출력</span><span class="sxs-lookup"><span data-stu-id="d7580-133">OUTPUTS</span></span>

### <span data-ttu-id="d7580-134">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="d7580-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d7580-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d7580-135">NOTES</span></span>

## <span data-ttu-id="d7580-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7580-136">RELATED LINKS</span></span>