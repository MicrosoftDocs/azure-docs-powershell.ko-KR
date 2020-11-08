---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: 5d2dbd8d8cbb7ca9de264f5d25769a0f0c715730
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047211"
---
# <span data-ttu-id="a8cac-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a8cac-101">New-AzBatchTask</span></span>

## <span data-ttu-id="a8cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8cac-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cac-103">작업 아래에 일괄 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="a8cac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a8cac-104">SYNTAX</span></span>

### <span data-ttu-id="a8cac-105">JobId_Single (기본값)</span><span class="sxs-lookup"><span data-stu-id="a8cac-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8cac-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="a8cac-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8cac-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="a8cac-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8cac-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="a8cac-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] -CommandLine <String>
 [-ResourceFiles <PSResourceFile[]>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8cac-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a8cac-109">DESCRIPTION</span></span>
<span data-ttu-id="a8cac-110">**AzBatchTask** Cmdlet은 *JobId* 매개 변수 또는 *작업* 매개 변수에 지정 된 작업 아래에 Azure Batch 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="a8cac-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a8cac-111">EXAMPLES</span></span>

### <span data-ttu-id="a8cac-112">예제 1: 일괄 처리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="a8cac-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="a8cac-113">이 명령은 ID 작업이 000001 인 작업 아래에 ID Task23 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="a8cac-114">작업이 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-114">The task runs the specified command.</span></span>
<span data-ttu-id="a8cac-115">$Context 변수에 컨텍스트를 할당 하려면 **Get-AzBatchAccountKey** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-115">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a8cac-116">예제 2: 일괄 처리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="a8cac-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="a8cac-117">이 명령은 **AzBatchJob** cmdlet을 사용 하 여 000001 ID 작업을 포함 하는 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="a8cac-118">이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a8cac-119">이 명령은 해당 작업 아래에 ID Task26 있는 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="a8cac-120">작업에서 높은 권한을 사용 하 여 지정 된 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="a8cac-121">예제 3: 파이프라인을 사용 하 여 지정 된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="a8cac-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="a8cac-122">첫 번째 명령은 **Get-AzBatchAccountKey** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="a8cac-123">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="a8cac-124">다음 두 명령은 New-Object cmdlet을 사용 하 여 **Pscloudtask** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="a8cac-125">이 명령은 $Task 01 및 $Task 02 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="a8cac-126">마지막 명령은 **AzBatchJob** 를 사용 하 여 000001의 ID 작업을 포함 하는 일괄 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="a8cac-127">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 작업을 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a8cac-128">이 명령은 해당 작업 아래에 작업 컬렉션을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="a8cac-129">이 명령은 $Context에 저장 된 컨텍스트를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="a8cac-130">예제 4: 지정 된 작업에 작업 컬렉션 추가</span><span class="sxs-lookup"><span data-stu-id="a8cac-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="a8cac-131">첫 번째 명령은 **Get-AzBatchAccountKey** 를 사용 하 여 ContosoBatchAccount 라는 일괄 계정에 대 한 계정 키에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="a8cac-132">명령이이 개체 참조를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="a8cac-133">다음 두 명령은 New-Object cmdlet을 사용 하 여 **Pscloudtask** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="a8cac-134">이 명령은 $Task 01 및 $Task 02 변수에 작업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="a8cac-135">마지막 명령은 ID 작업이 000001 인 작업 아래에 $Task 01 및 $Task 02에 저장 된 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="a8cac-136">예제 5: 출력 파일이 있는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="a8cac-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="a8cac-137">예제 6: 인증 토큰 설정이 있는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="a8cac-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="a8cac-138">예제 7: 컨테이너에서 실행 되는 작업 추가</span><span class="sxs-lookup"><span data-stu-id="a8cac-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="a8cac-139">변수</span><span class="sxs-lookup"><span data-stu-id="a8cac-139">PARAMETERS</span></span>

### <span data-ttu-id="a8cac-140">-AffinityInformation</span><span class="sxs-lookup"><span data-stu-id="a8cac-140">-AffinityInformation</span></span>
<span data-ttu-id="a8cac-141">일괄 처리 서비스가 작업을 실행할 노드를 선택 하는 데 사용 하는 지역 힌트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-142">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="a8cac-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="a8cac-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="a8cac-144">작업에서 일괄 처리 서비스 작업을 수행 하는 데 사용할 수 있는 인증 토큰에 대 한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="a8cac-145">이 설정을 선택 하면 일괄 처리 서비스에서 계정 액세스 키 없이 일괄 처리 서비스 작업을 인증 하는 데 사용할 수 있는 인증 토큰이 있는 작업을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="a8cac-146">토큰은 AZ_BATCH_AUTHENTICATION_TOKEN 환경 변수를 통해 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="a8cac-147">토큰을 사용 하 여 수행할 수 있는 작업은 설정에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="a8cac-148">예를 들어 작업에 다른 작업을 추가 하거나 작업 또는 다른 작업의 상태를 확인 하기 위해 작업이 작업 권한을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a8cac-149">-BatchContext</span></span>
<span data-ttu-id="a8cac-150">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a8cac-151">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a8cac-152">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-152">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a8cac-153">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a8cac-154">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a8cac-155">-명령줄</span><span class="sxs-lookup"><span data-stu-id="a8cac-155">-CommandLine</span></span>
<span data-ttu-id="a8cac-156">작업의 명령줄을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-156">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-157">-제약 조건</span><span class="sxs-lookup"><span data-stu-id="a8cac-157">-Constraints</span></span>
<span data-ttu-id="a8cac-158">이 작업에 적용 되는 실행 제한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-158">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="a8cac-159">-ContainerSettings</span></span>
<span data-ttu-id="a8cac-160">작업이 실행 되는 컨테이너에 대 한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="a8cac-161">이 작업을 실행 하는 풀에 containerConfiguration가 설정 되어 있는 경우에도이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="a8cac-162">이 작업을 실행 하는 풀에 containerConfiguration가 설정 되어 있지 않으면이를 설정 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="a8cac-163">이를 지정 하면 AZ_BATCH_NODE_ROOT_DIR 아래에 재귀적으로 모든 디렉터리가 컨테이너에 매핑되고, 모든 작업 환경 변수는 컨테이너에 매핑되고, 작업 명령줄이 컨테이너에서 실행 됩니다..</span><span class="sxs-lookup"><span data-stu-id="a8cac-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8cac-164">-DefaultProfile</span></span>
<span data-ttu-id="a8cac-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8cac-166">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="a8cac-166">-DependsOn</span></span>
<span data-ttu-id="a8cac-167">작업이 다른 작업에 의존 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="a8cac-168">작업은 모든 종속 작업을 성공적으로 완료할 때까지 예약 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a8cac-169">-DisplayName</span></span>
<span data-ttu-id="a8cac-170">작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-170">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="a8cac-171">-EnvironmentSettings</span></span>
<span data-ttu-id="a8cac-172">이 cmdlet이 작업에 추가 하는 환경 설정을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="a8cac-173">키는 환경 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-173">The key is the environment setting name.</span></span>
<span data-ttu-id="a8cac-174">값은 환경 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="a8cac-175">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-176">-Id</span><span class="sxs-lookup"><span data-stu-id="a8cac-176">-Id</span></span>
<span data-ttu-id="a8cac-177">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-177">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-178">-작업</span><span class="sxs-lookup"><span data-stu-id="a8cac-178">-Job</span></span>
<span data-ttu-id="a8cac-179">이 cmdlet이 작업을 만드는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="a8cac-180">**Pscloudjob** 개체를 가져오려면 Get-AzBatchJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="a8cac-181">-JobId</span></span>
<span data-ttu-id="a8cac-182">이 cmdlet이 작업을 만드는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-183">-MultiInstanceSettings</span><span class="sxs-lookup"><span data-stu-id="a8cac-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="a8cac-184">다중 인스턴스 작업을 실행 하는 방법에 대 한 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-184">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-185">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="a8cac-185">-OutputFile</span></span>
<span data-ttu-id="a8cac-186">명령줄을 실행 한 후 계산 노드에서 일괄 처리 서비스를 업로드할 파일 목록을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="a8cac-187">다중 인스턴스 작업의 경우 기본 작업이 실행 되는 계산 노드에서만 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="a8cac-188">-ResourceFiles</span></span>
<span data-ttu-id="a8cac-189">작업에 필요한 리소스 파일을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="a8cac-190">키는 리소스 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-190">The key is the resource file path.</span></span>
<span data-ttu-id="a8cac-191">값은 리소스 파일 blob 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-191">The value is the resource file blob source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSResourceFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-192">-작업</span><span class="sxs-lookup"><span data-stu-id="a8cac-192">-Tasks</span></span>
<span data-ttu-id="a8cac-193">추가할 작업 컬렉션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="a8cac-194">각 작업에는 고유 ID가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-194">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="a8cac-195">-UserIdentity</span></span>
<span data-ttu-id="a8cac-196">작업이 실행 되는 사용자 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cac-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cac-197">CommonParameters</span></span>
<span data-ttu-id="a8cac-198">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a8cac-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cac-199">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a8cac-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cac-200">입력</span><span class="sxs-lookup"><span data-stu-id="a8cac-200">INPUTS</span></span>

### <span data-ttu-id="a8cac-201">Microsoft.Azure.Commands.Batch. PSCloudJob 모델</span><span class="sxs-lookup"><span data-stu-id="a8cac-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="a8cac-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a8cac-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a8cac-203">출력</span><span class="sxs-lookup"><span data-stu-id="a8cac-203">OUTPUTS</span></span>

### <span data-ttu-id="a8cac-204">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a8cac-204">System.Void</span></span>

## <span data-ttu-id="a8cac-205">상속자</span><span class="sxs-lookup"><span data-stu-id="a8cac-205">NOTES</span></span>

## <span data-ttu-id="a8cac-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8cac-206">RELATED LINKS</span></span>

[<span data-ttu-id="a8cac-207">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a8cac-207">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a8cac-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="a8cac-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="a8cac-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a8cac-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="a8cac-210">새로운 AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a8cac-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="a8cac-211">제거-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a8cac-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="a8cac-212">중지-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="a8cac-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="a8cac-213">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a8cac-213">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

