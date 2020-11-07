---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877729"
---
# <span data-ttu-id="ef418-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="ef418-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="ef418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef418-102">SYNOPSIS</span></span>
<span data-ttu-id="ef418-103">전방 도어 만들기에 대 한 PSLoadBalancingSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ef418-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ef418-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef418-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef418-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef418-105">DESCRIPTION</span></span>
<span data-ttu-id="ef418-106">전방 도어 만들기에 대 한 PSLoadBalancingSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ef418-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ef418-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef418-107">EXAMPLES</span></span>

### <span data-ttu-id="ef418-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef418-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="ef418-109">전방 도어 만들기에 대 한 PSLoadBalancingSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ef418-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="ef418-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef418-110">PARAMETERS</span></span>

### <span data-ttu-id="ef418-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="ef418-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="ef418-112">가장 느린 대기 시간 버킷에 대 한 프로브 추가 대기 시간 (밀리초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="ef418-113">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef418-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef418-114">-DefaultProfile</span></span>
<span data-ttu-id="ef418-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef418-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ef418-116">-Name</span></span>
<span data-ttu-id="ef418-117">상태 검색 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-117">health probe setting name.</span></span>

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

### <span data-ttu-id="ef418-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="ef418-118">-SampleSize</span></span>
<span data-ttu-id="ef418-119">부하 분산 결정에 대해 고려할 샘플 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="ef418-120">기본값은 4입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef418-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="ef418-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="ef418-122">샘플 기간 내에서 기본 값이 완료 되어야 하는 샘플 수는 2입니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef418-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef418-123">CommonParameters</span></span>
<span data-ttu-id="ef418-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef418-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef418-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef418-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef418-126">입력</span><span class="sxs-lookup"><span data-stu-id="ef418-126">INPUTS</span></span>

### <span data-ttu-id="ef418-127">않아야</span><span class="sxs-lookup"><span data-stu-id="ef418-127">None</span></span>

## <span data-ttu-id="ef418-128">출력</span><span class="sxs-lookup"><span data-stu-id="ef418-128">OUTPUTS</span></span>

### <span data-ttu-id="ef418-129">FrontDoor. PSLoadBalancingSetting/.</span><span class="sxs-lookup"><span data-stu-id="ef418-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="ef418-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ef418-130">NOTES</span></span>

## <span data-ttu-id="ef418-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef418-131">RELATED LINKS</span></span>

<span data-ttu-id="ef418-132">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ef418-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>