---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056549"
---
# <span data-ttu-id="44098-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="44098-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="44098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44098-102">SYNOPSIS</span></span>
<span data-ttu-id="44098-103">일일 또는 월별 그레인에 대 한 예약 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="44098-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="44098-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44098-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44098-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44098-105">DESCRIPTION</span></span>
<span data-ttu-id="44098-106">**AzConsumptionReservationSummary** cmdlet은 일일 또는 월별 그레인에 대 한 예약 요약을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="44098-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="44098-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44098-107">EXAMPLES</span></span>

### <span data-ttu-id="44098-108">예제 1: 월간 그레인에 대 한 예약 주문 Id를 사용 하 여 예약 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="44098-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="44098-109">예제 2: 예약 주문 Id와 월별 그레인에 대 한 예약 Id를 사용 하 여 예약 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="44098-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="44098-110">예제 3: 일일 그레인 제공 날짜 범위에 대 한 예약 주문 Id를 사용 하 여 예약 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="44098-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="44098-111">예제 4: 일일 그레인 제공 날짜 범위에 대 한 예약 주문 Id 및 예약 Id를 사용 하 여 예약 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="44098-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="44098-112">변수</span><span class="sxs-lookup"><span data-stu-id="44098-112">PARAMETERS</span></span>

### <span data-ttu-id="44098-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44098-113">-DefaultProfile</span></span>
<span data-ttu-id="44098-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44098-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44098-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="44098-115">-EndDate</span></span>
<span data-ttu-id="44098-116">예약 요약의 끝 데이터 (UTC의 YYYY-DD)는 일일 그레인에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="44098-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44098-117">-그레인</span><span class="sxs-lookup"><span data-stu-id="44098-117">-Grain</span></span>
<span data-ttu-id="44098-118">예약 요약의 시간 세분화는 일 단위 또는 월 단위 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44098-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44098-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="44098-119">-ReservationId</span></span>
<span data-ttu-id="44098-120">예약 순서 내에서 예약의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="44098-120">The identifier of a reservation within a reservation order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44098-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="44098-121">-ReservationOrderId</span></span>
<span data-ttu-id="44098-122">예약 구입의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="44098-122">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44098-123">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="44098-123">-StartDate</span></span>
<span data-ttu-id="44098-124">일일 그레인에만 필요 하며 예약 요약의 시작 데이터 (UTC에서 yyyy-mm-dd)입니다.</span><span class="sxs-lookup"><span data-stu-id="44098-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44098-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44098-125">CommonParameters</span></span>
<span data-ttu-id="44098-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44098-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44098-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44098-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44098-128">입력</span><span class="sxs-lookup"><span data-stu-id="44098-128">INPUTS</span></span>

### <span data-ttu-id="44098-129">않아야</span><span class="sxs-lookup"><span data-stu-id="44098-129">None</span></span>

## <span data-ttu-id="44098-130">출력</span><span class="sxs-lookup"><span data-stu-id="44098-130">OUTPUTS</span></span>

### <span data-ttu-id="44098-131">PSReservationSummary를 사용 하 여 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44098-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="44098-132">상속자</span><span class="sxs-lookup"><span data-stu-id="44098-132">NOTES</span></span>

## <span data-ttu-id="44098-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44098-133">RELATED LINKS</span></span>