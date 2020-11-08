---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214246"
---
# <span data-ttu-id="a1111-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a1111-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="a1111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1111-102">SYNOPSIS</span></span>
<span data-ttu-id="a1111-103">Azure Site Recovery 복제 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="a1111-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1111-104">SYNTAX</span></span>

### <span data-ttu-id="a1111-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1111-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1111-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a1111-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1111-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a1111-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1111-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a1111-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1111-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a1111-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1111-110">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="a1111-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1111-111">설명은</span><span class="sxs-lookup"><span data-stu-id="a1111-111">DESCRIPTION</span></span>
<span data-ttu-id="a1111-112">**업데이트 AzRecoveryServicesAsrPolicy** cmdlet은 지정 된 Azure Site Recovery 복제 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="a1111-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a1111-113">EXAMPLES</span></span>

### <span data-ttu-id="a1111-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="a1111-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="a1111-115">지정 된 매개 변수를 사용 하 여 복제 정책 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a1111-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="a1111-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="a1111-117">지정 된 매개 변수를 사용 하 여 azure to azure 복제 정책 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a1111-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="a1111-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="a1111-119">지정 된 매개 변수를 사용 하 여 azure to azure 복제 정책을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a1111-120">변수</span><span class="sxs-lookup"><span data-stu-id="a1111-120">PARAMETERS</span></span>

### <span data-ttu-id="a1111-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="a1111-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="a1111-122">응용 프로그램 일치 복구 지점을 만들 빈도 (시간)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="a1111-123">-인증</span><span class="sxs-lookup"><span data-stu-id="a1111-123">-Authentication</span></span>
<span data-ttu-id="a1111-124">사용 되는 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a1111-125">-AzureToAzure</span></span>
<span data-ttu-id="a1111-126">Azure에서 Azure 재해 복구를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-126">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a1111-127">-AzureToVMware</span></span>
<span data-ttu-id="a1111-128">Azure에서 vMWare 재해 복구를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-128">Specifies the Azure to vMWare disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-129">-압축</span><span class="sxs-lookup"><span data-stu-id="a1111-129">-Compression</span></span>
<span data-ttu-id="a1111-130">압축을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1111-131">-DefaultProfile</span></span>
<span data-ttu-id="a1111-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a1111-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a1111-133">-HyperVToAzure</span></span>
<span data-ttu-id="a1111-134">지정 된 정책이 Azure에 Hyper-v 가상 컴퓨터를 복제 하는 데 사용 됨을 나타내는 Switch 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1111-135">-InputObject</span></span>
<span data-ttu-id="a1111-136">Cmdlet에 대 한 Input 개체: 업데이트할 복제 정책에 해당 하는 ASR 복제 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="a1111-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="a1111-138">정책에 대 한 multiVm 동기화 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="a1111-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="a1111-140">유지할 번호 복구 지점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a1111-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a1111-142">복제 대상의 Azure storage 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="a1111-143">New-AzRecoveryServicesASRReplicationProtectedItem cmdlet을 사용 하 여 복제를 사용 하도록 설정 하는 동안 대체가 제공 되지 않은 경우 복제 대상 저장소 계정으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="a1111-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="a1111-145">생성 후 복구 지점을 유지 하는 시간 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="a1111-146">-ReplicaDeletion</span></span>
<span data-ttu-id="a1111-147">VMM 관리 사이트에서 다른 복제를 사용 하지 않도록 설정할 때 복제 가상 컴퓨터를 삭제할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="a1111-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="a1111-149">복제 빈도 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="a1111-150">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-150">Valid values are:</span></span>

- <span data-ttu-id="a1111-151">30</span><span class="sxs-lookup"><span data-stu-id="a1111-151">30</span></span>
- <span data-ttu-id="a1111-152">300</span><span class="sxs-lookup"><span data-stu-id="a1111-152">300</span></span>
- <span data-ttu-id="a1111-153">900</span><span class="sxs-lookup"><span data-stu-id="a1111-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="a1111-154">-ReplicationMethod</span></span>
<span data-ttu-id="a1111-155">복제 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="a1111-156">-ReplicationPort</span></span>
<span data-ttu-id="a1111-157">복제에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="a1111-158">-ReplicationStartTime</span></span>
<span data-ttu-id="a1111-159">복제 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-159">Specifies the replication start time.</span></span>
<span data-ttu-id="a1111-160">작업의 시작 부분에서 24 시간 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="a1111-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="a1111-162">경고가 표시 되는 RPO 임계값 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="a1111-163">-VmmToVmm</span></span>
<span data-ttu-id="a1111-164">지정 된 정책이 두 개의 Hyper-v 사이트 간에 VMM 관리 Hyper-v 가상 컴퓨터를 복제 하는 데 사용 됨을 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a1111-165">-VMwareToAzure</span></span>
<span data-ttu-id="a1111-166">지정 된 정책이 Azure에 VMware 가상 머신을 복제 하는 데 사용 됨을 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1111-167">-확인</span><span class="sxs-lookup"><span data-stu-id="a1111-167">-Confirm</span></span>
<span data-ttu-id="a1111-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1111-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1111-169">-WhatIf</span></span>
<span data-ttu-id="a1111-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1111-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1111-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1111-172">CommonParameters</span></span>
<span data-ttu-id="a1111-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1111-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1111-174">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a1111-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1111-175">입력</span><span class="sxs-lookup"><span data-stu-id="a1111-175">INPUTS</span></span>

### <span data-ttu-id="a1111-176">SiteRecovery. r i m g 정책</span><span class="sxs-lookup"><span data-stu-id="a1111-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a1111-177">출력</span><span class="sxs-lookup"><span data-stu-id="a1111-177">OUTPUTS</span></span>

### <span data-ttu-id="a1111-178">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="a1111-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a1111-179">상속자</span><span class="sxs-lookup"><span data-stu-id="a1111-179">NOTES</span></span>

## <span data-ttu-id="a1111-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1111-180">RELATED LINKS</span></span>