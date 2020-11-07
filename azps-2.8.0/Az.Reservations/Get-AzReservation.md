---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: d7eab73fbe6bed4a51df7c5056a0dc52787de845
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871921"
---
# <span data-ttu-id="28a1c-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="28a1c-101">Get-AzReservation</span></span>

## <span data-ttu-id="28a1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="28a1c-103">`Reservation`지정 된 예약 순서로 s 가져오기</span><span class="sxs-lookup"><span data-stu-id="28a1c-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="28a1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28a1c-104">SYNTAX</span></span>

### <span data-ttu-id="28a1c-105">명령줄 (기본값)</span><span class="sxs-lookup"><span data-stu-id="28a1c-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28a1c-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="28a1c-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28a1c-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="28a1c-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28a1c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="28a1c-108">DESCRIPTION</span></span>
<span data-ttu-id="28a1c-109">`Reservation`단일에서 s를 나열 `ReservationOrder` 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a1c-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="28a1c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="28a1c-110">EXAMPLES</span></span>

### <span data-ttu-id="28a1c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="28a1c-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="28a1c-112">지정 된에서 `Reservation` s를 나열 `ReservationOrder` 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a1c-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="28a1c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="28a1c-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="28a1c-114">특정 `Reservation` 세부 정보를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="28a1c-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="28a1c-115">변수</span><span class="sxs-lookup"><span data-stu-id="28a1c-115">PARAMETERS</span></span>

### <span data-ttu-id="28a1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a1c-116">-DefaultProfile</span></span>
<span data-ttu-id="28a1c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28a1c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a1c-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="28a1c-118">-ReservationId</span></span>
<span data-ttu-id="28a1c-119">보려는의 Id입니다. `Reservation`</span><span class="sxs-lookup"><span data-stu-id="28a1c-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a1c-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="28a1c-120">-ReservationOrder</span></span>
<span data-ttu-id="28a1c-121">파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="28a1c-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28a1c-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="28a1c-122">-ReservationOrderId</span></span>
<span data-ttu-id="28a1c-123">이 포함 된의 Id입니다 `ReservationOrder` `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="28a1c-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="28a1c-124">필수.</span><span class="sxs-lookup"><span data-stu-id="28a1c-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28a1c-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="28a1c-125">-ReservationOrderPage</span></span>
<span data-ttu-id="28a1c-126">파이프 개체 매개 변수 `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="28a1c-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28a1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a1c-127">CommonParameters</span></span>
<span data-ttu-id="28a1c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28a1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a1c-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28a1c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a1c-130">입력</span><span class="sxs-lookup"><span data-stu-id="28a1c-130">INPUTS</span></span>

### <span data-ttu-id="28a1c-131">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="28a1c-131">System.Guid</span></span>

### <span data-ttu-id="28a1c-132">PSReservationOrder에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="28a1c-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="28a1c-133">PSReservationOrderPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="28a1c-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="28a1c-134">출력</span><span class="sxs-lookup"><span data-stu-id="28a1c-134">OUTPUTS</span></span>

### <span data-ttu-id="28a1c-135">PSReservationPage에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="28a1c-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="28a1c-136">Microsoft. Azure. PSReservation</span><span class="sxs-lookup"><span data-stu-id="28a1c-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="28a1c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="28a1c-137">NOTES</span></span>

## <span data-ttu-id="28a1c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28a1c-138">RELATED LINKS</span></span>