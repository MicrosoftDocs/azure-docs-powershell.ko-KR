---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac33f0feae7d54798753637f8f7898ab796f0939
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872889"
---
# <span data-ttu-id="22ebc-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="22ebc-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="22ebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="22ebc-103">큐 서비스에 대 한 메트릭 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="22ebc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22ebc-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="22ebc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="22ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="22ebc-106">큐 서비스에 대 한 메트릭 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="22ebc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="22ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="22ebc-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="22ebc-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="22ebc-109">큐 서비스에 대 한 메트릭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="22ebc-110">변수</span><span class="sxs-lookup"><span data-stu-id="22ebc-110">PARAMETERS</span></span>

### <span data-ttu-id="22ebc-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="22ebc-111">-FarmName</span></span>
<span data-ttu-id="22ebc-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ebc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ebc-113">-ResourceGroupName</span></span>
<span data-ttu-id="22ebc-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ebc-115">-생략</span><span class="sxs-lookup"><span data-stu-id="22ebc-115">-Skip</span></span>
<span data-ttu-id="22ebc-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ebc-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="22ebc-117">-Top</span></span>
<span data-ttu-id="22ebc-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="22ebc-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ebc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ebc-120">CommonParameters</span></span>
<span data-ttu-id="22ebc-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22ebc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ebc-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22ebc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ebc-123">입력</span><span class="sxs-lookup"><span data-stu-id="22ebc-123">INPUTS</span></span>

## <span data-ttu-id="22ebc-124">출력</span><span class="sxs-lookup"><span data-stu-id="22ebc-124">OUTPUTS</span></span>

### <span data-ttu-id="22ebc-125">Microsoft AzureStack. 관리 모델. 미터법</span><span class="sxs-lookup"><span data-stu-id="22ebc-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="22ebc-126">상속자</span><span class="sxs-lookup"><span data-stu-id="22ebc-126">NOTES</span></span>

## <span data-ttu-id="22ebc-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22ebc-127">RELATED LINKS</span></span>
