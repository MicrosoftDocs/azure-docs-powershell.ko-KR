---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: c401e5b4a85d8c994e96d77f39d646dabb74e02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528630"
---
# <span data-ttu-id="8fa1b-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8fa1b-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="8fa1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fa1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa1b-103">일괄 처리 서비스에서 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8fa1b-104">SYNTAX</span></span>

### <span data-ttu-id="8fa1b-105">CloudServiceAndTargetDedicated (기본값)</span><span class="sxs-lookup"><span data-stu-id="8fa1b-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fa1b-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="8fa1b-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa1b-107">CloudServiceAndAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="8fa1b-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fa1b-108">VirtualMachineAndAutoScale 크기 조정</span><span class="sxs-lookup"><span data-stu-id="8fa1b-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa1b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8fa1b-109">DESCRIPTION</span></span>
<span data-ttu-id="8fa1b-110">**새-AzureBatchPool** Cmdlet은 *batchcontext* 매개 변수에서 지정 하는 계정 아래에서 Azure 일괄 처리 서비스에 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="8fa1b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8fa1b-111">EXAMPLES</span></span>

### <span data-ttu-id="8fa1b-112">예제 1: CloudServiceConfiguration를 사용 하 여 TargetDedicated 매개 변수 집합을 사용 하 여 새 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="8fa1b-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="8fa1b-113">예제 2: VirtualMachineConfiguration를 사용 하 여 TargetDedicated 매개 변수 집합을 사용 하 여 새 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="8fa1b-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="8fa1b-114">이 명령은 TargetDedicated 매개 변수 집합을 사용 하 여 ID MyPool 인 새 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="8fa1b-115">대상 할당은 3 개의 계산 노드입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="8fa1b-116">풀은 제품군 4의 최신 운영 체제 버전으로 이미지 된 작은 가상 컴퓨터를 사용 하도록 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="8fa1b-117">예제 3: 자동 크기 조정 매개 변수 집합을 사용 하 여 새 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="8fa1b-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="8fa1b-118">이 명령은 자동 크기 조정 매개 변수 집합을 사용 하 여 ID AutoScalePool 인 새 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="8fa1b-119">풀은 최신 운영 체제 버전의 패밀리 4를 사용 하 여 이미지를 지정 하 고, 대상 계산 노드의 수는 자동 크기 조정 수식에 의해 결정 됨을 기준으로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="8fa1b-120">예제 4: 서브넷에 노드가 있는 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="8fa1b-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="8fa1b-121">예제 5: 사용자 지정 사용자 계정을 사용 하 여 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="8fa1b-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="8fa1b-122">변수</span><span class="sxs-lookup"><span data-stu-id="8fa1b-122">PARAMETERS</span></span>

### <span data-ttu-id="8fa1b-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="8fa1b-123">-ApplicationLicenses</span></span>
<span data-ttu-id="8fa1b-124">일괄 서비스는 풀의 각 계산 노드에서 사용할 수 있도록 하는 응용 프로그램 라이선스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="8fa1b-125">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="8fa1b-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="8fa1b-127">크기 자동 조정 수식에 따라 풀 크기가 자동으로 조정 되기 전 까지의 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="8fa1b-128">기본값은 15 분 이며 최소 값은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="8fa1b-129">-AutoScaleFormula</span></span>
<span data-ttu-id="8fa1b-130">자동으로 수영장의 크기를 조정 하는 수식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-130">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-131">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8fa1b-131">-BatchContext</span></span>
<span data-ttu-id="8fa1b-132">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8fa1b-133">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-133">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8fa1b-134">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-134">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8fa1b-135">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8fa1b-136">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8fa1b-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="8fa1b-137">-CertificateReferences</span></span>
<span data-ttu-id="8fa1b-138">풀과 연결 된 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="8fa1b-139">일괄 처리 서비스는 풀의 각 계산 노드에 참조 된 인증서를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa1b-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="8fa1b-141">Azure 클라우드 서비스 플랫폼에 따라 풀에 대 한 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa1b-142">-DefaultProfile</span></span>
<span data-ttu-id="8fa1b-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa1b-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8fa1b-144">-DisplayName</span></span>
<span data-ttu-id="8fa1b-145">풀의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="8fa1b-146">-Id</span><span class="sxs-lookup"><span data-stu-id="8fa1b-146">-Id</span></span>
<span data-ttu-id="8fa1b-147">만들 풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-147">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="8fa1b-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="8fa1b-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="8fa1b-149">이 cmdlet이 전용 계산 노드 간의 직접적인 통신을 위해 풀을 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="8fa1b-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="8fa1b-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="8fa1b-151">단일 계산 노드에서 실행할 수 있는 최대 작업 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="8fa1b-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8fa1b-152">-Metadata</span></span>
<span data-ttu-id="8fa1b-153">새 풀에 추가할 메타 데이터를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="8fa1b-154">키는 메타 데이터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-154">The key is the metadata name.</span></span>
<span data-ttu-id="8fa1b-155">값은 메타 데이터 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-155">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa1b-156">-NetworkConfiguration</span></span>
<span data-ttu-id="8fa1b-157">풀에 대 한 네트워크 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-157">The network configuration for the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8fa1b-158">-ResizeTimeout</span></span>
<span data-ttu-id="8fa1b-159">풀에 계산 노드를 할당 하는 시간 초과를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="8fa1b-160">-StartTask</span></span>
<span data-ttu-id="8fa1b-161">풀에 대 한 작업 시작 사양을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="8fa1b-162">계산 노드가 풀을 조인 하거나 계산 노드가 다시 부팅 되거나 reimaged 경우 시작 작업이 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="8fa1b-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="8fa1b-164">풀에 할당할 전용 계산 노드의 대상 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="8fa1b-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="8fa1b-166">풀에 할당할 우선 순위가 낮은 계산 노드의 대상 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="8fa1b-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="8fa1b-168">ComputeNodeFillType 같은 작업 일정 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-169">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="8fa1b-169">-UserAccount</span></span>
<span data-ttu-id="8fa1b-170">풀의 각 노드에 만들 사용자 계정의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-170">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fa1b-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="8fa1b-172">가상 컴퓨터 인프라의 풀에 대 한 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1b-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="8fa1b-173">-VirtualMachineSize</span></span>
<span data-ttu-id="8fa1b-174">풀의 가상 컴퓨터 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="8fa1b-175">가상 컴퓨터 크기에 대 한 자세한 내용은 https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure 사이트의 가상 컴퓨터 크기를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="8fa1b-176">-확인</span><span class="sxs-lookup"><span data-stu-id="8fa1b-176">-Confirm</span></span>
<span data-ttu-id="8fa1b-177">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa1b-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa1b-178">-WhatIf</span></span>
<span data-ttu-id="8fa1b-179">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fa1b-180">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fa1b-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa1b-181">CommonParameters</span></span>
<span data-ttu-id="8fa1b-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fa1b-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa1b-183">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa1b-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa1b-184">입력</span><span class="sxs-lookup"><span data-stu-id="8fa1b-184">INPUTS</span></span>

### <span data-ttu-id="8fa1b-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8fa1b-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="8fa1b-186">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8fa1b-186">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="8fa1b-187">출력</span><span class="sxs-lookup"><span data-stu-id="8fa1b-187">OUTPUTS</span></span>

### <span data-ttu-id="8fa1b-188">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="8fa1b-188">System.Void</span></span>

## <span data-ttu-id="8fa1b-189">상속자</span><span class="sxs-lookup"><span data-stu-id="8fa1b-189">NOTES</span></span>

## <span data-ttu-id="8fa1b-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fa1b-190">RELATED LINKS</span></span>

[<span data-ttu-id="8fa1b-191">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8fa1b-191">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8fa1b-192">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8fa1b-192">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="8fa1b-193">-AzureBatchPool 제거</span><span class="sxs-lookup"><span data-stu-id="8fa1b-193">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="8fa1b-194">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8fa1b-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

