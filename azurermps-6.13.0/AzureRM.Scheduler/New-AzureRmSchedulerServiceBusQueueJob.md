---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerservicebusqueuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: 0382362c16ba65aa194029677cf8ca846e93db54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526060"
---
# <span data-ttu-id="28b0c-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="28b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="28b0c-103">Service bus 큐 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28b0c-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="28b0c-106">**AzureRmSchedulerServiceBusQueueJob** Cmdlet은 Azure Scheduler에서 service bus 큐 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>
<span data-ttu-id="28b0c-107">이 cmdlet은 *Erroractiontype* 매개 변수에 기반 하는 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="28b0c-108">동적 매개 변수는 다른 매개 변수 값에 따라 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-108">Dynamic parameters become available based on other parameter values.</span></span>
<span data-ttu-id="28b0c-109">다른 매개 변수를 지정한 후 동적 매개 변수의 이름을 검색 하려면 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="28b0c-110">필수 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="28b0c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="28b0c-111">EXAMPLES</span></span>

## <span data-ttu-id="28b0c-112">변수</span><span class="sxs-lookup"><span data-stu-id="28b0c-112">PARAMETERS</span></span>

### <span data-ttu-id="28b0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b0c-113">-DefaultProfile</span></span>
<span data-ttu-id="28b0c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="28b0c-115">-EndTime</span></span>
<span data-ttu-id="28b0c-116">작업에 대 한 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="28b0c-117">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="28b0c-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="28b0c-118">-ErrorActionType</span></span>
<span data-ttu-id="28b0c-119">작업에 대 한 오류 동작 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="28b0c-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28b0c-121">Http</span><span class="sxs-lookup"><span data-stu-id="28b0c-121">Http</span></span> 
- <span data-ttu-id="28b0c-122">Https</span><span class="sxs-lookup"><span data-stu-id="28b0c-122">Https</span></span> 
- <span data-ttu-id="28b0c-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="28b0c-123">StorageQueue</span></span> 
- <span data-ttu-id="28b0c-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="28b0c-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="28b0c-125">Service<c13> Stopic</span><span class="sxs-lookup"><span data-stu-id="28b0c-125">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="28b0c-126">-ExecutionCount</span></span>
<span data-ttu-id="28b0c-127">작업이 실행 되는 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="28b0c-128">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-129">-빈도</span><span class="sxs-lookup"><span data-stu-id="28b0c-129">-Frequency</span></span>
<span data-ttu-id="28b0c-130">작업의 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="28b0c-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28b0c-132">길이의</span><span class="sxs-lookup"><span data-stu-id="28b0c-132">Minute</span></span> 
- <span data-ttu-id="28b0c-133">시간씩</span><span class="sxs-lookup"><span data-stu-id="28b0c-133">Hour</span></span> 
- <span data-ttu-id="28b0c-134">부활절</span><span class="sxs-lookup"><span data-stu-id="28b0c-134">Day</span></span> 
- <span data-ttu-id="28b0c-135">이번</span><span class="sxs-lookup"><span data-stu-id="28b0c-135">Week</span></span> 
- <span data-ttu-id="28b0c-136">달은</span><span class="sxs-lookup"><span data-stu-id="28b0c-136">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-137">-Interval</span><span class="sxs-lookup"><span data-stu-id="28b0c-137">-Interval</span></span>
<span data-ttu-id="28b0c-138">작업에 대 한 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="28b0c-139">-JobCollectionName</span></span>
<span data-ttu-id="28b0c-140">작업이 속한 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="28b0c-141">-JobName</span></span>
<span data-ttu-id="28b0c-142">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-142">Specifies a name for the job.</span></span>

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

### <span data-ttu-id="28b0c-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="28b0c-143">-JobState</span></span>
<span data-ttu-id="28b0c-144">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-144">Specifies the state of the job.</span></span>
<span data-ttu-id="28b0c-145">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28b0c-146">수</span><span class="sxs-lookup"><span data-stu-id="28b0c-146">Enabled</span></span> 
- <span data-ttu-id="28b0c-147">비활성화</span><span class="sxs-lookup"><span data-stu-id="28b0c-147">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b0c-148">-ResourceGroupName</span></span>
<span data-ttu-id="28b0c-149">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-149">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="28b0c-150">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="28b0c-150">-ServiceBusMessage</span></span>
<span data-ttu-id="28b0c-151">Service bus 큐 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-151">Specifies a service bus queue message.</span></span>

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

### <span data-ttu-id="28b0c-152">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="28b0c-152">-ServiceBusNamespace</span></span>
<span data-ttu-id="28b0c-153">Service bus 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-153">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="28b0c-154">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="28b0c-154">-ServiceBusQueueName</span></span>
<span data-ttu-id="28b0c-155">서비스 버스 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-155">Specifies a service bus queue name.</span></span>

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

### <span data-ttu-id="28b0c-156">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="28b0c-156">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="28b0c-157">공유 액세스 서명 키 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-157">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="28b0c-158">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="28b0c-158">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="28b0c-159">공유 액세스 서명 키 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-159">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="28b0c-160">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="28b0c-160">-ServiceBusTransportType</span></span>
<span data-ttu-id="28b0c-161">서비스 버스 전송 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-161">Specifies a service bus transport type.</span></span>
<span data-ttu-id="28b0c-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28b0c-163">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="28b0c-163">NetMessaging</span></span> 
- <span data-ttu-id="28b0c-164">AMQP</span><span class="sxs-lookup"><span data-stu-id="28b0c-164">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="28b0c-165">-StartTime</span></span>
<span data-ttu-id="28b0c-166">작업에 대 한 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-166">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="28b0c-167">-확인</span><span class="sxs-lookup"><span data-stu-id="28b0c-167">-Confirm</span></span>
<span data-ttu-id="28b0c-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b0c-169">-WhatIf</span></span>
<span data-ttu-id="28b0c-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b0c-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b0c-172">CommonParameters</span></span>
<span data-ttu-id="28b0c-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b0c-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b0c-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b0c-175">입력</span><span class="sxs-lookup"><span data-stu-id="28b0c-175">INPUTS</span></span>

### <span data-ttu-id="28b0c-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28b0c-176">System.String</span></span>

## <span data-ttu-id="28b0c-177">출력</span><span class="sxs-lookup"><span data-stu-id="28b0c-177">OUTPUTS</span></span>

### <span data-ttu-id="28b0c-178">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="28b0c-178">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="28b0c-179">상속자</span><span class="sxs-lookup"><span data-stu-id="28b0c-179">NOTES</span></span>

## <span data-ttu-id="28b0c-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28b0c-180">RELATED LINKS</span></span>

[<span data-ttu-id="28b0c-181">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-181">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="28b0c-182">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="28b0c-182">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="28b0c-183">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="28b0c-184">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="28b0c-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="28b0c-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="28b0c-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="28b0c-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="28b0c-188">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-188">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="28b0c-189">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="28b0c-189">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)

