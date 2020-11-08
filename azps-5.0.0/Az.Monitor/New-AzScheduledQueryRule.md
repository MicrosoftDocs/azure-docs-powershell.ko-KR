---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRule.md
ms.openlocfilehash: 5a896bedd7e0dd6e220fb4b8dae2cc2e87ae0fcb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217292"
---
# <span data-ttu-id="cd363-101">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd363-101">New-AzScheduledQueryRule</span></span>

## <span data-ttu-id="cd363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd363-102">SYNOPSIS</span></span>
<span data-ttu-id="cd363-103">로그 알림 규칙을 만듭니다 (예약 된 쿼리 규칙 유형).</span><span class="sxs-lookup"><span data-stu-id="cd363-103">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="cd363-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd363-104">SYNTAX</span></span>

```
New-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> -Schedule <PSScheduledQueryRuleSchedule>
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -Enabled <Boolean> -ResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd363-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd363-105">DESCRIPTION</span></span>
<span data-ttu-id="cd363-106">로그 알림 규칙을 만듭니다 (예약 된 쿼리 규칙 유형).</span><span class="sxs-lookup"><span data-stu-id="cd363-106">Creates a Log Alert Rule (Scheduled Query Rule type)</span></span>

## <span data-ttu-id="cd363-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd363-107">EXAMPLES</span></span>

### <span data-ttu-id="cd363-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd363-108">Example 1</span></span>
```powershell
PS C:\> New-AzScheduledQueryRule -Location "West Europe" -Action $alertingAction -Enabled $true -Description "log alert foo" -Schedule $schedule -Source $source -Name "LogAlertRule1"
```

## <span data-ttu-id="cd363-109">변수</span><span class="sxs-lookup"><span data-stu-id="cd363-109">PARAMETERS</span></span>

### <span data-ttu-id="cd363-110">-작업</span><span class="sxs-lookup"><span data-stu-id="cd363-110">-Action</span></span>
<span data-ttu-id="cd363-111">예약 된 쿼리 규칙 경고 동작</span><span class="sxs-lookup"><span data-stu-id="cd363-111">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd363-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd363-112">-AsJob</span></span>
<span data-ttu-id="cd363-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cd363-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd363-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd363-114">-DefaultProfile</span></span>
<span data-ttu-id="cd363-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd363-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd363-116">-설명</span><span class="sxs-lookup"><span data-stu-id="cd363-116">-Description</span></span>
<span data-ttu-id="cd363-117">이 경고에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="cd363-117">The description for this alert</span></span>

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

### <span data-ttu-id="cd363-118">-사용</span><span class="sxs-lookup"><span data-stu-id="cd363-118">-Enabled</span></span>
<span data-ttu-id="cd363-119">Azure alert state-유효한 값-$true, $false</span><span class="sxs-lookup"><span data-stu-id="cd363-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd363-120">-위치</span><span class="sxs-lookup"><span data-stu-id="cd363-120">-Location</span></span>
<span data-ttu-id="cd363-121">이 알림의 위치</span><span class="sxs-lookup"><span data-stu-id="cd363-121">The location for this alert</span></span>

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

### <span data-ttu-id="cd363-122">-이름</span><span class="sxs-lookup"><span data-stu-id="cd363-122">-Name</span></span>
<span data-ttu-id="cd363-123">알림 이름</span><span class="sxs-lookup"><span data-stu-id="cd363-123">The alert name</span></span>

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

### <span data-ttu-id="cd363-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd363-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd363-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cd363-125">The resource group name</span></span>

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

### <span data-ttu-id="cd363-126">-일정</span><span class="sxs-lookup"><span data-stu-id="cd363-126">-Schedule</span></span>
<span data-ttu-id="cd363-127">예약 된 쿼리 규칙 일정</span><span class="sxs-lookup"><span data-stu-id="cd363-127">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd363-128">-원본</span><span class="sxs-lookup"><span data-stu-id="cd363-128">-Source</span></span>
<span data-ttu-id="cd363-129">예약 된 쿼리 규칙 원본</span><span class="sxs-lookup"><span data-stu-id="cd363-129">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd363-130">태그</span><span class="sxs-lookup"><span data-stu-id="cd363-130">-Tag</span></span>
<span data-ttu-id="cd363-131">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="cd363-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd363-132">-확인</span><span class="sxs-lookup"><span data-stu-id="cd363-132">-Confirm</span></span>
<span data-ttu-id="cd363-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd363-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd363-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd363-134">-WhatIf</span></span>
<span data-ttu-id="cd363-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd363-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd363-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd363-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd363-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd363-137">CommonParameters</span></span>
<span data-ttu-id="cd363-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd363-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd363-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd363-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd363-140">입력</span><span class="sxs-lookup"><span data-stu-id="cd363-140">INPUTS</span></span>

### <span data-ttu-id="cd363-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd363-141">System.String</span></span>

## <span data-ttu-id="cd363-142">출력</span><span class="sxs-lookup"><span data-stu-id="cd363-142">OUTPUTS</span></span>

### <span data-ttu-id="cd363-143">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd363-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="cd363-144">상속자</span><span class="sxs-lookup"><span data-stu-id="cd363-144">NOTES</span></span>

## <span data-ttu-id="cd363-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd363-145">RELATED LINKS</span></span>