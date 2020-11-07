---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e15e6ee6186dc19f9f85264548c1b735ea242b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876807"
---
# <span data-ttu-id="8d329-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8d329-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="8d329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d329-102">SYNOPSIS</span></span>
<span data-ttu-id="8d329-103">새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="8d329-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d329-104">SYNTAX</span></span>

### <span data-ttu-id="8d329-105">BandwidthParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d329-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d329-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d329-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d329-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d329-107">DESCRIPTION</span></span>
<span data-ttu-id="8d329-108">**AzDataBoxEdgeBandwidthSchedule** Cmdlet은 대역폭 사용을 관리 하는 데 도움이 되도록 데이터 상자 가장자리 장치에 대 한 새 대역폭 일정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="8d329-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8d329-109">EXAMPLES</span></span>

### <span data-ttu-id="8d329-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d329-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="8d329-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="8d329-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="8d329-112">변수</span><span class="sxs-lookup"><span data-stu-id="8d329-112">PARAMETERS</span></span>

### <span data-ttu-id="8d329-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d329-113">-AsJob</span></span>
<span data-ttu-id="8d329-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8d329-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-115">-대역폭</span><span class="sxs-lookup"><span data-stu-id="8d329-115">-Bandwidth</span></span>
<span data-ttu-id="8d329-116">Mbps 단위 대역폭</span><span class="sxs-lookup"><span data-stu-id="8d329-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="8d329-117">-DaysOfWeek</span></span>
<span data-ttu-id="8d329-118">예정 된 DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="8d329-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d329-119">-DefaultProfile</span></span>
<span data-ttu-id="8d329-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d329-121">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="8d329-121">-DeviceName</span></span>
<span data-ttu-id="8d329-122">장치 이름</span><span class="sxs-lookup"><span data-stu-id="8d329-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8d329-123">-Name</span></span>
<span data-ttu-id="8d329-124">자원 이름</span><span class="sxs-lookup"><span data-stu-id="8d329-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d329-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d329-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8d329-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8d329-127">-StartTime</span></span>
<span data-ttu-id="8d329-128">일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="8d329-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="8d329-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="8d329-129">-StopTime</span></span>
<span data-ttu-id="8d329-130">일정 중지 시간</span><span class="sxs-lookup"><span data-stu-id="8d329-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="8d329-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="8d329-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="8d329-132">무제한 대역폭을 설정 하 고 false로 설정 하면 기본값을 20mbps로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d329-133">-확인</span><span class="sxs-lookup"><span data-stu-id="8d329-133">-Confirm</span></span>
<span data-ttu-id="8d329-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d329-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d329-135">-WhatIf</span></span>
<span data-ttu-id="8d329-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d329-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d329-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d329-138">CommonParameters</span></span>
<span data-ttu-id="8d329-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d329-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d329-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d329-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d329-141">입력</span><span class="sxs-lookup"><span data-stu-id="8d329-141">INPUTS</span></span>

### <span data-ttu-id="8d329-142">않아야</span><span class="sxs-lookup"><span data-stu-id="8d329-142">None</span></span>

## <span data-ttu-id="8d329-143">출력</span><span class="sxs-lookup"><span data-stu-id="8d329-143">OUTPUTS</span></span>

### <span data-ttu-id="8d329-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8d329-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="8d329-145">상속자</span><span class="sxs-lookup"><span data-stu-id="8d329-145">NOTES</span></span>

## <span data-ttu-id="8d329-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d329-146">RELATED LINKS</span></span>