---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: f857f578ab3f0b8baacd0c5d392659ac09b0790f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327578"
---
# <span data-ttu-id="887c8-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="887c8-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="887c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="887c8-102">SYNOPSIS</span></span>
<span data-ttu-id="887c8-103">자동 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="887c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="887c8-104">SYNTAX</span></span>

### <span data-ttu-id="887c8-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="887c8-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="887c8-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="887c8-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="887c8-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="887c8-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="887c8-108">설명</span><span class="sxs-lookup"><span data-stu-id="887c8-108">DESCRIPTION</span></span>
<span data-ttu-id="887c8-109">**New-AzAutoscaleProfile** cmdlet은 자동 크기 조정 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="887c8-110">예제</span><span class="sxs-lookup"><span data-stu-id="887c8-110">EXAMPLES</span></span>

### <span data-ttu-id="887c8-111">예제 1: 고정된 날짜로 단일 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="887c8-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="887c8-112">첫 번째 명령은 요청이라는 자동 조정 규칙을 만든 다음, $Rule 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="887c8-113">두 번째 명령은 2010에서 규칙을 사용하여 고정된 날짜로 Profile01이라는 프로필을 $Rule.</span><span class="sxs-lookup"><span data-stu-id="887c8-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="887c8-114">예제 2: 일정을 사용하여 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="887c8-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="887c8-115">첫 번째 명령은 요청이라는 자동 조정 규칙을 만든 다음, $Rule 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="887c8-116">두 번째 명령은 다음 명령의 규칙을 사용하여 두 번째 일정으로 SecondProfileName이라는 프로필을 $Rule.</span><span class="sxs-lookup"><span data-stu-id="887c8-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="887c8-117">예제 3: 두 가지 규칙으로 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="887c8-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="887c8-118">처음 두 명령은 규칙을 만들고 각각 $Rule 1 및 $Rule 2 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="887c8-119">세 번째 명령은 Rule1 및 Rule2의 규칙을 사용하여 ProfileName이라는 프로필을 만든 다음 $Profile 1 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="887c8-120">마지막 명령은 Rule1 및 Rule2의 규칙을 사용하여 SecondProfileName이라는 프로필을 만든 다음 $Profile 2 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="887c8-121">예제 4: 일정 또는 고정 날짜가 없는 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="887c8-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="887c8-122">첫 번째 명령은 요청이라는 자동 조정 규칙을 만든 다음, $Rule 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="887c8-123">두 번째 명령은 일정이나 고정 날짜 없이 프로필을 만든 다음, $Profile 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="887c8-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="887c8-124">PARAMETERS</span></span>

### <span data-ttu-id="887c8-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="887c8-125">-DefaultCapacity</span></span>
<span data-ttu-id="887c8-126">기본 용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887c8-127">-DefaultProfile</span></span>
<span data-ttu-id="887c8-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="887c8-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="887c8-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="887c8-129">-EndTimeWindow</span></span>
<span data-ttu-id="887c8-130">기간의 끝을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="887c8-131">-MaximumCapacity</span></span>
<span data-ttu-id="887c8-132">최대 용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="887c8-133">-MinimumCapacity</span></span>
<span data-ttu-id="887c8-134">최소 용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-135">-Name</span><span class="sxs-lookup"><span data-stu-id="887c8-135">-Name</span></span>
<span data-ttu-id="887c8-136">만들 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="887c8-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="887c8-138">재발 빈도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="887c8-139">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="887c8-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="887c8-140">없음</span><span class="sxs-lookup"><span data-stu-id="887c8-140">None</span></span>
- <span data-ttu-id="887c8-141">초</span><span class="sxs-lookup"><span data-stu-id="887c8-141">Second</span></span>
- <span data-ttu-id="887c8-142">분</span><span class="sxs-lookup"><span data-stu-id="887c8-142">Minute</span></span>
- <span data-ttu-id="887c8-143">Hour</span><span class="sxs-lookup"><span data-stu-id="887c8-143">Hour</span></span>
- <span data-ttu-id="887c8-144">Day</span><span class="sxs-lookup"><span data-stu-id="887c8-144">Day</span></span>
- <span data-ttu-id="887c8-145">주</span><span class="sxs-lookup"><span data-stu-id="887c8-145">Week</span></span>
- <span data-ttu-id="887c8-146">월</span><span class="sxs-lookup"><span data-stu-id="887c8-146">Month</span></span>
- <span data-ttu-id="887c8-147">연도에 이러한 모든 값이 지원되지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-148">-Rule</span><span class="sxs-lookup"><span data-stu-id="887c8-148">-Rule</span></span>
<span data-ttu-id="887c8-149">프로필에 추가할 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="887c8-150">-ScheduleDay</span></span>
<span data-ttu-id="887c8-151">예약된 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="887c8-152">-ScheduleHour</span></span>
<span data-ttu-id="887c8-153">예약된 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="887c8-154">-ScheduleMinute</span></span>
<span data-ttu-id="887c8-155">예약된 분을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="887c8-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="887c8-157">일정의 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="887c8-158">-StartTimeWindow</span></span>
<span data-ttu-id="887c8-159">시간 창의 시작을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="887c8-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="887c8-161">시간 창의 표준 시간대를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="887c8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887c8-162">CommonParameters</span></span>
<span data-ttu-id="887c8-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="887c8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887c8-164">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="887c8-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887c8-165">입력</span><span class="sxs-lookup"><span data-stu-id="887c8-165">INPUTS</span></span>

### <span data-ttu-id="887c8-166">System.String</span><span class="sxs-lookup"><span data-stu-id="887c8-166">System.String</span></span>

### <span data-ttu-id="887c8-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="887c8-167">System.DateTime</span></span>

### <span data-ttu-id="887c8-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="887c8-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="887c8-169">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="887c8-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="887c8-170">System.Collections.Generic.List `1[[System.Nullable` 1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="887c8-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="887c8-171">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="887c8-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="887c8-172">출력</span><span class="sxs-lookup"><span data-stu-id="887c8-172">OUTPUTS</span></span>

### <span data-ttu-id="887c8-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="887c8-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="887c8-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="887c8-174">NOTES</span></span>

## <span data-ttu-id="887c8-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="887c8-175">RELATED LINKS</span></span>

[<span data-ttu-id="887c8-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="887c8-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="887c8-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="887c8-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="887c8-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="887c8-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="887c8-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="887c8-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="887c8-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="887c8-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)

