---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 2b470a9837fafbb20d2e83f6fa9e7b4308b12d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871918"
---
# <span data-ttu-id="351a8-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="351a8-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="351a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351a8-102">SYNOPSIS</span></span>
<span data-ttu-id="351a8-103">사용 가능한 예약 카탈로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="351a8-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="351a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="351a8-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="351a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="351a8-105">DESCRIPTION</span></span>
<span data-ttu-id="351a8-106">지정 된 Azure 구독에 대해 예약 된 인스턴스 구입에 사용할 수 있는 지역 및 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="351a8-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="351a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="351a8-107">EXAMPLES</span></span>

### <span data-ttu-id="351a8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="351a8-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="351a8-109">기본 구독에 대 한 westus에서 VirtualMachines catalog 가져오기</span><span class="sxs-lookup"><span data-stu-id="351a8-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="351a8-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="351a8-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="351a8-111">지정 된 구독에 대 한 SuseLinux 카탈로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="351a8-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="351a8-112">변수</span><span class="sxs-lookup"><span data-stu-id="351a8-112">PARAMETERS</span></span>

### <span data-ttu-id="351a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351a8-113">-DefaultProfile</span></span>
<span data-ttu-id="351a8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="351a8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="351a8-115">-위치</span><span class="sxs-lookup"><span data-stu-id="351a8-115">-Location</span></span>
<span data-ttu-id="351a8-116">카탈로그에 예약 된 리소스의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="351a8-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="351a8-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="351a8-117">-ReservedResourceType</span></span>
<span data-ttu-id="351a8-118">카탈로그에 예약 된 리소스의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="351a8-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="351a8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="351a8-119">-SubscriptionId</span></span>
<span data-ttu-id="351a8-120">구독 Id</span><span class="sxs-lookup"><span data-stu-id="351a8-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351a8-121">CommonParameters</span></span>
<span data-ttu-id="351a8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="351a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351a8-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="351a8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351a8-124">입력</span><span class="sxs-lookup"><span data-stu-id="351a8-124">INPUTS</span></span>

### <span data-ttu-id="351a8-125">않아야</span><span class="sxs-lookup"><span data-stu-id="351a8-125">None</span></span>

## <span data-ttu-id="351a8-126">출력</span><span class="sxs-lookup"><span data-stu-id="351a8-126">OUTPUTS</span></span>

### <span data-ttu-id="351a8-127">PSCatalog에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="351a8-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="351a8-128">상속자</span><span class="sxs-lookup"><span data-stu-id="351a8-128">NOTES</span></span>

## <span data-ttu-id="351a8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="351a8-129">RELATED LINKS</span></span>