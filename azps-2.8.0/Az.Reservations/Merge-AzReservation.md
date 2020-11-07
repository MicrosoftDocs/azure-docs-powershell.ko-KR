---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 8974a8a0bf8230b630a848e922527bc0b08bdb02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871897"
---
# <span data-ttu-id="02320-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="02320-101">Merge-AzReservation</span></span>

## <span data-ttu-id="02320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02320-102">SYNOPSIS</span></span>
<span data-ttu-id="02320-103">두 개의 `Reservation` s를 병합 합니다.</span><span class="sxs-lookup"><span data-stu-id="02320-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="02320-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02320-104">SYNTAX</span></span>

### <span data-ttu-id="02320-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="02320-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02320-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="02320-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02320-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02320-107">DESCRIPTION</span></span>
<span data-ttu-id="02320-108">지정 된 `Reservation` s를 새에 병합 `Reservation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="02320-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="02320-109">`Reservation`병합 되는 두 s의 속성은 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="02320-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="02320-110">예제의</span><span class="sxs-lookup"><span data-stu-id="02320-110">EXAMPLES</span></span>

### <span data-ttu-id="02320-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="02320-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="02320-112">지정 된 두 s를 하나로 병합 합니다. `Reservation``Reservation`</span><span class="sxs-lookup"><span data-stu-id="02320-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="02320-113">변수</span><span class="sxs-lookup"><span data-stu-id="02320-113">PARAMETERS</span></span>

### <span data-ttu-id="02320-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02320-114">-DefaultProfile</span></span>
<span data-ttu-id="02320-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02320-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02320-116">-예약</span><span class="sxs-lookup"><span data-stu-id="02320-116">-Reservation</span></span>
<span data-ttu-id="02320-117">결합할 두 ReservationIds의 쉼표로 구분 된 문자열</span><span class="sxs-lookup"><span data-stu-id="02320-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02320-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="02320-118">-ReservationId</span></span>
<span data-ttu-id="02320-119">`ReservationOrder`2 s이 (가) 포함 된에 대 한 ReservationOrderId `Reservation`</span><span class="sxs-lookup"><span data-stu-id="02320-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02320-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="02320-120">-ReservationOrderId</span></span>
<span data-ttu-id="02320-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="02320-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="02320-122">-확인</span><span class="sxs-lookup"><span data-stu-id="02320-122">-Confirm</span></span>
<span data-ttu-id="02320-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02320-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02320-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02320-124">-WhatIf</span></span>
<span data-ttu-id="02320-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02320-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02320-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02320-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02320-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02320-127">CommonParameters</span></span>
<span data-ttu-id="02320-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02320-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02320-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02320-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02320-130">입력</span><span class="sxs-lookup"><span data-stu-id="02320-130">INPUTS</span></span>

### <span data-ttu-id="02320-131">않아야</span><span class="sxs-lookup"><span data-stu-id="02320-131">None</span></span>

## <span data-ttu-id="02320-132">출력</span><span class="sxs-lookup"><span data-stu-id="02320-132">OUTPUTS</span></span>

### <span data-ttu-id="02320-133">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="02320-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="02320-134">상속자</span><span class="sxs-lookup"><span data-stu-id="02320-134">NOTES</span></span>

## <span data-ttu-id="02320-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02320-135">RELATED LINKS</span></span>