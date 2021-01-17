---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B5FE41A-090B-4859-B021-05CF0A8B7882
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchTask.md
ms.openlocfilehash: bf1a70dc697366099f1949878e81a25bd3adb0fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327123"
---
# <span data-ttu-id="d1c64-101">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d1c64-101">Get-AzBatchTask</span></span>

## <span data-ttu-id="d1c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1c64-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c64-103">작업에 대한 Batch 태스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-103">Gets the Batch tasks for a job.</span></span>

## <span data-ttu-id="d1c64-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1c64-104">SYNTAX</span></span>

### <span data-ttu-id="d1c64-105">ODataFilter(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1c64-105">ODataFilter (Default)</span></span>
```
Get-AzBatchTask [-JobId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c64-106">ID</span><span class="sxs-lookup"><span data-stu-id="d1c64-106">Id</span></span>
```
Get-AzBatchTask [-JobId] <String> [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1c64-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1c64-107">ParentObject</span></span>
```
Get-AzBatchTask [[-Job] <PSCloudJob>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 [-Expand <String>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c64-108">설명</span><span class="sxs-lookup"><span data-stu-id="d1c64-108">DESCRIPTION</span></span>
<span data-ttu-id="d1c64-109">**Get-AzBatchTask** cmdlet은 Batch 작업에 대한 Azure Batch 태스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-109">The **Get-AzBatchTask** cmdlet gets Azure Batch tasks for a Batch job.</span></span>
<span data-ttu-id="d1c64-110">*JobId* 매개 변수 또는 Job 매개 변수를 사용하여 *작업을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="d1c64-110">Specify a job by either the *JobId* parameter or the *Job* parameter.</span></span>
<span data-ttu-id="d1c64-111">단일 작업을 얻습니다. ID 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="d1c64-111">To get a single task, specify the *Id* parameter.</span></span>
<span data-ttu-id="d1c64-112">필터 매개 *변수를* 지정하여 OData(Open Data Protocol) 필터와 일치하는 작업을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-112">You can specify the *Filter* parameter to get the tasks that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="d1c64-113">예제</span><span class="sxs-lookup"><span data-stu-id="d1c64-113">EXAMPLES</span></span>

### <span data-ttu-id="d1c64-114">예제 1: ID로 작업 수행</span><span class="sxs-lookup"><span data-stu-id="d1c64-114">Example 1: Get a task by ID</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job01" -Id "Task03" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 7/25/2015 11:24:52 PM
DisplayName                 :
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task03
LastModified                : 7/25/2015 11:24:52 PM
PreviousState               : Running
PreviousStateTransitionTime : 7/25/2015 11:24:59 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 7/25/2015 11:24:59 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job01/tasks/Task03
```

<span data-ttu-id="d1c64-115">이 명령은 Job01에서 ID Task03이 있는 태스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-115">This command gets the task with ID Task03 under job Job01.</span></span>
<span data-ttu-id="d1c64-116">Get-AzBatchAccountKey cmdlet을 사용하여 $Context 변수에 컨텍스트를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d1c64-117">예제 2: 지정된 작업에서 완료된 모든 태스크를 얻게</span><span class="sxs-lookup"><span data-stu-id="d1c64-117">Example 2: Get all completed tasks from a specified job</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job02" -Filter "state eq 'completed'" -BatchContext $Context
AffinityInformation         :
CommandLine                 : cmd /c dir /s
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task17
LastModified                : 3/24/2015 10:21:51 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:22:00 PM
ResourceFiles               :
RunElevated                 : False
State                       : Completed
StateTransitionTime         : 3/24/2015 10:22:00 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task17

AffinityInformation         :
CommandLine                 : cmd /c echo hello > newFile.txt
ComputeNodeInformation      : Microsoft.Azure.Commands.Batch.Models.PSComputeNodeInformation
Constraints                 : Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
CreationTime                : 3/24/2015 10:21:51 PM
EnvironmentSettings         :
ETag                        : 0x8D295483E08BD9D
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSTaskExecutionInformation
Id                          : Task27
LastModified                : 3/24/2015 10:23:35 PM
PreviousState               : Running
PreviousStateTransitionTime : 3/24/2015 10:23:37 PM
ResourceFiles               :
RunElevated                 : True
State                       : Completed
StateTransitionTime         : 3/24/2015 10:23:37 PM
Statistics                  :
Url                         : https://pfuller.westus.batch.azure.com/jobs/Job02/tasks/Task27
```

<span data-ttu-id="d1c64-118">이 명령은 ID Job02가 있는 작업에서 완료된 태스크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-118">This command gets the completed tasks from the job that has the ID Job02.</span></span>

## <span data-ttu-id="d1c64-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1c64-119">PARAMETERS</span></span>

### <span data-ttu-id="d1c64-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d1c64-120">-BatchContext</span></span>
<span data-ttu-id="d1c64-121">이 cmdlet이 Batch 서비스와 상호 작용하는 데 사용하는 **BatchAccountContext** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d1c64-122">Get-AzBatchAccount cmdlet을 사용하여 BatchAccountContext를 얻을 경우 Batch 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d1c64-123">대신 공유 키 인증을 사용 Get-AzBatchAccountKey 키가 채워진 BatchAccountContext 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d1c64-124">공유 키 인증을 사용하는 경우 기본 액세스 키가 기본적으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d1c64-125">사용할 키를 변경하기 위해 BatchAccountContext.KeyInUse 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c64-126">-DefaultProfile</span></span>
<span data-ttu-id="d1c64-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c64-128">-Expand</span><span class="sxs-lookup"><span data-stu-id="d1c64-128">-Expand</span></span>
<span data-ttu-id="d1c64-129">OData expand 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-129">Specifies an OData expand clause.</span></span>
<span data-ttu-id="d1c64-130">이 매개 변수에 대한 값을 지정하여 얻을 주 엔터티의 관련 엔터티를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-130">Specify a value for this parameter to get associated entities of the main entity to get.</span></span>

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

### <span data-ttu-id="d1c64-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="d1c64-131">-Filter</span></span>
<span data-ttu-id="d1c64-132">작업에 대한 OData 필터 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-132">Specifies an OData filter clause for tasks.</span></span>
<span data-ttu-id="d1c64-133">필터를 지정하지 않으면 이 cmdlet은 Batch 계정 또는 작업에 대한 모든 태스크를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-133">If you do not specify a filter, this cmdlet returns all tasks for the Batch account or job.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c64-134">-Id</span><span class="sxs-lookup"><span data-stu-id="d1c64-134">-Id</span></span>
<span data-ttu-id="d1c64-135">이 cmdlet이 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-135">Specifies the ID of the task that this cmdlet gets.</span></span>
<span data-ttu-id="d1c64-136">와일드카드 문자는 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-136">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c64-137">-Job</span><span class="sxs-lookup"><span data-stu-id="d1c64-137">-Job</span></span>
<span data-ttu-id="d1c64-138">이 cmdlet에서 얻을 수 있는 태스크가 포함된 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-138">Specifies the job that contains tasks that this cmdlet gets.</span></span>
<span data-ttu-id="d1c64-139">**PSCloudJob 개체를 얻습니다.** Get-AzBatchJob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-139">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c64-140">-JobId</span><span class="sxs-lookup"><span data-stu-id="d1c64-140">-JobId</span></span>
<span data-ttu-id="d1c64-141">이 cmdlet에서 수행하는 태스크를 포함하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-141">Specifies the ID of the job that contains the tasks that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c64-142">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d1c64-142">-MaxCount</span></span>
<span data-ttu-id="d1c64-143">반환할 최대 작업 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-143">Specifies the maximum number of tasks to return.</span></span>
<span data-ttu-id="d1c64-144">0 이하의 값을 지정하는 경우 cmdlet은 상한을 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-144">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d1c64-145">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-145">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1c64-146">-Select</span><span class="sxs-lookup"><span data-stu-id="d1c64-146">-Select</span></span>
<span data-ttu-id="d1c64-147">OData select 절을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-147">Specifies an OData select clause.</span></span>
<span data-ttu-id="d1c64-148">이 매개 변수에 대한 값을 지정하여 모든 개체 속성이 아닌 특정 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-148">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="d1c64-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c64-149">CommonParameters</span></span>
<span data-ttu-id="d1c64-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1c64-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c64-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1c64-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c64-152">입력</span><span class="sxs-lookup"><span data-stu-id="d1c64-152">INPUTS</span></span>

### <span data-ttu-id="d1c64-153">System.String</span><span class="sxs-lookup"><span data-stu-id="d1c64-153">System.String</span></span>

### <span data-ttu-id="d1c64-154">Microsoft.Azure.Commands.Batch. Models.PSCloudJob</span><span class="sxs-lookup"><span data-stu-id="d1c64-154">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="d1c64-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d1c64-155">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d1c64-156">출력</span><span class="sxs-lookup"><span data-stu-id="d1c64-156">OUTPUTS</span></span>

### <span data-ttu-id="d1c64-157">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d1c64-157">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

## <span data-ttu-id="d1c64-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1c64-158">NOTES</span></span>

## <span data-ttu-id="d1c64-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1c64-159">RELATED LINKS</span></span>

[<span data-ttu-id="d1c64-160">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d1c64-160">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d1c64-161">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="d1c64-161">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="d1c64-162">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d1c64-162">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="d1c64-163">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d1c64-163">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="d1c64-164">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d1c64-164">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="d1c64-165">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d1c64-165">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)