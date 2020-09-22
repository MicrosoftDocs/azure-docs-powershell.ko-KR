---
title: Azure PowerShell 릴리스 정보
description: Azure PowerShell 모듈의 모든 최신 업데이트에 대해 알아봅니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244231"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="178c1-103">Azure PowerShell 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="178c1-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="178c1-104">4.6.1 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="178c1-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="178c1-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-105">Az.Compute</span></span>
* <span data-ttu-id="178c1-106">'New-AzVm'에서 '-EncryptionAtHost' 매개 변수를 패치하여 기본값인 false가 제거됨[#12776]</span><span class="sxs-lookup"><span data-stu-id="178c1-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="178c1-107">4.6.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="178c1-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-108">Az.Accounts</span></span>
* <span data-ttu-id="178c1-109">검색 엔드포인트가 기본 AzureCloud나 기타 공용 환경을 반환하지 않는 경우 모든 퍼블릭 클라우드 환경이 로드됨 [#12633]</span><span class="sxs-lookup"><span data-stu-id="178c1-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="178c1-110">'Get-AzSubscription'에서 SubscriptionPolicies가 노출됨 [#12551]</span><span class="sxs-lookup"><span data-stu-id="178c1-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-111">Az.Automation</span></span>
* <span data-ttu-id="178c1-112">Hybrid Worker 그룹을 지정하기 위해 'Set-AzAutomationWebhook'에 '-RunOn' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-113">Az.Compute</span></span>
* <span data-ttu-id="178c1-114">'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', 'Update-AzVmss'에 '-EncryptionAtHost' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="178c1-115">'Get-AzVM' 및 'Get-AzVmss' 반환 개체에 'SecurityProfile'이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="178c1-116">'-InstanceView' 스위치가 'Get-AzHostGroup'에 선택적 매개 변수로 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="178c1-117">새 cmdlet 'Invoke-AzVmPatchAssessment'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-118">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-119">PSPipelineRun 클래스에 누락된 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-120">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-121">호스트 기능에서 암호화를 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-122">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-123">일시 삭제 사용 안 함 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="178c1-124">특성 SecretValueText 제거 계획에 대한 경고 메시지가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="178c1-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="178c1-125">Az.Maintenance</span></span>
* <span data-ttu-id="178c1-126">'New-AzMaintenanceConfiguration'에 선택적 일정 관련 필드가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="178c1-127">'Get-AzMaintenancePublicConfiguration'에 대한 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="178c1-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="178c1-128">Az.ManagedServices</span></span>
* <span data-ttu-id="178c1-129">관리되는 서비스 할당 및 정의의 cmdlet에 대한 호환성이 손상되는 변경 경고가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-130">Az.Monitor</span></span>
* <span data-ttu-id="178c1-131">로그 및 메트릭 사용을 분리하기 위해 'Set-AzDiagnosticSetting'에 설정된 매개 변수가 확장됨 [#12482]</span><span class="sxs-lookup"><span data-stu-id="178c1-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="178c1-132">파이프라인에서 메트릭 경고를 가져오는 경우 'Add-AzMetricAlertRuleV2'에 대한 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-133">Az.Resources</span></span>
* <span data-ttu-id="178c1-134">Azure Policy를 통해 별칭을 수정할 수 있는지 여부를 나타내는 정보를 포함하도록 'Get-AzPolicyAlias' 응답이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="178c1-135">새 cmdlet 'Set-AzRoleAssignment'가 생성됨</span><span class="sxs-lookup"><span data-stu-id="178c1-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="178c1-136">관리 그룹 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzDeploymentManagementGroupWhatIfResult'가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="178c1-137">테넌트 범위에서 ARM 템플릿 What-If 결과를 가져오는 'Get-AzTenantWhatIfResult' 새 cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="178c1-138">ARM 템플릿 What-If 결과를 사용하도록 'New-AzManagementGroupDeployment' 및 'New-AzTenantDeployment'에 대한 '-WhatIf' 및 '-Confirm'이 재정의됨</span><span class="sxs-lookup"><span data-stu-id="178c1-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="178c1-139">새 배포 cmdlet에 대한 '-WhatIf' 및 '-Confirm' 동작이 False를 준수하도록 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="178c1-140">'-TemplateObject' 및 'TemplateParameterObject'에 대한 직렬화 오류가 수정됨 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="178c1-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="178c1-141">예정된 출력 형식 변경을 위해 'Get-AzResourceGroupDeploymentOperation'에 호환성이 손상되는 변경 특성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="178c1-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="178c1-142">Az.SignalR</span></span>
* <span data-ttu-id="178c1-143">'Restart-AzSignalR' 및 'Update-AzSignalR' 도움말 파일 오류가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="178c1-144">'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream' cmdlet이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-145">Az.Storage</span></span>
* <span data-ttu-id="178c1-146">지원되는 Blob 쿼리 가속</span><span class="sxs-lookup"><span data-stu-id="178c1-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="178c1-147">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="178c1-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="178c1-148">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="178c1-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="178c1-149">도움말 파일 업데이트, 자세한 설명 추가 및 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="178c1-150">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="178c1-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="178c1-151">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="178c1-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="178c1-152">관련 하위 디렉터리가 없는 경우 Blob 다운로드 실패가 수정됨 [#12592]</span><span class="sxs-lookup"><span data-stu-id="178c1-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="178c1-153">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="178c1-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="178c1-154">스토리지 계정에 대해 개체 복제 정책 설정/가져오기/제거가 지원됨</span><span class="sxs-lookup"><span data-stu-id="178c1-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="178c1-155">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="178c1-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="178c1-156">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="178c1-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="178c1-157">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="178c1-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="178c1-158">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="178c1-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="178c1-159">스토리지 계정의 Blob Service에서 ChangeFeed 사용/사용 안 함이 지원됨</span><span class="sxs-lookup"><span data-stu-id="178c1-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="178c1-160">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="178c1-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="178c1-161">4.5.0 - 2020년 8월</span><span class="sxs-lookup"><span data-stu-id="178c1-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-162">Az.Accounts</span></span>
* <span data-ttu-id="178c1-163">매개 변수 'MaxContextPopulation'을 허용하도록 'Connect-AzAccount' 업데이트됨 [# 9865]</span><span class="sxs-lookup"><span data-stu-id="178c1-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="178c1-164">SubscriptionClient 버전이 2019-06-01로 업데이트되고 테넌트 도메인을 표시 [#9838]</span><span class="sxs-lookup"><span data-stu-id="178c1-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="178c1-165">구독의 managedBy 테넌트 정보 및 홈 테넌트 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="178c1-166">원격 분석 데이터의 모듈 이름, 버전 정보 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="178c1-167">환경 메타데이터 엔드포인트가 호환되지 않는 값을 반환하는 경우 SqlDatabaseDnsSuffix 및 ServiceManagementUrl이 조정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="178c1-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="178c1-168">Az.Aks</span></span>
* <span data-ttu-id="178c1-169">'ClientIdAndSecret'을 'ServicePrincipalIdAndSecret'으로 제거하고 'ClientIdAndSecret'을 별칭으로 설정함 [#12381]</span><span class="sxs-lookup"><span data-stu-id="178c1-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="178c1-170">'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks'를 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster'로 제거하고 원본을 별칭으로 설정함 [#12373].</span><span class="sxs-lookup"><span data-stu-id="178c1-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-171">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-172">새 'Add-AzApiManagementApiToGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="178c1-173">새 'Get-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="178c1-174">새 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="178c1-175">새 'Get-AzApiManagementGatewayKey' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="178c1-176">새 'New-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="178c1-177">새 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="178c1-178">새 'New-AzApiManagementResourceLocationObject' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="178c1-179">새 'Remove-AzApiManagementApiFromGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="178c1-180">새 'Remove-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="178c1-181">새 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="178c1-182">새 'Update-AzApiManagementGateway' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="178c1-183">'Get-AzApiManagementApi' cmdlet에 선택적 [-GatewayId] 매개 변수가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-185">'Deny'가 특히 NetworkRules 기본 작업으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-186">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-187">Enum.Parse가 null 값을 Enabled 또는 Disabled 열거형 값으로 강제 변환하려는 경우 예외가 throw되는 문제를 수정했습니다. [#12344]</span><span class="sxs-lookup"><span data-stu-id="178c1-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-188">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-189">전송 중 암호화 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="178c1-190">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="178c1-191">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'EncryptionInTransit' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="178c1-192">프라이빗 링크 기능을 사용하여 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="178c1-193">cmdlet 'New-AzHDInsightCluster'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="178c1-194">cmdlet 'New-AzHDInsightClusterConfig'에 새 매개 변수 'PublicNetworkAccessType' 및 'OutboundPublicNetworkAccessType' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="178c1-195">'New-AzHDInsightCluster' 또는 'Get-AzHDInsightCluster'를 호출하는 경우 가상 네트워크 정보가 반환됨</span><span class="sxs-lookup"><span data-stu-id="178c1-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-196">Az.Network</span></span>
* <span data-ttu-id="178c1-197">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="178c1-198">작업을 중단하지 않는 변경이 추가됨: 'Remove-AzExpressRouteCircutPeeringConfig'의 프라이빗 피어링을 위한 PeerAddressType 기능</span><span class="sxs-lookup"><span data-stu-id="178c1-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="178c1-199">AddressPrefixType 및 PeerAddressType 매개 변수의 대/소문자를 무시하도록 코드가 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="178c1-200">'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' 및 'New-AzPublicIpPrefix'에 대한 경고 메시지를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-202">'Remove-AzOperationalInsightsworkspace'에 대한 '-ForceDelete' 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="178c1-203">새 cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="178c1-204">새 cmdlet 'Restore-AzOperationalInsightsWorkspace'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-206">Azure Backup 컨테이너/항목 검색 환경이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-207">Az.Resources</span></span>
* <span data-ttu-id="178c1-208">'New-AzRoleAssignment'에 'Condition', 'ConditionVersion' 및 'Description' 속성을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="178c1-209">여기에는 데이터 모델과 관련된 모든 변경 사항이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-210">Az.Sql</span></span>
* <span data-ttu-id="178c1-211">'New-AzSqlServer' 'Set-AzSqlServer'에서 서버 이름 대/소문자를 구분하지 않는 잠재적인 오류를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="178c1-212">'New-AzSqlDatabaseSecondary'의 기존 데이터베이스 오류에서 반환되는 잘못된 데이터베이스 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-213">Az.Storage</span></span>
* <span data-ttu-id="178c1-214">새 권한 x,t를 사용하여 컨테이너/blob Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="178c1-215">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="178c1-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="178c1-216">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="178c1-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="178c1-217">새 권한 x,t,f를 사용하여 계정 Sas 토큰 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="178c1-218">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="178c1-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="178c1-219">단일 파일 사용량 공유 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="178c1-220">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="178c1-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="178c1-221">4.4.0 - 2020년 7월</span><span class="sxs-lookup"><span data-stu-id="178c1-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-222">Az.Accounts</span></span>
* <span data-ttu-id="178c1-223">새 cmdlet 'Invoke-AzRestMethod' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="178c1-224">'Start-Job'을 사용하여 여러 Azure PowerShell cmdlet을 실행하는 등 다중 프로세스 시나리오에서 인증 오류를 발생시킬 수 있는 문제 해결 [#9448]</span><span class="sxs-lookup"><span data-stu-id="178c1-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="178c1-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="178c1-225">Az.Aks</span></span>
* <span data-ttu-id="178c1-226">'Get-AzAks'가 모든 클러스터를 가져오지 않는 버그 수정 [#12296]</span><span class="sxs-lookup"><span data-stu-id="178c1-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="178c1-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="178c1-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="178c1-228">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-229">Az.Automation</span></span>
* <span data-ttu-id="178c1-230">이스케이프 문자를 포함하는 문자열을 json 개체로 변환할 수 없는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-231">Az.Compute</span></span>
* <span data-ttu-id="178c1-232">'latest' 이미지 버전이 없는 'New-AzVmss'를 사용하는 경우 경고 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-233">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-234">Data Factory에 대한 전역 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="178c1-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="178c1-235">Az.EventGrid</span></span>
* <span data-ttu-id="178c1-236">2020-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="178c1-237">추가된 새로운 기능:</span><span class="sxs-lookup"><span data-stu-id="178c1-237">Added new features:</span></span>
    - <span data-ttu-id="178c1-238">입력 매핑</span><span class="sxs-lookup"><span data-stu-id="178c1-238">Input mapping</span></span>
    - <span data-ttu-id="178c1-239">이벤트 배달 스키마</span><span class="sxs-lookup"><span data-stu-id="178c1-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="178c1-240">Private Link</span><span class="sxs-lookup"><span data-stu-id="178c1-240">Private Link</span></span>
    - <span data-ttu-id="178c1-241">클라우드 이벤트 V10 스키마</span><span class="sxs-lookup"><span data-stu-id="178c1-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="178c1-242">대상으로 Service Bus 항목</span><span class="sxs-lookup"><span data-stu-id="178c1-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="178c1-243">대상으로 Azure 함수</span><span class="sxs-lookup"><span data-stu-id="178c1-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="178c1-244">WebHook 일괄 처리</span><span class="sxs-lookup"><span data-stu-id="178c1-244">WebHook Batching</span></span>
    - <span data-ttu-id="178c1-245">보안 웹후크(AAD 지원)</span><span class="sxs-lookup"><span data-stu-id="178c1-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="178c1-246">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="178c1-246">IpFiltering</span></span>
* <span data-ttu-id="178c1-247">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="178c1-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="178c1-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="178c1-249">웹후크 일괄 처리를 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="178c1-250">AAD를 사용하여 보안 웹후크를 지원하는 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="178c1-251">Azure 함수 및 Service Bus 항목을 새 대상으로 지원하기 위해 EndpointType 매개 변수에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="178c1-252">배달 스키마에 대한 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="178c1-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 및 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="178c1-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="178c1-254">IpFiltering을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="178c1-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="178c1-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="178c1-256">입력 매핑을 지원하기 위해 새로운 선택적 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-257">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-258">API 2020-05-01을 사용하도록 업데이트된 모듈</span><span class="sxs-lookup"><span data-stu-id="178c1-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="178c1-259">Storage, Keyvault 및 Web App Service 리소스에 대한 프라이빗 링크 지원을 추가함</span><span class="sxs-lookup"><span data-stu-id="178c1-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-260">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-261">국가 클라우드에서 ADLSGen1/2 스토리지로 클러스터를 만드는 것이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-262">Az.Monitor</span></span>
* <span data-ttu-id="178c1-263">메트릭 또는 로그가 null인 경우 'Get-AzDiagnosticSetting'에 대한 버그 수정 [#12272]</span><span class="sxs-lookup"><span data-stu-id="178c1-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-264">Az.Network</span></span>
* <span data-ttu-id="178c1-265">VWan HubVnet 연결의 매개 변수 교환 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="178c1-266">Azure Network Virtual Appliance 사이트에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="178c1-267">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="178c1-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="178c1-268">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="178c1-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="178c1-269">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="178c1-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="178c1-270">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="178c1-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="178c1-271">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="178c1-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="178c1-272">Azure Network Virtual Appliance에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="178c1-273">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="178c1-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="178c1-274">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="178c1-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="178c1-275">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="178c1-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="178c1-276">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="178c1-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="178c1-277">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="178c1-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="178c1-278">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="178c1-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="178c1-279">Application Gateway를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="178c1-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="178c1-280">StorageSync를 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="178c1-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="178c1-281">SignalR을 Private Link 공통 cmdlet에 온보딩</span><span class="sxs-lookup"><span data-stu-id="178c1-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-283">인증에 대한 프로젝트 참조 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="178c1-284">Azure Backup 튜닝 cmdlet은 텍스트를 보다 정확하게 작성하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="178c1-285">Azure Backup은 'Get-AzRecoveryServicesBackupJob' cmdlet을 사용하여 MAB 에이전트 작업을 가져오는 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-286">Az.Resources</span></span>
* <span data-ttu-id="178c1-287">SDK를 사용하도록 'Save-AzResourceGroupDeploymentTemplate'을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="178c1-288">'Unregister-AzResourceProvider' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-289">Az.Sql</span></span>
* <span data-ttu-id="178c1-290">Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet에서 서비스 주체 및 게스트 사용자에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="178c1-291">데이터 분류 cmdlet의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="178c1-292">다음의 Azure SQL Managed Instance 장애 조치에 대한 지원 추가: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="178c1-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-293">Az.Storage</span></span>
* <span data-ttu-id="178c1-294">일부 데이터 평면 cmdlet에 대해 UserAgent가 추가되지 않는 문제를 해결했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="178c1-295">MinimumTlsVersion 및 AllowBlobPublicAccess로 스토리지 계정 만들기/업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="178c1-296">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="178c1-297">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="178c1-298">스토리지 계정의 Blob Service에서 버전 관리 사용/사용 안 함 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="178c1-299">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="178c1-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="178c1-300">Blob 버전 관리로 Blob 나열 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="178c1-301">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="178c1-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="178c1-302">단일 Blob 스냅샷 또는 Blob 버전 가져오기/제거 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="178c1-303">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="178c1-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="178c1-304">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="178c1-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="178c1-305">Azure.Storage.Blobs V12에서 생성된 Blob 개체의 파이프라인 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="178c1-306">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="178c1-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="178c1-307">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="178c1-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="178c1-308">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="178c1-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="178c1-309">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="178c1-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="178c1-310">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="178c1-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="178c1-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="178c1-311">Az.StorageSync</span></span>
* <span data-ttu-id="178c1-312">ApiVersion 2020-03-01을 대상으로 하는 새 버전의 StorageSync SDK 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="178c1-313">스토리지 동기화 서비스 업데이트 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="178c1-314">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="178c1-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="178c1-315">IncomingTrafficPolicy 및 PrivateEndpointConnections가 StorageSyncService cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-316">Az.Websites</span></span>
* <span data-ttu-id="178c1-317">App Service 계획과 동일한 리소스 그룹에 속하지 않는 슬롯에 대한 작업을 수행하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="178c1-318">4.3.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="178c1-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-319">Az.Accounts</span></span>
* <span data-ttu-id="178c1-320">기본적으로 환경 검색 설정이 지원되며 'Add-AzEnvironment'를 통해 환경을 추가할 수 있음</span><span class="sxs-lookup"><span data-stu-id="178c1-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="178c1-321">미리 로드된 어셈블리 업데이트 [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="178c1-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="178c1-322">Azure.Core 어셈블리 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="178c1-323">다중 스레드 실행에서 'Connect-AzAccount'가 실패할 수 있는 문제 해결 [#11201]</span><span class="sxs-lookup"><span data-stu-id="178c1-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="178c1-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="178c1-324">Az.Aks</span></span>
* <span data-ttu-id="178c1-325">이전에 사용하던 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile)를 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 및 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 호출로 대체</span><span class="sxs-lookup"><span data-stu-id="178c1-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-326">Az.Batch</span></span>
* <span data-ttu-id="178c1-327">'Microsoft.Azure.Management.Batch' SDK 버전 11.0.0을 사용하도록 Az.Batch 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="178c1-328">'New-AzBatchAccount' cmdlet에서 BatchAccount ID를 설정하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-330">계정 기능 표시 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="178c1-331">PublicNetworkAccess 수정 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-332">Az.Compute</span></span>
* <span data-ttu-id="178c1-333">Set-AzVM 및 Set-AzVmssVM cmdlet에 SimulateEviction 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="178c1-334">AzGalleryImageVersion cmdlet에 대한 StorageAccountType 매개 변수의 인수 완성자에 'Premium_LRS' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="178c1-335">VMCustomScriptExtension에 Substatuses 추가 [#11297]</span><span class="sxs-lookup"><span data-stu-id="178c1-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="178c1-336">New-AzVM 및 New-AzVMConfig cmdlet에 대한 EvictionPolicy 매개 변수의 인수 완성자에 'Delete' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="178c1-337">새 SAP용 VM 확장의 이름 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-338">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-339">ADF .Net SDK 버전을 4.9.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-340">Az.EventHub</span></span>
* <span data-ttu-id="178c1-341">'New-AzEventHubNamespace' 및 'Set-AzEventHubNamespace' cmdlet에 관리 ID 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="178c1-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="178c1-342">Az.Functions</span></span>
* <span data-ttu-id="178c1-343">PowerShell 7.0 및 Java 11 함수 앱을 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-344">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-345">호스트를 나열하고 HDInsight 클러스터의 특정 호스트를 다시 시작하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="178c1-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="178c1-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="178c1-347">SDK 버전을 1.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="178c1-348">설정 및 관리 ID 내보내기에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-349">Az.Monitor</span></span>
* <span data-ttu-id="178c1-350">'Set-AzActivityLogAlert'에 대한 입력 개체 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="178c1-351">'Set-AzActionGroup'에 대한 'InputObject' 매개 변수 수정 [#10868]</span><span class="sxs-lookup"><span data-stu-id="178c1-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-352">Az.Network</span></span>
* <span data-ttu-id="178c1-353">'Remove-AzExpressRouteCircuitConnectionConfig'에 AddressPrefixType 매개 변수 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="178c1-354">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="178c1-355">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="178c1-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="178c1-356">방화벽 정책에 대한 네트워크 규칙에서 대상 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="178c1-357">백 엔드 주소 풀 작업에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="178c1-358">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="178c1-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="178c1-359">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="178c1-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="178c1-360">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="178c1-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="178c1-361">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="178c1-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="178c1-362">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="178c1-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="178c1-363">'New-AzIpGroup'에 대한 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="178c1-364">Azure FirewallPolicy에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="178c1-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="178c1-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="178c1-366">기능에 대한 새로운 명령이 업데이트됨: VirtualWan P2SVpnGateway에서 사용자 지정 dns 서버 설정/제거</span><span class="sxs-lookup"><span data-stu-id="178c1-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="178c1-367">New-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="178c1-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="178c1-368">Update-AzP2sVpnGateway 업데이트됨: 고객이 P2SVpnGateway에 설정할 dns 서버를 지정할 수 있는 선택적 매개 변수 '-CustomDnsServer'가 추가되었으며, 이 매개 변수는 지점 및 사이트 간 클라이언트에서 사용 가능</span><span class="sxs-lookup"><span data-stu-id="178c1-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="178c1-369">'Update-AzVpnGateway' 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="178c1-370">고객이 VpnGateway에 설정할 사용자 지정 bgps를 지정할 수 있도록 선택적 매개 변수 '-BgpPeeringAddress' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="178c1-371">VirtualHub 리소스의 라우팅 상태 초기화를 지원하는 새 cmdlet 추가:</span><span class="sxs-lookup"><span data-stu-id="178c1-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="178c1-372">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="178c1-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="178c1-373">방화벽 정책에 대한 최근 Swagger 변화에 따라 아래 항목 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="178c1-374">RuleGroup, RuleCollectionGroup 및 RuleType의 이름 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="178c1-375">여러 NAT 규칙 컬렉션을 지원하도록 방화벽 정책 NAT 규칙 컬렉션에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="178c1-376">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 및 'New-AzFirewallPolicyNetworkRule'에 대한 필수 매개 변수 'SourceIpGroup' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="178c1-377">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="178c1-378">[호환성이 손상되는 변경] 'New-AzFirewallPolicyApplicationRule' 수정, 'SourceAddress' 매개 변수를 필수로 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="178c1-379">[호환성이 손상되는 변경] 다음 필수 매개 변수 제거: 'New-AzFirewallPolicyNatRuleCollection'의 'TranslatedAddress', 'TranslatedPort'</span><span class="sxs-lookup"><span data-stu-id="178c1-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="178c1-380">PrivateLink On Application Gateway를 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="178c1-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="178c1-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="178c1-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="178c1-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="178c1-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="178c1-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="178c1-387">VirtualHub의 HubRouteTables 자식 리소스에 대한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="178c1-388">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="178c1-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="178c1-389">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="178c1-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="178c1-390">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="178c1-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="178c1-391">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="178c1-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="178c1-392">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="178c1-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="178c1-393">VirtualWan의 사용자 지정 라우팅에 대한 선택적 RoutingConfiguration 입력 매개 변수를 지원하도록 기존 cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="178c1-394">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="178c1-395">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="178c1-396">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="178c1-397">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="178c1-398">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="178c1-399">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="178c1-400">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="178c1-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="178c1-401">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="178c1-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-403">PSWorkspace가 IOperationalInsightsWorkspace를 구현하지 않는 버그 수정 [#12135]</span><span class="sxs-lookup"><span data-stu-id="178c1-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="178c1-404">'Set-AzOperationalInsightsWorkspace'에서 'Sku' 매개 변수의 올바른 값 세트에 'pergb2018' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="178c1-405">매개 변수 'FunctionParameter'에 대한 별칭 'FunctionParameters' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="178c1-406">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="178c1-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="178c1-407">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="178c1-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-409">Azure Backup에서 MAB 항목을 가져오기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="178c1-410">Azure Site Recovery에서 'StandardSSD_LRS' 디스크 형식 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-411">Az.Resources</span></span>
* <span data-ttu-id="178c1-412">'PSADUser'에서 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' 추가 [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="178c1-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="178c1-413">'Get-AzADUser'에서 '-Mail'이 작동하지 않는 문제 해결 [#11981]</span><span class="sxs-lookup"><span data-stu-id="178c1-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="178c1-414">'Get-AzDeploymentWhatIfResult' 및 'Get-AzResourceGroupDeploymentWhatIfResult'에 '-ExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="178c1-415">'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 '-WhatIfExcludeChangeType' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="178c1-416">보다 나은 오류 메시지를 표시하도록 'Test-Az\*Deployment' cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="178c1-417">deployment create 및 What-If cmdlet의 '-Name' 매개 변수에 대한 도움말 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-418">Az.Sql</span></span>
* <span data-ttu-id="178c1-419">Set SQL Server Azure Active Directory Admin cmdlet의 서비스 주체에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="178c1-420">데이터 분류 cmdlet의 동기화 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="178c1-421">'Set-AzSqlServerActiveDirectoryAdministrator'에서 메일로 사용자 검색 지원 [#12192]</span><span class="sxs-lookup"><span data-stu-id="178c1-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-422">Az.Storage</span></span>
* <span data-ttu-id="178c1-423">RequireInfrastructureEncryption을 사용하여 스토리지 계정 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="178c1-424">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="178c1-425">Azure.Core 로딩 논리를 Az.Accounts로 이동</span><span class="sxs-lookup"><span data-stu-id="178c1-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-426">Az.Websites</span></span>
* <span data-ttu-id="178c1-427">'Restore-AzDeletedWebApp'에서 복원이 실패할 경우 생성된 웹앱을 삭제하는 보호 기능 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="178c1-428">'New-AzWebApp' 및 'New-AzWebAppSlot'에 대한 'SourceWebApp.Location' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="178c1-429">'Set-AzWebApp' 및 'Set-AzWebAppSlot'에서 컨테이너 설정을 변경할 수 없는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="178c1-430">Get-AzWebApp에 대한 -Name을 제공하지 않으면 SiteConfig를 가져오는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="178c1-431">Linux 앱용 ASP를 만드는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="178c1-432">리소스 그룹 간 복제에 대한 예외 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="178c1-433">4.2.0 - 2020년 6월</span><span class="sxs-lookup"><span data-stu-id="178c1-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-434">Az.Accounts</span></span>
* <span data-ttu-id="178c1-435">Azure Automation 또는 PowerShell 작업에서 Az가 로그를 건너뛸 수 있는 문제 수정[#11492]</span><span class="sxs-lookup"><span data-stu-id="178c1-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="178c1-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="178c1-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="178c1-437">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-438">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-439">서비스 관리 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="178c1-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="178c1-440">Az.Billing</span></span>
* <span data-ttu-id="178c1-441">소비 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-443">PrivateEndpoint 및 PublicNetworkAccess control을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-444">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-445">데이터 팩터리 V2 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="178c1-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="178c1-446">Az.DataShare</span></span>
* <span data-ttu-id="178c1-447">''Az.DataShare'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="178c1-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="178c1-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="178c1-449">''Az.DesktopVirtualization'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-451">SDK를 0.21.0으로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="178c1-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="178c1-452">다음에 선택적 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="178c1-453">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="178c1-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="178c1-454">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="178c1-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-456">'Start-AzPolicyComplianceScan'의 예제 3 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="178c1-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="178c1-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="178c1-458">PowerBI cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="178c1-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="178c1-459">Az.PrivateDns</span></span>
* <span data-ttu-id="178c1-460">Remove-AzPrivateDnsRecordSet에 대한 자세한 정보 출력 문자열 형식 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-462">xml 입력에서 영역 간 복제를 위한 복구 계획을 세우기 위한 Azure Site Recovery 지원.</span><span class="sxs-lookup"><span data-stu-id="178c1-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="178c1-463">SiteRecovery 및 Backup cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-464">Az.Resources</span></span>
* <span data-ttu-id="178c1-465">Get-AzDeploymentScriptLog 및 Save-AzDeploymentScriptLog cmdlet에 Tail 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="178c1-466">형식이 지정된 출력 속성을 Get-AzDeploymentScript cmdlet 출력에 표시</span><span class="sxs-lookup"><span data-stu-id="178c1-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="178c1-467">-DeploymentScriptInputObject 매개 변수의 이름이 -DeploymentScriptObject로 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="178c1-468">cmdlet 메시지에서 누락된 파일/대상 이름이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="178c1-469">리소스 관리자 및 태그 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-470">Az.Sql</span></span>
* <span data-ttu-id="178c1-471">UsePrivateLinkConnection을 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="178c1-472">SyncMemberAzureDatabaseResourceId를 'New-AzSqlSyncMember' 및 'Update-AzSqlSyncMember'에 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="178c1-473">SQL Server Azure Active Directory Admin cmdlet을 설정하는 게스트 사용자 조회 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-474">Az.Storage</span></span>
* <span data-ttu-id="178c1-475">데이터 평면 cmdlet의 어셈블리 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="178c1-476">4.1.0 - 2020년 5월</span><span class="sxs-lookup"><span data-stu-id="178c1-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="178c1-477">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-477">Highlights since the last release</span></span>
* <span data-ttu-id="178c1-478">지원되는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="178c1-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="178c1-479">Az.Functions 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="178c1-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources 및 Az.Storage의 주요 릴리스 출시</span><span class="sxs-lookup"><span data-stu-id="178c1-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-481">Az.Accounts</span></span>
* <span data-ttu-id="178c1-482">'AzureSynapseAnalyticsEndpointResourceId' 및 'AzureSynapseAnalyticsEndpointSuffix' 매개 변수를 허용하도록 'Add-AzEnvironment' 및 'Set-AzEnvironment' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="178c1-483">Az.Accounts에 Azure.Core 관련 어셈블리가 추가되었으며 지원되는 PowerShell 플랫폼은 Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="178c1-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="178c1-484">Az.Aks</span></span>
* <span data-ttu-id="178c1-485">API 버전을 2019-10-01로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="178c1-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="178c1-486">Windows 컨테이너를 사용하여 AKS 만들기 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="178c1-487">새 cmdlet 추가: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool', 'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="178c1-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-488">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-489">'New-AzApiManagement' 및 'Set-AzApiManagement': [-AssignIdentity] 매개 변수 이름을 [-SystemAssignedIdentity]로 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="178c1-490">'New-AzApiManagement' 및 'Set-AzApiManagement': 새 매개 변수 추가: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="178c1-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="178c1-491">'Get-AzApiManagementProperty': 'Get-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="178c1-492">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="178c1-493">'New-AzApiManagementProperty': 'New-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="178c1-494">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="178c1-495">'Set-AzApiManagementProperty': 'Set-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="178c1-496">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="178c1-497">'Remove-AzApiManagementProperty': 'Remove-AzApiManagementNamedValue'로 이름 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="178c1-498">PropertyId 매개 변수 이름을 NamedValueId로 변경.</span><span class="sxs-lookup"><span data-stu-id="178c1-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="178c1-499">새 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementAuthorizationServer'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="178c1-500">새 'Get-AzApiManagementNamedValueSecretValue' cmdlet이 추가되었으며 'Get-AzApiManagementNamedValue'는 더 이상 비밀 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="178c1-501">새 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet이 추가되었으며 'Get-AzApiManagementOpenIdConnectProvider'는 더 이상 클라이언트 암호를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="178c1-502">새 'Get-AzApiManagementSubscriptionKey' cmdlet이 추가되었으며 'Get-AzApiManagementSubscription'은 더 이상 구독 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="178c1-503">새 'Get-AzApiManagementTenantAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="178c1-504">새 'Get-AzApiManagementTenantGitAccessSecret' cmdlet이 추가되었으며 'Get-AzApiManagementTenantGitAccess'는 더 이상 키를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="178c1-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="178c1-506">매개 변수 추가: 'New-AzApplicationInsights'에 대한 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="178c1-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="178c1-507">'Update-AzApplicationInsights' cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="178c1-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="178c1-508">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="178c1-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-509">Az.Batch</span></span>
* <span data-ttu-id="178c1-510">'Microsoft.Azure.Batch' SDK 버전 13.0.0 및 'Microsoft.Azure.Management.Batch' SDK 버전 9.0.0을 사용하도록 Az.Batch가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="178c1-511">새 '-CertificateKind' 매개 변수를 사용하여 'AzBatchCertificate'에 추가할 인증서 종류를 선택하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="178c1-512">이전에 항상 ''였던 'ApplicationPackages' 속성이 'PSApplication'에서 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="178c1-513">이제 'Get-AzBatchApplicationPackage'를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="178c1-514">예를 들면 다음과 같습니다. 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="178c1-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="178c1-515">'New-AzBatchPool'을 사용하여 풀을 만들 때 'PSImageReference'의 'VirtualMachineImageId' 속성은 이제 Shared Image Gallery 이미지만 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="178c1-516">'New-AzBatchPool'을 사용하여 풀을 만들 때 공용 IP 없이 'PSNetworkConfiguration'의 새 'PublicIPAddressConfiguration'을 사용하여 풀을 프로비저닝할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="178c1-517">'PSNetworkConfiguration'의 'PublicIPs' 속성도 'PSPublicIPAddressConfiguration'으로 이동되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="178c1-518">이 속성은 'IPAddressProvisioningType'이 'UserManaged'인 경우에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-519">Az.Compute</span></span>
* <span data-ttu-id="178c1-520">'Update-AzVM' cmdlet에 HostId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="178c1-521">'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' 및 'Set-AzVmssOsProfile' cmdlet의 도움말 문서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="178c1-522">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="178c1-522">Breaking changes</span></span>
    - <span data-ttu-id="178c1-523">'Get-AzVMImage' cmdlet에서 FilterExpression 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="178c1-524">'New-AzVmssConfig', 'New-AzVMConfig' 및 'Update-AzVM' cmdlet에서 AssignIdentity 매개 변수가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="178c1-525">'New-AzVmssConfig' 및 'Update-AzVmss' cmdlet에서 AutomaticRepairMaxInstanceRepairsPercent가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="178c1-526">ProximityPlacementGroup에서 AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus 및 VirtualMachineScaleSetsColocationStatus 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="178c1-527">AutomaticRepairsPolicy에서 MaxInstanceRepairsPercent 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="178c1-528">AvailabilitySets, VirtualMachines 및 VirtualMachineScaleSets 형식이 IList<SubResource>에서 IList<SubResourceWithColocationStatus>로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="178c1-529">'Get-AzVM' cmdlet에 대한 설명이 보다 정확하게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-530">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-531">Managed IR에서 데이터 흐름 런타임 속성의 CRUD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-532">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-533">Front Door 규칙 엔진 개체를 생성, 업데이트, 검색 및 삭제할 수 있는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="178c1-534">Front Door 규칙 엔진 개체를 작성할 수 있는 도우미 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="178c1-535">Front Door 회람 규칙 개체에 대한 규칙 엔진 참조 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="178c1-536">Front Door 백 엔드 개체에 Private Link 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="178c1-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="178c1-537">Az.Functions</span></span>
* <span data-ttu-id="178c1-538">''Az.Functions'' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-539">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-540">고객 관리형 키 디스크 암호화 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="178c1-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="178c1-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="178c1-542">더 이상 액세스 정책이 기본적으로 현재 보안 주체로 설정되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-543">Az.IotHub</span></span>
* <span data-ttu-id="178c1-544">SQL과 비슷한 언어를 사용하여 정보를 검색하기 위해 IoT 허브에서 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="178c1-545">'Add-AzIotHubDevice'가 자식 디바이스 없는 에지 지원 디바이스를 만들 수 없는 문제 해결 [#11597]</span><span class="sxs-lookup"><span data-stu-id="178c1-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="178c1-546">IoT Hub, 디바이스 또는 모듈에 대한 SAS 토큰을 생성하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="178c1-547">구성 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="178c1-548">IoT Edge 자동 배포를 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="178c1-549">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-549">New cmdlets are:</span></span>
    - <span data-ttu-id="178c1-550">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="178c1-551">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="178c1-552">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="178c1-553">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="178c1-554">IoT Edge 배포 메트릭 쿼리를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="178c1-555">지정된 에지 디바이스에 구성 콘텐츠를 적용하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-556">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-557">다음 별칭 제거: 'New-AzKeyVaultCertificateAdministratorDetails' 및 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="178c1-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="178c1-558">키 자격 증명 모음을 만들 때 기본적으로 일시 삭제 사용</span><span class="sxs-lookup"><span data-stu-id="178c1-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="178c1-559">키 자격 증명 모음을 만들 때 특정 네트워크 위치의 액세스를 제어하도록 네트워크 규칙을 설정할 수 있음</span><span class="sxs-lookup"><span data-stu-id="178c1-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="178c1-560">BYOK(Bring Your Own Key) 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="178c1-561">'Add-AzKeyVaultKey'가 키 교환 키 생성 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="178c1-562">'Get-AzKeyVaultKey'가 PEM 형식의 공개 키 다운로드 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="178c1-563">'AzKeyVaultKey' 도움말 문서의 'KeyOps' 부분 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-564">Az.Monitor</span></span>
* <span data-ttu-id="178c1-565">'Set-AzDiagnosticSettings'의 버그 수정, 일부 범주에는 보존 정책이 적용되지 않음 [#11589]</span><span class="sxs-lookup"><span data-stu-id="178c1-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="178c1-566">메트릭 경고 V2에 WebTest를 사용하기 위한 조건 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="178c1-567">'New-AzMetricAlertRuleV2Criteria': webtest 사용 조건을 만드는 옵션 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="178c1-568">'Add-AzMetricAlertRuleV2': 새 webtest 사용 조건 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="178c1-569">PSLogProfile에서 RetentionPolicy에 대한 중복 정의 제거 [#7608]</span><span class="sxs-lookup"><span data-stu-id="178c1-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="178c1-570">PSEventData에 정의된 중복 속성 제거 [#11353]</span><span class="sxs-lookup"><span data-stu-id="178c1-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="178c1-571">'Get-AzLog'를 'Get-AzActivityLog'로 이름 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-572">Az.Network</span></span>
* <span data-ttu-id="178c1-573">영역 기본 동작이 변경된다는 것을 알리기 위해 주요 변경 특성을 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="178c1-574">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="178c1-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="178c1-575">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="178c1-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="178c1-576">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="178c1-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="178c1-577">새로운 최상위 리소스 SecurityPartnerProvider에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="178c1-578">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-578">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="178c1-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="178c1-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="178c1-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="178c1-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="178c1-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="178c1-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="178c1-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="178c1-583">'PSPrivateEndpointConnection'의 'PSPrivateLinkResource' 및 'GroupId'에서 'RequiredZoneNames' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="178c1-584">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject에 대한 잘못된 형식의 SuccessThresholdRoundTripTimeMs 매개 변수 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="178c1-585">AllowVnetToVnetTraffic 인수의 기본값을 True로 설정하도록 VirtualWan cmdlet 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="178c1-586">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="178c1-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="178c1-587">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="178c1-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="178c1-588">프라이빗 엔드포인트에 대한 DNS 영역 그룹을 지원하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="178c1-589">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="178c1-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="178c1-590">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="178c1-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="178c1-591">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="178c1-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="178c1-592">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="178c1-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="178c1-593">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="178c1-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="178c1-594">'AzureFirewall'에 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' 및 'DNSServers' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="178c1-595">'AzureFirewall'에 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' 및 'DnsServer' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="178c1-596">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="178c1-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="178c1-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-599">새로 생성된 SDK를 적용하도록 레거시 코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="178c1-600">사용되지 않는 API 때문에 cmdlet 삭제</span><span class="sxs-lookup"><span data-stu-id="178c1-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="178c1-601">'Get-AzOperationalInsightsSavedSearchResult'(별칭 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="178c1-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="178c1-602">'Get-AzOperationalInsightsSearchResult'(별칭 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="178c1-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="178c1-603">'Get-AzOperationalInsightsLinkTarget'(별칭 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="178c1-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="178c1-604">'Set-AzOperationalInsightsWorkspace' 및 'New-AzOperationalInsightsWorkspace'에 대한 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="178c1-605">연결된 스토리지 계정에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="178c1-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="178c1-606">클러스터 및 연결된 서비스에 대한 cmdlet 작성</span><span class="sxs-lookup"><span data-stu-id="178c1-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-608">Azure Site Recovery - Azure와 Azure 공급자 간 근접 배치 그룹 가상 머신을 보호하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="178c1-609">Azure Site Recovery - 영역 간 복제에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="178c1-610">Azure Backup - Azure 파일 공유 복구 지점의 장기 보존 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="178c1-611">Azure Backup - 'Get-AzRecoveryServicesBackupItem' cmdlet 출력에 디스크 제외 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="178c1-612">사이트 복구 서비스용 Vault 자격 증명 파일에 대한 프라이빗 엔드포인트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-613">Az.Resources</span></span>
* <span data-ttu-id="178c1-614">새 역할 정의를 만들 때 보기 지연에 대한 메시지 경고 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="178c1-615">강력한 형식의 개체를 출력하도록 정책 cmdlet 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="178c1-616">'Get-AzResourceLock' cmdlet에 사용되는 '-TenantLevel' 매개 변수 제거 [#11335]</span><span class="sxs-lookup"><span data-stu-id="178c1-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="178c1-617">'Remove-AzResourceGroup -Id ResourceId' 수정[#9882]</span><span class="sxs-lookup"><span data-stu-id="178c1-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="178c1-618">리소스 그룹 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="178c1-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="178c1-619">구독 범위에서 ARM 템플릿 가상 시나리오 결과를 가져오는 새 cmdlet 추가: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="178c1-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="178c1-620">별칭: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="178c1-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="178c1-621">ARM 템플릿 가상 시나리오 결과를 사용하도록 'New-AzDeployment' 및 'New-AzResourceGroupDeployment'에 대한 '-WhatIf' 및 '-Confirm' 매개 변수 재정의</span><span class="sxs-lookup"><span data-stu-id="178c1-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="178c1-622">배포 cmdlet에서 'ApiVersion' 매개 변수의 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="178c1-623">배포 오류에 대한 향상된 오류 메시지를 표시하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="178c1-624">배포 오류에 대한 correlationId 로깅 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="178c1-625">배포 스크립트 출력에 'error' 속성 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="178c1-626">nuget Microsoft.Azure.Management.ResourceManager를 '3.7.1-preview'로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="178c1-627">nuget 3.7.1-preview에서 DeploymentValidateResult의 Error 속성이 readonly로 변경되어 특정 테스트 사례를 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="178c1-628">SDK ResourceManager 3.7.1-preview의 GenericResourceExpanded 도입</span><span class="sxs-lookup"><span data-stu-id="178c1-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="178c1-629">모든 배포용 Get cmdlet에 대한 태그 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="178c1-630">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="178c1-631">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="178c1-632">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="178c1-633">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="178c1-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-635">잘못된 인증서 지문을 가져오는 --SecretIdentifier를 사용한 인증서 추가의 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-636">Az.Sql</span></span>
* <span data-ttu-id="178c1-637">성능 강화:</span><span class="sxs-lookup"><span data-stu-id="178c1-637">Enhance performance of:</span></span>
    - <span data-ttu-id="178c1-638">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="178c1-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="178c1-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="178c1-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="178c1-640">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="178c1-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="178c1-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="178c1-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="178c1-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="178c1-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="178c1-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="178c1-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="178c1-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="178c1-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="178c1-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="178c1-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="178c1-646">'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' cmdlet에서 'RetentionDays' 매개 변수의 클라이언트 쪽 유효성 검사 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="178c1-647">Vnet에서 스토리지 계정을 감사하고, Storage Blob 데이터 기여자 역할을 만들 때 발생하는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-648">Az.Storage</span></span>
* <span data-ttu-id="178c1-649">get/list account cmdlet 'Get-AzStorageAccount'에 '-AsJob' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="178c1-650">키 자동 회전을 지원하기 위해 스토리지 계정을 KeyvaultEncryption으로 업데이트할 때 KeyVersion을 선택 사항으로 지정</span><span class="sxs-lookup"><span data-stu-id="178c1-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="178c1-651">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="178c1-652">파이프라인을 사용하여 Azure 파일 디렉터리 제거 오류 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="178c1-653">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="178c1-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="178c1-654">수정 [#9880]: Swagger에 맞게 NetWorkRule DefaultAction 값 정의 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="178c1-655">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="178c1-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="178c1-656">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="178c1-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="178c1-657">수정 [#11624]: 서버 오류를 방지하기 위해 NetworkRules를 추가할 때 중복 규칙 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="178c1-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="178c1-658">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="178c1-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="178c1-659">Microsoft.Azure.Cosmos.Table SDK를 1.0.7로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="178c1-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="178c1-660">DataLake Gen2 항목 목록에 부품 항목만 반환되는 경우 ContinuationToken을 사용하여 다시 나열하라고 사용자에게 알리는 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="178c1-661">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="178c1-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="178c1-662">Azure Files Active Directory 도메인 서비스 인증을 사용하여 스토리지 계정을 만들거나 업데이트하는 기능 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="178c1-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="178c1-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="178c1-665">스토리지 계정의 Kerberos 키 새로 만들기 또는 나열 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="178c1-666">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="178c1-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="178c1-667">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="178c1-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="178c1-668">스토리지 계정 장애 조치(failover) 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="178c1-669">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="178c1-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="178c1-670">'Get-AzStorageBlobCopyState'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="178c1-671">'Get-AzStorageFileCopyState' 및 'Start-AzStorageBlobCopy'의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="178c1-672">스토리지 클라이언트 라이브러리 v12를 큐 및 파일 cmdlet에 통합</span><span class="sxs-lookup"><span data-stu-id="178c1-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="178c1-673">출력 형식을 CloudFile에서 AzureStorageFile로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="178c1-674">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="178c1-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="178c1-675">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="178c1-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="178c1-676">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="178c1-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="178c1-677">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="178c1-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="178c1-678">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="178c1-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="178c1-679">출력 형식을 CloudFileDirectory에서 AzureStorageFileDirectory로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="178c1-680">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="178c1-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="178c1-681">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="178c1-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="178c1-682">출력 형식을 CloudFileShare에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="178c1-683">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="178c1-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="178c1-684">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="178c1-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="178c1-685">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="178c1-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="178c1-686">출력 형식을 FileShareProperties에서 AzureStorageFileShare로 변경했으며, 원래 출력은 새 출력의 하위 자식 속성이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="178c1-687">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="178c1-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="178c1-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="178c1-688">Az.TrafficManager</span></span>
* <span data-ttu-id="178c1-689">'DisableAzureTrafficManagerEndpoint' 자세한 정보 출력에서 잘못된 프로필 이름 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-690">Az.Websites</span></span>
* <span data-ttu-id="178c1-691">'Update-AzWebAppAccessRestrictionConfig'의 도움말에서 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="178c1-692">3.8.0 - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="178c1-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="178c1-693">마지막 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-693">Highlights since the last release</span></span>
* <span data-ttu-id="178c1-694">Az.Storage에서 지원하는 PowerShell 버전: Windows PowerShell 5.1, PowerShell Core 6.2.4 이상, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="178c1-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-695">Az.Accounts</span></span>
* <span data-ttu-id="178c1-696">'Resolve-AzError'에서 Azure PowerShell 설문 조사 URL이 업데이트되었습니다. [#11507]</span><span class="sxs-lookup"><span data-stu-id="178c1-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-697">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-698">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="178c1-699">'Set-AzApiManagementGroup' - GroupId 매개 변수를 지정하도록 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-700">Az.Cdn</span></span>
* <span data-ttu-id="178c1-701">ChinaCDN 관련 가격 책정 SKU 표시가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-703">Identity, Encryption, UserOwnedStorage가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-704">Az.Compute</span></span>
* <span data-ttu-id="178c1-705">'Set-AzVmssOrchestrationServiceState' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="178c1-706">-InstanceView가 있는 'Get-AzVmss'는 OrchestrationService 상태를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-707">Az.IotHub</span></span>
* <span data-ttu-id="178c1-708">IoT 디바이스 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="178c1-709">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="178c1-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="178c1-710">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="178c1-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="178c1-711">IoT Hub에서 디바이스에 대한 직접 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="178c1-712">IoT 디바이스 모듈 쌍 구성을 관리합니다. 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="178c1-713">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="178c1-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="178c1-714">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="178c1-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="178c1-715">IoT 자동 디바이스 관리 구성을 대규모로 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="178c1-716">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-716">New cmdlets are:</span></span>
    - <span data-ttu-id="178c1-717">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="178c1-718">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="178c1-719">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="178c1-720">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="178c1-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="178c1-721">Iot Hub에서 에지 모듈 메서드를 호출하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-722">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-723">자격 증명 모음에서 일시 삭제 및 제거 보호를 사용하도록 설정할 수 있는 새 cmdlet 'Update-AzKeyVault'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="178c1-724">Microsoft.PowerShell.SecretManagement에 대한 지원이 추가되었습니다. [#11178]</span><span class="sxs-lookup"><span data-stu-id="178c1-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="178c1-725">'Remove-AzKeyVaultManagedStorageSasDefinition' 예제의 오류가 해결되었습니다. [#11479]</span><span class="sxs-lookup"><span data-stu-id="178c1-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="178c1-726">프라이빗 엔드포인트에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="178c1-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="178c1-727">Az.Maintenance</span></span>
* <span data-ttu-id="178c1-728">GA용 유지 관리 cmdlet의 릴리스 버전 게시</span><span class="sxs-lookup"><span data-stu-id="178c1-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-729">Az.Monitor</span></span>
* <span data-ttu-id="178c1-730">프라이빗 링크 범위용 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="178c1-731">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="178c1-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="178c1-732">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="178c1-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="178c1-733">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="178c1-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="178c1-734">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="178c1-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="178c1-735">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="178c1-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="178c1-736">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="178c1-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="178c1-737">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="178c1-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-738">Az.Network</span></span>
* <span data-ttu-id="178c1-739">Virtual Network 게이트웨이의 개인 IP에 대한 연결을 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="178c1-740">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="178c1-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="178c1-741">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="178c1-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="178c1-742">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="178c1-743">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="178c1-744">FQDN 기반 LocalNetworkGateways 및 VpnSites를 사용하도록 설정하는 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="178c1-745">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="178c1-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="178c1-746">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="178c1-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="178c1-747">ExpressRouteCircuitConnectionConfig(Global Reach)의 IPv6 주소 패밀리에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="178c1-748">'Set-AzExpressRouteCircuitConnectionConfig'가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="178c1-749">IPv6CircuitConnectionProperties를 포함한 모든 기존 속성을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="178c1-750">'Add-AzExpressRouteCircuitConnectionConfig'가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="178c1-751">주소 접두사의 주소 패밀리를 지정하는 또 다른 선택적 매개 변수 AddressPrefixType이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="178c1-752">Virtual Network 게이트웨이 연결에서 DPD 시간 제한 설정을 사용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="178c1-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="178c1-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-756">정책 준수 검사를 트리거하기 위한 'Start-AzPolicyComplianceScan' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="178c1-757">'Get-AzPolicyState' 출력에 정책 정의, 집합 정의 및 할당 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-759">'New-AzServiceFabricCluster' 예제의 코드 서식 및 사용 편의성이 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-760">Az.Sql</span></span>
* <span data-ttu-id="178c1-761">'Get-AzSqlInstanceOperation' 및 'Stop-AzSqlInstanceOperation' cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="178c1-762">VNet에서 스토리지 계정에 대한 감사가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-763">Az.Storage</span></span>
* <span data-ttu-id="178c1-764">향후 릴리스의 Azure File cmdlet 출력 변경에 대한 호환성이 손상되는 변경 공지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="178c1-765">스토리지 계정 생성/업데이트 시 새로운 SkuName StandardGZRS, StandardRAGZRS가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="178c1-766">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="178c1-767">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="178c1-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="178c1-768">DataLake Gen2가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="178c1-769">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="178c1-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="178c1-770">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="178c1-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="178c1-771">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="178c1-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="178c1-772">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="178c1-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="178c1-773">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="178c1-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="178c1-774">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="178c1-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="178c1-775">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="178c1-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="178c1-776">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="178c1-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="178c1-777">0.10.0-preview - 2020년 4월</span><span class="sxs-lookup"><span data-stu-id="178c1-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="178c1-778">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-778">General</span></span>
* <span data-ttu-id="178c1-779">이제 Az 모듈이 Azure Stack Hub에서 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="178c1-780">따라서 Linux 및 macOS와의 플랫폼 간 호환성이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="178c1-781">Azure Stack Hub는 이제 Az 모듈을 사용하여 PowerShell Core를 지원합니다. 자세한 내용은 [여기](https://aka.ms/az4AzureStack)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="178c1-782">Az 모듈은 2019-03-01-hybrid 프로필을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="178c1-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="178c1-783">Az.Billing</span></span>
  - <span data-ttu-id="178c1-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-784">Az.Compute</span></span>
  - <span data-ttu-id="178c1-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="178c1-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="178c1-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-786">Az.EventHub</span></span>
  - <span data-ttu-id="178c1-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-787">Az.IotHub</span></span>
  - <span data-ttu-id="178c1-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-788">Az.KeyVault</span></span>
  - <span data-ttu-id="178c1-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-789">Az.Monitor</span></span>
  - <span data-ttu-id="178c1-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-790">Az.Network</span></span>
  - <span data-ttu-id="178c1-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-791">Az.Resources</span></span>
  - <span data-ttu-id="178c1-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-792">Az.Storage</span></span>
  - <span data-ttu-id="178c1-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-793">Az.Websites</span></span>
* <span data-ttu-id="178c1-794">Azure Stack Hub와 함께 작동하는 az용 새 PowerShell 모듈 3개(Az.Databox, Az.IotHub 및 Az.EventHub)가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="178c1-795">AzureRM을 Az로 변경하는 것과 같은 사소한 변경을 수행하면 명령이 비교적 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="178c1-796">Azure Stack Hub에 대한 PowerShell 설명서의 업데이트된 링크는 [여기](https://aka.ms/InstallASHPowerShell)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="178c1-797">3.7.0 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="178c1-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-798">Az.Accounts</span></span>
* <span data-ttu-id="178c1-799">로그인하지 않을 때 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault'에서 NullReferenceException이 발생하는 문제가 해결되었습니다. [# 10292]</span><span class="sxs-lookup"><span data-stu-id="178c1-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-800">Az.Compute</span></span>
* <span data-ttu-id="178c1-801">'New-AzDiskConfig' cmdlet에 다음 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="178c1-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="178c1-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="178c1-803">암호화 속성이 'New-AzGalleryImageVersion'cmdlet의 대상 매개 변수에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="178c1-804">'Set-AzVmss'-Reimage 및 'Invoke-AzVMReimage'cmdlet에 대한 tempDisk 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="178c1-805">[#11354]</span><span class="sxs-lookup"><span data-stu-id="178c1-805">[#11354]</span></span>
* <span data-ttu-id="178c1-806">새로운 SAP 확장을 위해 아래 cmdlet에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="178c1-807">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="178c1-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="178c1-808">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="178c1-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="178c1-809">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="178c1-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="178c1-810">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="178c1-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="178c1-811">도움말 문서의 예제에서 오류가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="178c1-812">VM PowerState의 정확한 문자열 값을 테이블 형식으로 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="178c1-813">'New-AzVmssConfig': SinglePlacementGroup이 비활성화된 경우 AutomaticRepairs 속성의 직렬화가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="178c1-814">[#11257]</span><span class="sxs-lookup"><span data-stu-id="178c1-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-815">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-816">ADF .Net SDK 버전이 4.8.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="178c1-817">재실행을 지원하기 위해 'Invoke-AzDataFactoryV2Pipeline' 명령에 선택적 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-819">'Export-AzDataLakeStoreItem' 및 'Import-AzDataLakeStoreItem'에 대해 호환성이 손상되는 변경 설명을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="178c1-820">'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' 및 'Get-AzDAtaLakeStoreItemContent'에 대한 바이트 인코딩 옵션이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-821">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-822">클러스터 생성 시 최소 지원 TLS 버전 지정이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-823">Az.IotHub</span></span>
* <span data-ttu-id="178c1-824">디바이스별 분산 설정을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="178c1-825">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="178c1-826">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="178c1-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="178c1-827">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="178c1-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-828">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-829">'New-AzKeyVault'에 대해 호환성이 손상되는 변경 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-830">Az.Monitor</span></span>
* <span data-ttu-id="178c1-831">'New-AzScheduledQueryRuleLogMetricTrigger'에 대한 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-832">Az.Network</span></span>
* <span data-ttu-id="178c1-833">교차 테넌트 VirtualHubVnetConnections를 허용하도록 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="178c1-834">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="178c1-835">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="178c1-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="178c1-836">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="178c1-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="178c1-837">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="178c1-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="178c1-838">SQL Management SDK 종속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-840">오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-842">Azure Site Recovery는 Azure 디스크 암호화 Virtual Machines에 대한 VM 속성을 다시 보호하고 업데이트하는 기능을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="178c1-843">Azure Site Recovery VmwareToAzure 속성 DR 모니터링이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="178c1-844">Azure Backup은 실패한 항목에 대한 정책 업데이트 재시도 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="178c1-845">Azure Backup은 백업 및 복원 중에 디스크 제외 설정에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="178c1-846">Azure Backup은 AzureFileShare에서 여러 파일/폴더 복원을 위한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="178c1-847">Azure Backup은 IaasVM 정책을 업데이트하는 동안 사용자 지정 리소스 그룹 지원에 대한 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-848">Az.Resources</span></span>
* <span data-ttu-id="178c1-849">'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType'이 기본 apiVersion 대신 실제 apiVersion 리소스를 사용하도록 수정했습니다. [# 11267]</span><span class="sxs-lookup"><span data-stu-id="178c1-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="178c1-850">오류 시나리오에 대해 correlationId 로깅이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="178c1-851">작은 설명서가 'Get-AzResourceLock'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="178c1-852">예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-852">Added example.</span></span>
* <span data-ttu-id="178c1-853">'Get-AzADUser'의 매개 변수 값에서 작은 따옴표를 이스케이프 처리하였습니다. [# 11317]</span><span class="sxs-lookup"><span data-stu-id="178c1-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="178c1-854">배포 스크립트('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')에 대한 새로운 cmdlet 추가가 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-855">Az.Sql</span></span>
* <span data-ttu-id="178c1-856">'Invoke-AzSqlDatabaseFailover'에 읽기 가능한 보조 매개 변수를 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="178c1-857">'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' cmdlet을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="178c1-858">데이터베이스에서 열을 분류할 때 저장된 민감도 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="178c1-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="178c1-859">Az.Support</span></span>
* <span data-ttu-id="178c1-860">'Az.Support' 모듈의 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-861">Az.Websites</span></span>
* <span data-ttu-id="178c1-862">아래의 새로운 cmdlet을 통해 webapp 트래픽 라우팅 규칙을 사용하는 작업에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="178c1-863">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="178c1-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="178c1-864">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="178c1-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="178c1-865">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="178c1-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="178c1-866">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="178c1-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="178c1-867">3.6.1 - 2020년 3월</span><span class="sxs-lookup"><span data-stu-id="178c1-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-868">Az.Accounts</span></span>
* <span data-ttu-id="178c1-869">'피드백 보내기'에서 Azure PowerShell 설문 조사 페이지가 열립니다[#11020].</span><span class="sxs-lookup"><span data-stu-id="178c1-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="178c1-870">'오류 해결'에서 Azure PowerShell 설문 조사 URL이 표시됩니다[#11021].</span><span class="sxs-lookup"><span data-stu-id="178c1-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="178c1-871">UserAgent에서 Az 버전이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-872">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-873">DeveloperPortal 엔드포인트에서 사용자 지정 도메인을 검색하고 구성하기 위한 지원이 추가되었습니다[#11007].</span><span class="sxs-lookup"><span data-stu-id="178c1-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="178c1-874">Json 형식의 API 정의를 다운로드하기 위한 'Export-AzApiManagementApi' 지원이 추가되었습니다[#9987].</span><span class="sxs-lookup"><span data-stu-id="178c1-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="178c1-875">Json 문서에서 OpenApi 3.0 정의를 가져오기 위한 'Import-AzApiManagementApi' 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="178c1-876">AAD B2C 공급자에 대한 '로그인 테넌트'를 구성하기 위한 'New-AzApiManagementIdentityProvider' 및 'Set-AzApiManagementIdentityProvider' 지원이 추가되었습니다[#9784].</span><span class="sxs-lookup"><span data-stu-id="178c1-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-878">csproj 및 psd1에서 System.Buffers에 대한 참조가 명시적으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-879">Az.IotHub</span></span>
* <span data-ttu-id="178c1-880">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="178c1-881">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="178c1-882">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="178c1-883">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="178c1-884">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="178c1-885">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="178c1-886">Iot Hub의 대상 IoT 디바이스에서 모듈을 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="178c1-887">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="178c1-888">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="178c1-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="178c1-889">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="178c1-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="178c1-890">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="178c1-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="178c1-891">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="178c1-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="178c1-892">Iot Hub에서 대상 IoT 디바이스에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="178c1-893">Iot Hub에서 대상 IoT 디바이스의 모듈에 대한 연결 문자열을 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="178c1-894">IoT 디바이스의 부모 디바이스를 가져오거나 설정하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="178c1-895">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="178c1-896">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="178c1-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="178c1-897">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="178c1-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="178c1-898">디바이스 부모-자식 관계를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-899">Az.Monitor</span></span>
* <span data-ttu-id="178c1-900">'Get-AzMetricDefinition'에 대한 출력 값이 수정되었습니다[#9714].</span><span class="sxs-lookup"><span data-stu-id="178c1-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-901">Az.Network</span></span>
* <span data-ttu-id="178c1-902">SQL Management SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="178c1-903">PrivateLinkServiceConnectionState 클래스의 명명 차이 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="178c1-904">ActionsRequired 필드가 ActionRequired에 매핑됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="178c1-905">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-906">Az.Resources</span></span>
* <span data-ttu-id="178c1-907">Get-AzRoleAssignment'의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="178c1-908">'Remove-AzADGroup'에서 '-Force' 및 '-PassThru' 스위치가 선택적으로 표시됩니다[#10849].</span><span class="sxs-lookup"><span data-stu-id="178c1-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="178c1-909">'Remove-AzADGroup'에서 'MailNickname'이 반환되지 않는 문제가 해결되었습니다[#11167].</span><span class="sxs-lookup"><span data-stu-id="178c1-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="178c1-910">'Remove-AzADGroup' 파이프 작업이 작동하지 않는 문제가 해결되었습니다[#11171].</span><span class="sxs-lookup"><span data-stu-id="178c1-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="178c1-911">GetAzureRoleAssignmentCommand의 null 참조 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="178c1-912">예정된 정책 cmdlet 변경에 대한 호환성이 손상되는 변경 특성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="178c1-913">서버 쪽에서 리소스 그룹 태그 필터링을 수행하도록 'Get-AzResourceGroup'이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="178c1-914">-ResourceId를 허용하도록 Tag cmdlet이 확장되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="178c1-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="178c1-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="178c1-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="178c1-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="178c1-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="178c1-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="178c1-918">새 Tag cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="178c1-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="178c1-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="178c1-920">SDK 3.3.0에서 ScopedDeployment를 가져왔습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-921">Az.Sql</span></span>
* <span data-ttu-id="178c1-922">PublicNetworkAccess가 'New-AzSqlServer' 및 'Set-AzSqlServer'에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="178c1-923">관리형 데이터베이스에 대한 장기 보존 백업 구성에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="178c1-924">관리형 데이터베이스에서 LTR 정책을 가져오거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="178c1-925">관리형 데이터베이스, 관리형 인스턴스 또는 위치를 기준으로 LTR 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="178c1-926">LTR 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="178c1-927">LTR 백업을 복원하여 새 관리형 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="178c1-928">MinimalTlsVersion이 New-AzSqlServer 및 Set-AzSqlServer에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="178c1-929">MinimalTlsVersion을 New-AzSqlInstance 및 Set-AzSqlInstance에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="178c1-930">Az.Network에 대한 SQL SDK 버전이 높아졌습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-931">Az.Storage</span></span>
* <span data-ttu-id="178c1-932">ImmutabilityPolicy에서 AllowProtectedAppendWrite가 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="178c1-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="178c1-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="178c1-934">이후 릴리스에서 AzureStorageTable 형식 변경에 대한 호환성이 손상되는 변경 경고 메시지가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="178c1-935">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="178c1-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="178c1-936">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="178c1-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-937">Az.Websites</span></span>
* <span data-ttu-id="178c1-938">'New-AzAppServicePlan' 및 'Set-AzAppServicePlan'에 대한 Tag 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="178c1-939">웹 사이트에 사용자 지정 도메인을 추가할 때 예외가 throw되면 cmdlet 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="178c1-940">App Service 계획과 동일한 리소스 그룹에 속하지 않는 App Services에 대한 작업을 수행하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="178c1-941">다른 리소스 그룹의 WebApp/Function에 대한 액세스 제한이 적용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="178c1-942">WebAppSlot에 대한 사용자 지정 호스트 이름을 설정하는 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="178c1-943">3.5.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="178c1-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="178c1-944">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-944">Highlights since the last major release</span></span>
* <span data-ttu-id="178c1-945">클라이언트 쪽 원격 분석이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="178c1-946">디바이스 관리를 지원하는 cmdlet이 Az.IotHub에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="178c1-947">가용성 그룹 수신기에 대한 cmdlet이 Az.SqlVirtualMachine에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-948">Az.Accounts</span></span>
* <span data-ttu-id="178c1-949">SubscriptionId, TenantId 및 실행 시간이 클라이언트 쪽 원격 분석에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-950">Az.Automation</span></span>
* <span data-ttu-id="178c1-951">'New-AzAutomationSoftwareUpdateConfiguration' 참조 설명서의 예제 1에 있는 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-953">SDK가 7.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="178c1-954">서버 응답 본문이 비어 있는 경우 표시되는 오류 메시지가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-955">Az.Compute</span></span>
* <span data-ttu-id="178c1-956">업데이트하는 동안 빈 값이 ProximityPlacementGroupId에 허용되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-957">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-958">WAF에서 사용할 수 있는 관리형 규칙 정의를 가져오는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-959">Az.IotHub</span></span>
* <span data-ttu-id="178c1-960">Iot Hub에서 디바이스를 관리하기 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="178c1-961">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="178c1-962">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="178c1-963">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="178c1-964">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="178c1-965">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="178c1-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-966">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-967">Add-AzKeyVaultKey.md에 대해 중복된 텍스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-968">Az.Monitor</span></span>
* <span data-ttu-id="178c1-969">Get-AzLog cmdlet에 대한 설명이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="178c1-970">ActionGroupId라는 새 매개 변수가 'New-AzMetricAlertRuleV2' 명령에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="178c1-971">사용자는 ActionGroupId(string) 또는 ActionGorup(ActivityLogAlertActionGroup) 중 하나를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-972">Az.Network</span></span>
* <span data-ttu-id="178c1-973">'New-AzPrivateLinkService' cmdlet의 '-EnableProxyProtocol' 매개 변수에 대한 하나의 추가 매개 변수 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="178c1-974">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 FilterData 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="178c1-975">Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 및 Start-AzVirtualnetworkGatewayPacketCapture.md의 모든 내부 및 외부 패킷을 캡처하는 패킷 캡처 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="178c1-976">VNet 방화벽에서 Azure Firewall 정책이 지원됩니다</span><span class="sxs-lookup"><span data-stu-id="178c1-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="178c1-977">새로 추가된 cmdlet이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-977">No new cmdlets are added.</span></span> <span data-ttu-id="178c1-978">VNet 방화벽에서 방화벽 정책 제한이 완화되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-980">SQL Database에 대한 파일로 복원 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-981">Az.Resources</span></span>
* <span data-ttu-id="178c1-982">템플릿 배포 cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="178c1-983">관리 그룹에서 배포를 관리하는 새 \*-AzManagementGroupDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="178c1-984">테넌트 범위에서 배포를 관리하는 새 \*-AzTenantDeployment cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="178c1-985">구독 범위에서 구체적으로 작동하도록 \*-AzDeployment cmdlet이 리팩터링되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="178c1-986">\*-AzDeployment cmdlet에 대한 \*-AzSubscriptionDeployment 별칭이 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="178c1-987">'AvailableToOtherTenants' 매개 변수가 설정되지 않는 'Update-AzADApplication'이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="178c1-988">AmbiguousParameterSetException을 방지하기 위해 ApplicationObjectWithoutCredentialParameterSet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="178c1-989">도움말 파일이 다시 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-990">Az.Sql</span></span>
* <span data-ttu-id="178c1-991">Managed Instance에서 구독 간 특정 시점 복원에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="178c1-992">기존 SQL Managed Instance 하드웨어 생성 변경에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="178c1-993">'Update-AzSqlServerVulnerabilityAssessmentSetting' 도움말 예제(매개 변수/속성 출력 -EmailAdmins)가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="178c1-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="178c1-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="178c1-995">가용성 그룹 수신기에 대한 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="178c1-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="178c1-996">Az.StorageSync</span></span>
* <span data-ttu-id="178c1-997">'Invoke-AzStorageSyncCompatibilityCheck'에서 지원되는 문자 세트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="178c1-998">3.4.0 - 2020년 2월</span><span class="sxs-lookup"><span data-stu-id="178c1-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="178c1-999">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-999">Highlights since the last major release</span></span>
* <span data-ttu-id="178c1-1000">Az. CosmosDB 초기 버전 0.1.0 출시</span><span class="sxs-lookup"><span data-stu-id="178c1-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="178c1-1001">Az.Network ConnectionMonitor V2 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1002">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1003">AzureRmContext.json을 사용할 수 없을 때 컨텍스트 자동 저장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="178c1-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="178c1-1004">Azure Powershell Common 참조를 1.3.5-preview로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-1006">**Get-AzApiManagementApiSchema** API와 연결된 Open-Api 스키마 가져오기 수정   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="178c1-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="178c1-1007">**New-AzApiManagementProduct**\* 및 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="178c1-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="178c1-1008">https://github.com/Azure/azure-powershell/issues/10472 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="178c1-1009">**Set-AzApiManagementApi** cmdlet을 사용하여 ServiceUrl을 업데이트하는 방법을 보여주는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1010">Az.Compute</span></span>
* <span data-ttu-id="178c1-1011">VM 이름을 사용하지 않고 Get-AzVM -Status를 수행할 때 제한을 피하기 위해 VM 상태 수를 100개로 제한</span><span class="sxs-lookup"><span data-stu-id="178c1-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="178c1-1012">Update-AzDiskEncryptionSet cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="178c1-1013">다음 cmdlet에 EncryptionType 및 DiskEncryptionSetId 매개 변수 추가:</span><span class="sxs-lookup"><span data-stu-id="178c1-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="178c1-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="178c1-1015">Get-AzProximityPlacementGroup cmdlet에 ColocationStatus 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1016">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1017">ADF .Net SDK 버전을 4.7.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="178c1-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="178c1-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="178c1-1019">리소스에 대한 LIST 작업 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="178c1-1020">상태 검사 단계에 대한 작업을 수행하는 기능 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-1021">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-1022">AzHDInsightCluster의 문서 오류 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-1023">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-1024">Remove-AzureKeyVault가 새 New-AzureKeyVault와 일관성을 유지하도록 VaultName 특성에 이름 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1025">Az.Network</span></span>
* <span data-ttu-id="178c1-1026">Set-AzNetworkWatcherConfigFlowLog.md에 트래픽 분석 사용 안 함 시나리오를 보여주는 새 예제 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="178c1-1027">Azure Firewall에 관리 IP 구성을 할당하는 지원 추가 - 방화벽에서 관리 트래픽에 사용할 전용 서브넷 및 공용 IP</span><span class="sxs-lookup"><span data-stu-id="178c1-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="178c1-1028">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="178c1-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="178c1-1029">공용 IP 주소 개체를 허용하는 -ManagementPublicIpAddress 매개 변수(필수 아님) 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="178c1-1030">방화벽 개체에 SetManagementIpConfiguration 메서드 추가 - 입력으로 서브넷 및 공용 IP 주소 필요 - 서브넷 이름은 'AzureFirewallManagementSubnet'이어야 함</span><span class="sxs-lookup"><span data-stu-id="178c1-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="178c1-1031">네트워크 인터페이스 대신 NSG 예제를 보여주도록 AzNetworkSecurityGroup 예제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="178c1-1032">리소스 id 완성자가 매개 변수를 완성하지 못하게 방해하던 New-AzVpnSite 명령의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="178c1-1033">Application Gateway의 다시 쓰기 규칙 작업 세트에서 Url 구성에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="178c1-1034">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="178c1-1036">선택적 매개 변수를 사용하도록 Cmdlet 업데이트 - UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="178c1-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="178c1-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="178c1-1038">NetworkWatcher ConnectionMonitor 버전 2 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-1040">수정할 리소스를 결정하기 전에 규정 준수 평가 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="178c1-1041">Start-AzPolicyRemediation에 '-ResourceDiscoverMode' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="178c1-1042">정책 메타데이터 리소스를 가져오는 Get-AzPolicyMetadata cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="178c1-1043">API 버전 2019-10-01의 Get-AzPolicyState 및 Get-AzPolicyStateSummary 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1045">복제된 디스크를 제거할 수 있도록 Azure Site Recovery에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="178c1-1046">Recovery Services 자격 증명 모음을 만드는 동안 태그를 추가할 수 있도록 Azure Backup에 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1047">Az.Resources</span></span>
* <span data-ttu-id="178c1-1048">컨텍스트 구독을 기본값으로 하는 \*-AzPolicyAssignment cmdlet에서 -Scope를 선택 사항으로 설정</span><span class="sxs-lookup"><span data-stu-id="178c1-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="178c1-1049">암호 및 키 자격 증명을 사용하여 ADServicePrincipal을 만드는 예제 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1050">Az.Sql</span></span>
<span data-ttu-id="178c1-1051">DatabaseName 대신 PartnerDatabaseName이 있는지 확인하도록 New-AzSqlDatabaseSecondary cmdlet 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1052">Az.Storage</span></span>
* <span data-ttu-id="178c1-1053">스토리지 계정 만들기에서 테이블/큐 암호화 Keytype 설정 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="178c1-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="178c1-1055">StorageException에 ExtendedErrorInformation이 없으면 RequestId 표시</span><span class="sxs-lookup"><span data-stu-id="178c1-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="178c1-1056">cmdlet Start-AzStorageBlobCopy의 예제 6 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-1057">Az.Websites</span></span>
* <span data-ttu-id="178c1-1058">Set-AzWebapp 및 Set-AzWebappSlot이 AlwaysOn, MinTls 및 FtpsState 속성 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="178c1-1059">단일 Set-AzWebApp 명령을 사용하여 AppservicePlan을 변경하는 동시에 HttpsOnly를 설정하면 HttpsOnly가 기본값으로 다시 설정되는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="178c1-1060">3.3.0 - 2020년 1월</span><span class="sxs-lookup"><span data-stu-id="178c1-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1061">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1062">AzureAttestationServiceEndpointResourceId 및 AzureAttestationServiceEndpointSuffix 매개 변수를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-1063">Az.Cdn</span></span>
* <span data-ttu-id="178c1-1064">New-AzCdnEndpoint cmdlet에서 오류 응답 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="178c1-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1065">Az.Compute</span></span>
* <span data-ttu-id="178c1-1066">OS 프로필이 없는 관리 OD 디스크가 있는 VM의 Set-AzVMCustomScriptExtension cmdlet을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="178c1-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="178c1-1068">New-AzContainerGroup의 예에서 사용되는 고정 매개 변수 이름</span><span class="sxs-lookup"><span data-stu-id="178c1-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="178c1-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="178c1-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="178c1-1070">'Get-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="178c1-1071">Edge 스토리지 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="178c1-1072">'New-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="178c1-1073">새 Edge 스토리지 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="178c1-1074">'Remove-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="178c1-1075">Edge 스토리지 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="178c1-1076">'Invoke-AzDataBoxEdgeStorageContainer' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="178c1-1077">Edge 스토리지 컨테이너에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="178c1-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="178c1-1078">'Get-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="178c1-1079">Edge 스토리지 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="178c1-1080">'New-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="178c1-1081">새 Edge 스토리지 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="178c1-1082">'Remove-AzDataBoxEdgeStorageAccount' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="178c1-1083">Edge 스토리지 계정 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="178c1-1084">'Invoke-AzDataBoxEdgeShare' cmdlet 호출</span><span class="sxs-lookup"><span data-stu-id="178c1-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="178c1-1085">공유에서 데이터를 새로 고치는 작업 호출</span><span class="sxs-lookup"><span data-stu-id="178c1-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="178c1-1086">'Set-AzDataBoxEdgeStorageAccountCredential' cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="178c1-1087">az databoxedge 스토리지 계정 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="178c1-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1088">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1089">Get-AzDataFactoryV2IntegrationRuntime cmd에 AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId 및 VersionStatus 속성 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="178c1-1090">ADF .Net SDK 버전을 4.6.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="178c1-1091">고정 공용 IP 주소로 Azure-SSIS IR을 만들 수 있도록 'Set-AzureRmDataFactoryV2IntegrationRuntime'cmd에 대해 'PublicIPs' 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="178c1-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="178c1-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="178c1-1093">Get-AzDtlAllowedVMSizesPolicy.md에서 끊어진 링크 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1094">Az.EventHub</span></span>
* <span data-ttu-id="178c1-1095">10634 문제 해결: eventhubnamespace 제거에 대한 null 개체 참조 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-1096">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-1097">Invoke-AzHDInsightHiveJob.md 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="178c1-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="178c1-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="178c1-1099">MachineLearningCompute를 더 이상 사용할 수 없게 되어 아래 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="178c1-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="178c1-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="178c1-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="178c1-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="178c1-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="178c1-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="178c1-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="178c1-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="178c1-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="178c1-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="178c1-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="178c1-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="178c1-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="178c1-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1107">Az.Network</span></span>
* <span data-ttu-id="178c1-1108">Microsoft.Azure.Management.Sql의 종속성을 1.36-preview에서 1.37-preview로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="178c1-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1110">Azure Site Recovery는 Azure 간 공급자를 위해 고객 관리 키와 함께 유휴 상태에서 암호화된 관리 디스크 vms의 변경을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="178c1-1111">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용할 때 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="178c1-1112">Azure Site Recovery는 VMware에서 Azure로를 위해 보호를 사용하기 위해 디스크 수준의 선택적 입력으로서 디스크 암호화 집합 ID를 입력하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="178c1-1113">Azure Site Recovery는 HyperV에서 Azure로를 위해 디스크 암호화 집합 맵을 사용하여 복제 보호된 항목을 업데이트하도록 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1114">Az.Resources</span></span>
* <span data-ttu-id="178c1-1115">'Remove-AzTag'의 도움말 문서에서 오류를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1116">Az.Sql</span></span>
* <span data-ttu-id="178c1-1117">Azure Database의 마스터 DB에서 작동하도록 취약성 평가 세트 기준 cmdlet 기능을 수정하고 관리형 인스턴스 시스템 데이터베이스에서 이를 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="178c1-1118">SQL 인스턴스 장애 조치(failover) 그룹을 만들 때 오류 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="178c1-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="178c1-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="178c1-1120">올바른 새 라이선스 형식으로 DR 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1121">Az.Storage</span></span>
* <span data-ttu-id="178c1-1122">다음 릴리스에서 DefaultAction Value 변경에 대해 호환성이 손상되는 변경 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="178c1-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="178c1-1124">-IncludeGeoReplicationStats 매개 변수와 함께 get-AzureRMStorageAccount를 실행하여 스토리지 계정의 마지막 동기화 시간 가져오기 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="178c1-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="178c1-1126">3.2.0 - 2019년 12월</span><span class="sxs-lookup"><span data-stu-id="178c1-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="178c1-1127">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-1127">General</span></span>
* <span data-ttu-id="178c1-1128">모든 모듈의 상대 경로를 사용하기 위해 .psd1의 참조 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1129">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1130">Az 4.0 미리 보기를 위해 클라이언트 측 원격 분석에 대해 UserAgent를 올바르게 설정</span><span class="sxs-lookup"><span data-stu-id="178c1-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="178c1-1131">Az 4.0 미리 보기에서 컨텍스트가 null인 경우 사용자에게 친숙한 오류 메시지로 표시</span><span class="sxs-lookup"><span data-stu-id="178c1-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-1132">Az.Batch</span></span>
* <span data-ttu-id="178c1-1133">**New-AzBatchPool**이 'VirtualMachineConfiguration.ContainerConfiguration' 또는 'VirtualMachineConfiguration.DataDisks'를 서버로 제대로 보내지 않는 [#10602](https://github.com/Azure/azure-powershell/issues/10602) 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1134">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1135">ADF .Net SDK 버전을 4.5.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-1137">WAF 관리 규칙 제외 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="178c1-1138">자동 완성에 SocketAddr 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="178c1-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="178c1-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="178c1-1140">예외 처리</span><span class="sxs-lookup"><span data-stu-id="178c1-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-1141">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-1142">잠재적으로 설정되지 않은 오류 액세스 값 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="178c1-1143">타원 곡선 암호화 인증서 관리</span><span class="sxs-lookup"><span data-stu-id="178c1-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="178c1-1144">인증서 정책에 대한 곡선 지정을 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-1145">Az.Monitor</span></span>
* <span data-ttu-id="178c1-1146">진단 설정 추가 명령에 선택적 인수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="178c1-1147">스위치 인수(있는 경우)는 Log Analytics로 내보내기가 고정 스키마(전용 데이터 유형)가 되어야 함을</span><span class="sxs-lookup"><span data-stu-id="178c1-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="178c1-1148">나타냄</span><span class="sxs-lookup"><span data-stu-id="178c1-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1149">Az.Network</span></span>
* <span data-ttu-id="178c1-1150">AzureFirewall 애플리케이션, NAT 및 네트워크 규칙에서 IpGroups 지원.</span><span class="sxs-lookup"><span data-stu-id="178c1-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1151">Az.Resources</span></span>
* <span data-ttu-id="178c1-1152">이름이 일부 내장 매개 변수 이름과 충돌하는 경우 템플릿 배포가 템플릿 매개 변수를 읽지 못하는 문제 수정.</span><span class="sxs-lookup"><span data-stu-id="178c1-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="178c1-1153">정책 세트 정의 내에 그룹화 지원을 도입하는 새로운 API 버전 2019-09-01을 사용하도록 정책 cmdlet 업데이트.</span><span class="sxs-lookup"><span data-stu-id="178c1-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1154">Az.Sql</span></span>
* <span data-ttu-id="178c1-1155">취약성 평가 자동 활성화에서 스토리지 생성을 StorageV2로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="178c1-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1156">Az.Storage</span></span>
* <span data-ttu-id="178c1-1157">Oauth 인증을 기반으로 스토리지 컨텍스트를 사용하여 Blob/컨테이너 ID 기반 SAS 토큰 생성 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="178c1-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="178c1-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="178c1-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="178c1-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="178c1-1160">모든 Idenity SAS 토큰을 해지할 수 있도록 스토리지 계정 사용자 위임 키 해지 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="178c1-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="178c1-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="178c1-1162">새로운 API 버전 2019-06-01을 지원하기 위해 Microsoft.Azure.Management.Storage 14.2.0으로 업그레이드.</span><span class="sxs-lookup"><span data-stu-id="178c1-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="178c1-1163">File Share cmdlet의 관리 평면에서 5120을 초과하는 값에 대해 QuotaGiB(Gibyby의 공유 할당량)를 지원하고 'Quota' 매개 변수 별칭을 'QuotaGiB' 매개 변수에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="178c1-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="178c1-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="178c1-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="178c1-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="178c1-1166">매개 변수 'Quota'에 매개 변수 별칭 'QuotaGiB' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="178c1-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="178c1-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="178c1-1168">Set-AzStorageContainerAcl가 저장된 액세스 정책을 정리할 수 있는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="178c1-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="178c1-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="178c1-1170">3.1.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="178c1-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="178c1-1171">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="178c1-1172">Az.DataBoxEdge 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="178c1-1173">Az.SqlVirtualMachine 1.0.0 릴리스됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1174">Az.Compute</span></span>
* <span data-ttu-id="178c1-1175">VM Reapply 기능</span><span class="sxs-lookup"><span data-stu-id="178c1-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="178c1-1176">Set-AzVM cmdlet에 Reapply 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="178c1-1177">VM 확장 집합 AutomaticRepairs 기능:</span><span class="sxs-lookup"><span data-stu-id="178c1-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="178c1-1178">다음 cmdlet에 EnableAutomaticRepair, AutomaticRepairGracePeriod 및 AutomaticRepairMaxInstanceRepairsPercent 매개 변수를 추가합니다.   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="178c1-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="178c1-1179">New-AzVM에 대한 교차 테넌트 갤러리 이미지 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="178c1-1180">New-AzVM, New-AzVMConfig 및 New-AzVmss cmdlet의 Priority 매개 변수의 인수 완성자에 'Spot' 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="178c1-1181">Add-AzVmssDataDisk cmdlet에 DiskIOPSReadWrite 및 DiskMBpsReadWrite 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="178c1-1182">New-AzGalleryImageVersion cmdlet의 SourceImageId 매개 변수를 선택 사항으로 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="178c1-1183">New-AzGalleryImageVersion cmdlet에 OSDiskImage 및 DataDiskImage 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="178c1-1184">New-AzGalleryImageDefinition cmdlet에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="178c1-1185">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 SkipExtensionsOnOverprovisionedVMs 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="178c1-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="178c1-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="178c1-1187">cmdlet `Get-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="178c1-1188">주문 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-1188">Get the Order</span></span>
* <span data-ttu-id="178c1-1189">cmdlet `New-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="178c1-1190">새 주문 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-1190">Create new Order</span></span>
* <span data-ttu-id="178c1-1191">cmdlet `Remove-AzDataBoxEdgeOrder` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="178c1-1192">주문 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1192">Remove the Order</span></span>
* <span data-ttu-id="178c1-1193">cmdlet `New-AzDataBoxEdgeShare` 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="178c1-1194">이제 로컬 공유를 만듬</span><span class="sxs-lookup"><span data-stu-id="178c1-1194">Now creates Local Share</span></span>
* <span data-ttu-id="178c1-1195">cmdlet `Set-AzDataBoxEdgeRole` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="178c1-1196">이제 IotRole을 공유에 매핑할 수 있음</span><span class="sxs-lookup"><span data-stu-id="178c1-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="178c1-1197">cmdlet `Invoke-AzDataBoxEdgeDevice` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="178c1-1198">스캔 업데이트 호출, 업데이트 다운로드, 디바이스에 업데이트 설치</span><span class="sxs-lookup"><span data-stu-id="178c1-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="178c1-1199">cmdlet `Get-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="178c1-1200">트리거에 대한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="178c1-1201">cmdlet `New-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="178c1-1202">새 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-1202">Create new Triggers</span></span>
* <span data-ttu-id="178c1-1203">cmdlet `Remove-AzDataBoxEdgeTrigger` 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="178c1-1204">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1205">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1206">ADF .Net SDK 버전을 4.4.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="178c1-1207">'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 'ExpressCustomSetup' 매개 변수를 추가하여 사용자 지정 설치 스크립트 없이 설치 구성 및 타사 구성 요소를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-1209">Get-AzDataLakeStoreDeletedItem 및 Restore-AzDataLakeStoreDeletedItem의 설명서 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1210">Az.EventHub</span></span>
* <span data-ttu-id="178c1-1211">10301 문제 해결: SAS 토큰 날짜 형식 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-1213">Enable-AzFrontDoorCustomDomainHttps 및 New-AzFrontDoorFrontendEndpointObject에 MinimumTlsVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="178c1-1214">New-AzFrontDoorHealthProbeSettingObject에 HealthProbeMethod 및 EnabledState 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="178c1-1215">BackendPoolsSettings 개체를 생성하여 Front Door 생성/업데이트에 전달하는 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="178c1-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="178c1-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1217">Az.Network</span></span>
* <span data-ttu-id="178c1-1218">'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 및 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 옵션 예제를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="178c1-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="178c1-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="178c1-1220">PrivateDns .net sdk를 버전 1.0.0으로 업데이트함</span><span class="sxs-lookup"><span data-stu-id="178c1-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1222">보호를 사용하도록 설정할 때 디스크 유형을 선택하도록 Azure Site Recovery 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="178c1-1223">복구 계획 동작 편집을 위한 Azure Site Recovery 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="178c1-1224">파일 스트림 DB를 허용하도록 Azure Backup SQL 복원 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="178c1-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="178c1-1225">Az.RedisCache</span></span>
* <span data-ttu-id="178c1-1226">'New-AzRedisCache' 및 'Set-AzRedisCache' cmdlet에 'MinimumTlsVersion' 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="178c1-1227">'Get-AzRedisCache' cmdlet 출력에 'MinimumTlsVersion'도 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="178c1-1228">'Set-AzRedisCache' 및 'New-AzRedisCache' cmdlet의 '-Size' 매개 변수에 대한 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1229">Az.Resources</span></span>
- <span data-ttu-id="178c1-1230">정책 할당에 새로운 EnforcementMode 속성이 있는 새 api 버전 2019-06-01을 사용하도록 정책 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="178c1-1231">정책 정의 만들기 도움말 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="178c1-1232">Remove-AZADServicePrincipal -ServicePrincipalName 버그를 수정하고, 서비스 사용자 이름을 찾을 수 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="178c1-1233">New-AZADServicePrincipal 버그를 수정하고, 테넌트에 구독이 없으면 null 참조를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="178c1-1234">연결된 애플리케이션에만 자격 증명을 추가하도록 New-AzAdServicePrincipal을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1235">Az.Sql</span></span>
* <span data-ttu-id="178c1-1236">데이터베이스 ReadReplicaCount에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="178c1-1237">영역 중복이 설정되지 않은 경우 Set-AzSqlDatabase가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="178c1-1238">3.0.0 - 2019년 11월</span><span class="sxs-lookup"><span data-stu-id="178c1-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="178c1-1239">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-1239">General</span></span>
* <span data-ttu-id="178c1-1240">Az.PrivateDns 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1241">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1242">'Resolve-Error' 별칭에 사용 중단 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="178c1-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="178c1-1243">Az.Advisor</span></span>
* <span data-ttu-id="178c1-1244">Get-AzAdvisorRecommendation cmdlet에 새로운 '운영 효율성' 범주가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-1245">Az.Batch</span></span>
* <span data-ttu-id="178c1-1246">`BatchAccountContext`의 `CoreQuota` 이름이 `DedicatedCoreQuota`로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="178c1-1247">또한 `LowPriorityCoreQuota`가 새로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="178c1-1248">이 변경 사항은 **Get-AzBatchAccount**에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="178c1-1249">이제 **New-AzBatchTask** `-ResourceFile` 매개 변수는 새로운 **New-AzBatchResourceFile** cmdlet을 사용하여 구성할 수 있는 `PSResourceFile` 개체의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="178c1-1250">새로운 **New-AzBatchResourceFile** cmdlet을 통해 `PSResourceFile` 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="178c1-1251">이들은 `-ResourceFile` 매개 변수의 **New-AzBatchTask**에 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="178c1-1252">그에 따라 기존 `HttpUrl` 방법 외에도 두 가지 종류의 리소스 파일이 새롭게 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="178c1-1253">`AutoStorageContainerName` 기반 리소스 파일은 전체 자동 스토리지 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="178c1-1254">`StorageContainerUrl` 기반 리소스 파일은 URL에 지정된 컨테이너를 일괄 처리 노드에 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="178c1-1255">**Get-AzBatchApplication**으로 반환되는 `PSApplication`의 `ApplicationPackages` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="178c1-1256">이제 **Get-AzBatchApplicationPackage**를 사용하여 애플리케이션 내부의 특정 패키지를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="178c1-1257">예: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`</span><span class="sxs-lookup"><span data-stu-id="178c1-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="178c1-1258">**Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** 및 **Set-AzBatchApplication**에서 `ApplicationId` 이름이 `ApplicationName`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="178c1-1259">이제 `ApplicationId`는 `ApplicationName`의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="178c1-1260">새로운 `PSWindowsUserConfiguration` 속성이 `PSUserAccount`에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="178c1-1261">`PSApplicationPackage`에서 `Version` 이름이 `Name`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="178c1-1262">`PSResourceFile`에서 `BlobSource` 이름이 `HttpUrl`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="178c1-1263">`PSVirtualMachineConfiguration`에서 `OSDisk` 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="178c1-1264">**Set-AzBatchPoolOSVersion**이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="178c1-1265">이 작업은 더 이상 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="178c1-1266">`PSCloudServiceConfiguration`에서 `TargetOSVersion`이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="178c1-1267">`PSCloudServiceConfiguration`에서 `CurrentOSVersion` 이름이 `OSVersion`으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="178c1-1268">`PSPoolUsageMetrics`에서 `DataEgressGiB` 및 `DataIngressGiB`가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="178c1-1269">**Get-AzBatchNodeAgentSku**가 제거되고 **Get-AzBatchSupportedImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="178c1-1270">**Get-AzBatchSupportedImage**가 **Get-AzBatchNodeAgentSku**와 동일한 데이터를 반환하지만 더 친숙한 형식이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="178c1-1271">이제 확인되지 않은 이미지도 새롭게 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="178c1-1272">각 이미지의 `Capabilities` 및 `BatchSupportEndOfLife`에 대한 추가 정보도 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="178c1-1273">**New-AzBatchPool**의 새로운 `MountConfiguration` 매개 변수를 통해 풀의 각 노드에서 원격 파일 시스템을 마운트할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="178c1-1274">이제 트래픽의 소스 포트를 기준으로 풀에 대한 네트워크 액세스를 차단하는 네트워크 보안 규칙이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="178c1-1275">이 작업은 `PSNetworkSecurityGroupRule`에서 `SourcePortRanges` 속성을 통해 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="178c1-1276">컨테이너를 실행할 때 Batch는 이제 컨테이너 작업 디렉터리 또는 일괄 처리 태스크 작업 디렉터리에서 작업 실행을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="178c1-1277">이 작업은 `PSTaskContainerSettings`에서 `WorkingDirectory` 속성에 의해 제어됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="178c1-1278">새로운 `PublicIPs` 속성을 통해 `PSNetworkConfiguration`에서 공용 IP의 컬렉션을 지정할 수 있는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="178c1-1279">그 결과 사용자 제공 IP 목록의 IP가 풀에 있는 노드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="178c1-1280">지정하지 않은 경우 이제 `PSSTartTask`에서 `WaitForSuccess`의 기본값은 `$True`입니다(이전에는 `$False`).</span><span class="sxs-lookup"><span data-stu-id="178c1-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="178c1-1281">지정하지 않은 경우 이제 `PSAutoUserSpecification`에서 `Scope`의 기본값은 `Pool`입니다(이전에는 Windows의 경우 `Task`, Linux의 경우에는 `Pool`).</span><span class="sxs-lookup"><span data-stu-id="178c1-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-1282">Az.Cdn</span></span>
* <span data-ttu-id="178c1-1283">RulesEngine에 UrlRewriteAction 및 CacheKeyQueryStringAction이 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="178c1-1284">New-AzDeliveryRuleCondition cmdlet에서 'Selector' 입력 누락과 같은 여러 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1285">Az.Compute</span></span>
* <span data-ttu-id="178c1-1286">디스크 암호화 집합 기능</span><span class="sxs-lookup"><span data-stu-id="178c1-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="178c1-1287">새 cmdlet:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="178c1-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="178c1-1288">DiskEncryptionSetId 매개 변수가 다음 cmdlet에 추가되었습니다.   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="178c1-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="178c1-1289">DiskEncryptionSetId 및 EncryptionType 매개 변수가 다음 cmdlet에 추가되었습니다.   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="178c1-1290">New-AzVmssIPConfig에 PublicIPAddressVersion 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="178c1-1291">사용자 지정 스크립트 확장의 FileUris를 공용 설정에서 보호된 설정으로 이동</span><span class="sxs-lookup"><span data-stu-id="178c1-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="178c1-1292">New-AzVmss, New-AzVmssConfig 및 Update-AzVmss cmdlet에 ScaleInPolicy 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="178c1-1293">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="178c1-1293">Breaking changes</span></span>
    - <span data-ttu-id="178c1-1294">CreateOption이 업로드일 때 UploadSizeInBytes 매개 변수가 New-AzDiskConfig에 대해 DiskSizeGB 대신 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="178c1-1295">GalleryImageVersion 개체에서 PublishingProfile.Source.ManagedImage.Id가 StorageProfile.Source.Id로 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1296">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1297">ADF .Net SDK 버전을 4.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-1299">ADLS SDK 버전 업데이트(https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , 다음 수정 사항 제공</span><span class="sxs-lookup"><span data-stu-id="178c1-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="178c1-1300">휴지통 또는 디렉터리 항목의 creationtime을 역직렬화할 수 없을 때 예외가 발생하지 않도록 방지합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="178c1-1301">adlsclient에서 요청별 시간 제한 설정 노출</span><span class="sxs-lookup"><span data-stu-id="178c1-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="178c1-1302">badoffset 복구를 위한 원본 syncflag 전달 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="178c1-1303">응답이 확인된 후 연속 토큰을 검색하기 위한 EnumerateDirectory 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="178c1-1304">Concat 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-1306">모듈 간 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-1307">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-1308">ADLSGen1 스토리지가 포함된 클러스터를 가져오기 위해 Get-AzHDInsightCluster를 사용할 때 고객에게 '올바른 Base-64 문자열이 아닙니다' 오류가 표시되는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="178c1-1309">고객이 Azure Data Lake에 액세스하기 위해 서비스 주체 애플리케이션 ID를 제공할 수 있도록 세 가지 cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig 및 New-AzHDInsightCluster에 이름이 'ApplicationId'인 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="178c1-1310">Microsoft.Azure.Management.HDInsight가 2.1.0에서 5.1.0으로 변경됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="178c1-1311">다음 5가지 cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="178c1-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="178c1-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="178c1-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="178c1-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="178c1-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="178c1-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="178c1-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="178c1-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="178c1-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="178c1-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="178c1-1317">다음 3가지 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="178c1-1318">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="178c1-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="178c1-1319">Get-AzHDInsightOMS 대신 Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="178c1-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="178c1-1320">Disable-AzHDInsightOMS 대신 Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="178c1-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="178c1-1321">특정 위치의 기능 정보 가져오기를 지원하도록 cmdlet Get-AzHDInsightProperties가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="178c1-1322">Add-AzHDInsightConfigValue에서 매개 변수 집합('Spark1', 'Spark2')이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="178c1-1323">cmdlet Add-AzHDInsightSecurityProfile의 도움말 문서에 예제를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="178c1-1324">다음 cmdlet의 출력 유형이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="178c1-1325">Get-AzHDInsightProperties의 출력 유형이 CapabilitiesResponse에서 AzureHDInsightCapabilities로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="178c1-1326">Remove-AzHDInsightCluster의 출력 유형이 ClusterGetResponse에서 bool로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="178c1-1327">Set-AzHDInsightGatewaySettings의 출력 유형이 HttpConnectivitySettings에서 GatewaySettings로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="178c1-1328">몇 가지 시나리오 테스트 사례가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="178c1-1329">일부 별칭 제거: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="178c1-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1330">Az.IotHub</span></span>
* <span data-ttu-id="178c1-1331">주요 변경 내용:</span><span class="sxs-lookup"><span data-stu-id="178c1-1331">Breaking changes:</span></span>
    - <span data-ttu-id="178c1-1332">'Add-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="178c1-1333">'Add-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="178c1-1334">'Get-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="178c1-1335">'Get-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="178c1-1336">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="178c1-1337">'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 유형의 'OperationsMonitoringProperties' 속성이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="178c1-1338">'New-AzIotHubExportDevice' cmdlet이 더 이상 'New-AzIotHubExportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="178c1-1339">'New-AzIotHubImportDevice' cmdlet이 더 이상 'New-AzIotHubImportDevices' 별칭을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="178c1-1340">'Remove-AzIotHubEventHubConsumerGroup' cmdlet이 'EventHubEndpointName' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="178c1-1341">'Remove-AzIotHubEventHubConsumerGroup' cmdlet에 대한 매개 변수 집합 '__AllParameterSets'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="178c1-1342">'Set-AzIotHub' cmdlet이 'OperationsMonitoringProperties' 매개 변수를 더 이상 지원하지 않으며 원래 매개 변수 이름에 대해 별칭을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="178c1-1343">'Set-AzIotHub' cmdlet에 대한 매개 변수 집합 'UpdateOperationsMonitoringProperties'가 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1345">Azure Site Recovery가 Azure-Azure를 위한 NSG, 공용 IP 및 내부 부하 분산 장치와 같은 네트워킹 리소스 구성을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-1346">Azure Site Recovery가 vMWare-Azure를 위한 관리 디스크에 쓰기를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="178c1-1347">Azure Site Recovery가 vMWare-Azure를 위한 NIC 감소를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="178c1-1348">Azure Site Recovery가 Azure-Azure를 위한 가속 네트워킹을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-1349">Azure Site Recovery가 Azure-Azure를 위한 에이전트 자동 업데이트를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-1350">Azure Site Recovery가 Azure-Azure를 위한 표준 SSD를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-1351">Azure Site Recovery가 Azure-Azure를 위한 두 가지 Azure 디스크 암호화 전달을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-1352">Azure Site Recovery가 Azure-Azure를 위한 새로 추가된 디스크 보호를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-1353">VM을 위한 SoftDelete 기능 및 softdelete를 위한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1354">Az.Resources</span></span>
* <span data-ttu-id="178c1-1355">종속성 어셈블리 Microsoft.Extensions.Caching.Memory가 1.1.1에서 2.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1356">Az.Network</span></span>
* <span data-ttu-id="178c1-1357">일반 서비스 공급자 지원을 위해 PrivateEndpointConnection에 대한 모든 cmdlet이 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="178c1-1358">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="178c1-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="178c1-1364">PrivateLinkResource에 대한 새 cmdlet이 추가되었고 일반 서비스 공급자도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="178c1-1365">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-1365">New cmdlet:</span></span>
        - <span data-ttu-id="178c1-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="178c1-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="178c1-1367">Proxy Protocol V2 기능에 대한 새 필드 및 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="178c1-1368">PrivateLinkService에서 EnableProxyProtocol 속성 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="178c1-1369">PrivateEndpointConnection에서 LinkIdentifier 속성 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="178c1-1370">새로운 선택적인 매개 변수인 EnableProxyProtocol을 추가하도록 New-AzPrivateLinkService가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="178c1-1371">'New-AzApplicationGatewaySku' 참조 설명서의 잘못된 매개 변수 설명 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="178c1-1372">Azure 방화벽 정책을 지원하는 새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="178c1-1373">VirtualHub의 자식 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="178c1-1374">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="178c1-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="178c1-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="178c1-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="178c1-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="178c1-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="178c1-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="178c1-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="178c1-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="178c1-1380">VirtualHub의 새로운 속성 Sku 및 VirtualWan의 VirtualWANType에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="178c1-1381">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="178c1-1382">New-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="178c1-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="178c1-1383">Update-AzVirtualHub: 추가된 매개 변수 Sku</span><span class="sxs-lookup"><span data-stu-id="178c1-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="178c1-1384">New-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="178c1-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="178c1-1385">Update-AzVirtualWan: 추가된 매개 변수 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="178c1-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="178c1-1386">HubVnetConnection, VpnConnection 및 ExpressRouteConnection에 대한 EnableInternetSecurity 속성 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="178c1-1387">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="178c1-1389">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="178c1-1390">New-AzureRmVirtualHubVnetConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="178c1-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="178c1-1391">New-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="178c1-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="178c1-1392">Update-AzureRmVpnConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="178c1-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="178c1-1393">New-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="178c1-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="178c1-1394">Set-AzureRmExpressRouteConnection: 추가된 매개 변수 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="178c1-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="178c1-1395">TopLevel WebApplicationFirewall 정책 구성을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="178c1-1396">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="178c1-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="178c1-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="178c1-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="178c1-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="178c1-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="178c1-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="178c1-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="178c1-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="178c1-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="178c1-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="178c1-1403">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="178c1-1404">New-AzApplicationGatewayFirewallPolicy: 추가된 매개 변수 PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="178c1-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="178c1-1405">CustomRule에서 Geo-Match 연산자를 위한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="178c1-1406">FirewallCondition에서 연산자에 GeoMatch 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="178c1-1407">perListener 및 perSite 방화벽 규칙에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="178c1-1408">선택적 매개 변수로 다음 cmdlet이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="178c1-1409">New-AzApplicationGatewayHttpListener: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="178c1-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="178c1-1410">New-AzApplicationGatewayPathRuleConfig: 추가된 매개 변수 FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="178c1-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="178c1-1411">'PSBastion'에서 이름이 AzureBastionSubnet인 필수 서브넷의 수정은 대소문자를 구분하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="178c1-1412">Azure Firewall을 위한 네트워크 규칙의 대상 FQDN 및 NAT 규칙의 번역된 FQDN 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="178c1-1413">IpGroup의 최상위 리소스 RouteTables에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="178c1-1414">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="178c1-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="178c1-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="178c1-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="178c1-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="178c1-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="178c1-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="178c1-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-1420">Add-AzVmssSecret에서 지원되기 때문에 Add-AzServiceFabricApplicationCertificate cmdlet이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1421">Az.Sql</span></span>
* <span data-ttu-id="178c1-1422">Managed Instances에서 삭제된 데이터베이스의 복원을 위한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="178c1-1423">이전의 감사 cmdlet 코드가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="178c1-1424">사용되지 않는 별칭이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="178c1-1425">Get-AzSqlDatabaseIndexRecommendations(대신 Get-AzSqlDatabaseIndexRecommendation 사용)</span><span class="sxs-lookup"><span data-stu-id="178c1-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="178c1-1426">Get-AzSqlDatabaseRestorePoints(대신 Get-AzSqlDatabaseRestorePoint 사용)</span><span class="sxs-lookup"><span data-stu-id="178c1-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="178c1-1427">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="178c1-1428">사용되지 않는 취약성 평가 설정 cmdlet에 대한 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="178c1-1429">지능형 위협 탐지 설정 cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="178c1-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="178c1-1430">데이터베이스의 열에 대한 민감도 권장 사항의 사용 여부를 제어하는 cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1431">Az.Storage</span></span>
* <span data-ttu-id="178c1-1432">스토리지 계정을 만들거나 업데이트할 때 큰 파일 공유 사용 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="178c1-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="178c1-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="178c1-1435">파일 핸들을 닫거나/가져올 때, DeletePending 상태의 개체로 인한 오류를 방지하기 위해 입력 경로가 파일 디렉터리인지 또는 파일인지를 확인하는 과정을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="178c1-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="178c1-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="178c1-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="178c1-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="178c1-1438">2.8.0 - 2019년 10월</span><span class="sxs-lookup"><span data-stu-id="178c1-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="178c1-1439">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-1439">General</span></span>
* <span data-ttu-id="178c1-1440">Az.HealthcareApis 1.0.0 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1441">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1442">생성된 모듈에 대한 원격 분석 및 URL 다시 작성이 업데이트되고, Windows 단위 테스트가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-1444">**Set-AzApiManagementApi** - API 업데이트 지원이 ApiVersionSet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="178c1-1445">문제 https://github.com/Azure/azure-powershell/issues/10068 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-1446">Az.Automation</span></span>
* <span data-ttu-id="178c1-1447">Linux 다시 부팅 설정 매개 변수에 대한 New-AzureAutomationSoftwareUpdateConfiguration cmdlet이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-1448">Az.Batch</span></span>
* <span data-ttu-id="178c1-1449">**Get-AzBatchNodeAgentSku**가 더 이상 사용되지 않으며, 2.0.0 버전의 **Get-AzBatchSupportImage**로 대체되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1450">Az.Compute</span></span>
* <span data-ttu-id="178c1-1451">Priority, EvictionPolicy 및 MaxPrice 매개 변수가 New-AzVM 및 New-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="178c1-1452">Add-AzVMAdditionalUnattendContent 및 Add-AzVMSshPublicKey cmdlet에 대한 경고 메시지와 도움말 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="178c1-1453">Set-AzVMDiskEncryptionExtension의 관리 디스크가 있는 Linux VM에 대한 -skipVmBackup 예외가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="178c1-1454">Set-AzVMDiskEncryptionExtension의 두 가지 패스 시나리오에서 발생하는 암호화 설정 업데이트의 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1455">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1456">ADF V2 데이터 흐름에 대한 CRUD 명령으로 Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow 및 Get-AzDataFactoryV2DataFlow가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="178c1-1457">ADF V2 데이터 흐름 디버그 세션에 대한 작업 명령으로 Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 및 Stop-AzDataFactoryV2DataFlowDebugSession이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="178c1-1458">ADF .Net SDK 버전이 4.2.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-1460">도메인 없이 '-'가 있는 계정을 전달할 수 있도록 계정 유효성 검사가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="178c1-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="178c1-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="178c1-1462">PowerShell 버전이 1.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="178c1-1463">SDK 버전이 1.0.2로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="178c1-1464">새 SDK 버전을 참조하도록 테스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="178c1-1465">출력이 중첩 구조에서 평면화 구조로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1466">Az.IotHub</span></span>
* <span data-ttu-id="178c1-1467">새 라우팅 원본 추가: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="178c1-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="178c1-1468">사소한 버그 수정: Get-AzIothub에서 subscriptionId를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-1469">Az.Monitor</span></span>
* <span data-ttu-id="178c1-1470">작업 그룹에 대한 새 작업 그룹 수신기로 -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="178c1-1471">수신기에 사용하도록 설정된 일반 경고 스키마가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="178c1-1472">SMS, Azure 앱 푸시, ITSM 및 음성 수신기에는 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="178c1-1473">웹후크에서 이제 Azure Active Directory 인증을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1474">Az.Network</span></span>
* <span data-ttu-id="178c1-1475">서비스 엔드포인트 정책에 사용할 수 있는 별칭을 가져오기 위해 호출할 수 있는 새 Get-AzAvailableServiceAlias cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="178c1-1476">트래픽 선택기를 Virtual Network 게이트웨이 연결에 추가할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="178c1-1477">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="178c1-1479">cmdlet이 선택적인 -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection 매개 변수로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="178c1-1480">ESP 및 AH 프로토콜 지원이 네트워크 보안 규칙 구성에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="178c1-1481">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="178c1-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="178c1-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="178c1-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="178c1-1485">Cortex cmdlet의 예외 처리가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="178c1-1486">새 VirtualNetworkGateways 세대 및 SKU</span><span class="sxs-lookup"><span data-stu-id="178c1-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="178c1-1487">새 VirtualNetworkGateways 세대가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="178c1-1488">높은 처리량의 새 VirtualNetworkGateways SKU가 도입되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="178c1-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="178c1-1489">Az.RedisCache</span></span>
* <span data-ttu-id="178c1-1490">'-Size' 매개 변수에 대한 누락 값을 포함하도록 'Set-AzRedisCache' 참조 설명서가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1491">Az.Sql</span></span>
* <span data-ttu-id="178c1-1492">Managed Instance에서 Active Directory 관리자를 설정할 수 있는 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1493">Az.Storage</span></span>
* <span data-ttu-id="178c1-1494">스토리지 클라이언트 라이브러리가 11.1.0으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="178c1-1495">관리 평면 API를 사용하여 컨테이너를 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="178c1-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="178c1-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="178c1-1497">구독에서 스토리지 계정을 나열하면 NextPageLink를 통해 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="178c1-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="178c1-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="178c1-1499">Az.StorageSync</span></span>
* <span data-ttu-id="178c1-1500">Reset-AzStorageSyncServerCertificate의 9810 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-1501">Az.Websites</span></span>
* <span data-ttu-id="178c1-1502">앱의 ASP를 업데이트하는 Set-AzWebApp이 실패했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="178c1-1503">2.7.0 - 2019년 9월</span><span class="sxs-lookup"><span data-stu-id="178c1-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="178c1-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-1505">'Set-AzApiManagementPolicy' 참조 설명서에서 '-Format' 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="178c1-1506">참조 설명서에서 사용되지 않는 cmdlet 'Update-AzApiManagementDeployment'의 참조를 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="178c1-1507">그 대신 'Set-AzApiManagement'를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-1508">Az.Automation</span></span>
* <span data-ttu-id="178c1-1509">'Register-AzAutomationDscNode'에 대한 참조 설명서의 예제 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="178c1-1510">Register-AzAutomationDSCNode에 OS 제한에 대한 설명이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="178c1-1511">-Wait 옵션에 대한 Start-AzAutomationRunbook cmdlet Null 참조 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1512">Az.Compute</span></span>
* <span data-ttu-id="178c1-1513">New-AzDiskConfig에 UploadSizeInBytes 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="178c1-1514">New-AzSnapshotConfig에 증분 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="178c1-1515">다음과 같은 낮은 우선 순위의 가상 머신 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="178c1-1516">MaxPrice, EvictionPolicy 및 Priority 매개 변수가 New-AzVMConfig에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="178c1-1517">MaxPrice 매개 변수는 New-AzVmssConfig, Update-AzVM 및 Update-AzVmss cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="178c1-1518">구독의 모든 가용성 세트를 나열할 때 발생하는 Get-AzAvailabilitySet cmdlet에 대한 VM 참조 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="178c1-1519">Get-AzRemoteDesktopFile에 대한 null 예외가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="178c1-1520">종료 상대 위치에 대한 VHD 검색 메서드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="178c1-1521">New-AzVM 및 Update-AzVM에 대한 UltraSSD 이슈가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1522">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1523">ADF V2에 대한 3가지 새 명령 Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription 및 Get-AzDataFactoryV2TriggerSubscriptionStatus가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="178c1-1524">ADF .Net SDK 버전이 4.1.3으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-1525">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-1526">호출 주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="178c1-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1527">Az.IotHub</span></span>
* <span data-ttu-id="178c1-1528">지역 쌍 재해 복구 지역에 IotHub에 대한 장애 조치(failover) 호출 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="178c1-1529">IotHub에 대한 메시지 보강 관리 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="178c1-1530">새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="178c1-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="178c1-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="178c1-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="178c1-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="178c1-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="178c1-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="178c1-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="178c1-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-1535">Az.Monitor</span></span>
* <span data-ttu-id="178c1-1536">최신 모니터링 SDK, 즉, 0.24.1-preview를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="178c1-1537">메트릭 cmdlet에 줄 바꿈하지 않는 변경 내용을 추가합니다. 즉, 단위 열거형은 여러 새 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="178c1-1538">이러한 cmdlet은 읽기 전용이므로 cmdlet 입력이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="178c1-1539">이제 **ActionGroups** 요청의 api 버전은 **2019-06-01**이고, 이전에는 **2018-03-01**였습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="178c1-1540">시나리오 테스트가 이 변경 내용에 맞게 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="178c1-1541">**EmailReceiver** 및 **WebhookReceiver** 클래스에 대한 생성자가 새 필수 인수, 즉, **useCommonAlertSchema**라는 부울 값을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="178c1-1542">현재 이 값은 cmdlet의 주요 변경 사항을 숨기도록 **false**로 고정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="178c1-1543">**참고**: 이 변경 사항은 경고 팀에서 유효성을 검사해야 하는 임시 변경 내용입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="178c1-1544">이전 SDK에서 변경된 **Source** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="178c1-1545">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="178c1-1546">이전 SDK에서 변경된 **AlertingAction** 클래스(**ScheduledQueryRuleSource** 클래스와 관련됨)의 생성자에 대한 인수 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="178c1-1547">이번 변화로 인해 두 개의 단위 테스트를 수정해야 했습니다. 즉, 두 단위 테스트가 컴파일되었지만 테스트를 통과하지 못했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="178c1-1548">메트릭 경고 V2에 대한 동적 임계값 기준 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="178c1-1549">AzMetricAlertRuleV2Criteria: 이제 동적 임계값 조건도 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="178c1-1550">Add-AzMetricAlertRuleV2: 이제 동적 임계값 조건도 수락합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="178c1-1551">SQR(예약된 쿼리 규칙)의 향상된 기능</span><span class="sxs-lookup"><span data-stu-id="178c1-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="178c1-1552">Cmdlet이 'Location' 매개 변수를 두 가지 형식(eastus 같은 위치 또는 미국 동부 같은 위치 표시 이름)으로 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="178c1-1553">도움말 파일에 적절하게 표시된 'Enabled' 매개 변수</span><span class="sxs-lookup"><span data-stu-id="178c1-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="178c1-1554">선택적 매개 변수 'ActionGroup'에 대한 예제가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="178c1-1555">도움말 파일이 전체적으로 개선되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1555">Overall improved help files</span></span>
* <span data-ttu-id="178c1-1556">'Set-AzActionRule'의 범위 유형 결정 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1557">Az.Network</span></span>
* <span data-ttu-id="178c1-1558">'New-AzApplicationGateway' 참조 설명서의 잘못된 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="178c1-1559">'Get-AzNetworkWatcherPacketCapture' 참조 설명서에 패킷 캡처를 위한 모든 속성 검색과 관련된 메모가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="178c1-1560">NIC를 올바르게 열거하도록 'Test-AzNetworkWatcherIPFlow' 참조 설명서의 예제가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="178c1-1561">추가 세부 정보가 있는 경우 추가 세부 정보를 표시하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="178c1-1562">더 많은 형식의 SDK 예외를 처리하도록 클라우드 예외 구문 분석이 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="178c1-1563">보안 규칙 모델의 잘못된 매핑이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="178c1-1564">네트워크 인터페이스에 개인 IP 기능을 위한 속성이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="178c1-1565">PSNetworkInterface에 'PrivateEndpoint' 속성이 PSResourceId 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="178c1-1566">PSNetworkInterfaceIPConfiguration에 'PrivateLinkConnectionProperties' 속성이 PSIpConfigurationConnectivityInformation 형식으로 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="178c1-1567">새 모델 클래스 PSIpConfigurationConnectivityInformation이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="178c1-1568">Azure Firewall 리소스에 대한 새 ApplicationRuleProtocolType 'mssql'이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="178c1-1569">Virtual WAN에서 멀티 링크를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="178c1-1570">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1570">New cmdlets</span></span>
        - <span data-ttu-id="178c1-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="178c1-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="178c1-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="178c1-1573">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="178c1-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="178c1-1574">New-VpnSite</span></span>
        - <span data-ttu-id="178c1-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="178c1-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="178c1-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="178c1-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="178c1-1578">AzureRM cmdlet 대신 Az cmdlet을 사용하도록 일부 PowerShell 예제의 문서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1580">AzureVMpolicy 개체가 ProtectedItemsCount 특성으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="178c1-1581">VM 정책 및 원래 스토리지 계정 복원에 대한 테스트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1582">Az.Resources</span></span>
* <span data-ttu-id="178c1-1583">매개 변수 범위 없이 AzRoleAssignment를 호출할 수 없는 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-1585">'AzServiceFabricReliability' 참조 설명서에 대한 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="178c1-1586">애플리케이션 및 서비스를 관리하는 다음과 같은 새 cmdlet이 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="178c1-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="178c1-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="178c1-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="178c1-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="178c1-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="178c1-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="178c1-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="178c1-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="178c1-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="178c1-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="178c1-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="178c1-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="178c1-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="178c1-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="178c1-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="178c1-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="178c1-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="178c1-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="178c1-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="178c1-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="178c1-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="178c1-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="178c1-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="178c1-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="178c1-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="178c1-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="178c1-1600">Service Fabric SDK가 Service Fabric 리소스 공급자 api 버전 2019-03-01을 사용하는 1.2.0 버전으로 업그레이드되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="178c1-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="178c1-1601">Az.SignalR</span></span>
* <span data-ttu-id="178c1-1602">Update, Restart, CheckNameAvailability, GetUsage Cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1603">Az.Sql</span></span>
* <span data-ttu-id="178c1-1604">'Get-AzSqlElasticPool'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="178c1-1605">탄력적 풀을 만드는 vCore 예제가 추가되었습니다(AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="178c1-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="178c1-1606">Set-AzSqlServerAdvancedThreatProtectionPolicy 및 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy에서 EmailAddresses가 비어 있는 경우 EmailAddresses의 유효성을 검사하고 EmailAdmins가 false가 아닌지 확인하는 기능이 제거되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="178c1-1607">감사 범주를 사용하는 여러 진단 설정이 있는 경우 서버/데이터베이스 감사 설정을 제거하도록 설정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="178c1-1608">여러 Sql 취약성 평가 cmdlet에서 이메일 주소 유효성 검사가 수정되었습니다(Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 및 Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="178c1-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1609">Az.Storage</span></span>
* <span data-ttu-id="178c1-1610">'Get-AzStorageAccountKey'에 대한 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="178c1-1611">Azure 파일 업로드/다운에서, 원본 파일 SMB 속성(파일 특성, 파일 생성 시간, 파일을 마지막으로 쓴 시간)을 대상 파일에 보존하는 기능이 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="178c1-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="178c1-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="178c1-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="178c1-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="178c1-1614">컨테이너가 사용되는 ImmutabilityPolicy에서 properties/metadate fail을 사용하여 블록 Blob 업로드가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="178c1-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="178c1-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="178c1-1616">관리 평면 API를 사용하여 Azure 파일 공유 관리를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="178c1-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="178c1-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="178c1-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="178c1-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="178c1-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="178c1-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="178c1-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="178c1-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-1621">Az.Websites</span></span>
* <span data-ttu-id="178c1-1622">앱을 새 ASP로 마이그레이션할 때 웹앱 태그가 삭제되는 이슈가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="178c1-1623">Linux와 Windows에서 모두 작동하도록 Publish-AzureWebapp이 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="178c1-1624">'Get-AzWebAppPublishingProfile' 참조 설명서의 예제가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="178c1-1625">2.6.0 - 2019년 8월</span><span class="sxs-lookup"><span data-stu-id="178c1-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="178c1-1626">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-1626">General</span></span>
* <span data-ttu-id="178c1-1627">여러 모듈에서 기타 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1628">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1629">Azure Functions 인증에서 사용자가 할당한 MSI가 지원됨(# 9479)</span><span class="sxs-lookup"><span data-stu-id="178c1-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="178c1-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="178c1-1630">Az.Aks</span></span>
* <span data-ttu-id="178c1-1631">'Get-AzAks' 출력 관련 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="178c1-1632">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9847 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-1634">문제 https://github.com/Azure/azure-powershell/issues/9351 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="178c1-1635">productId, apiId, groupId 및 userId에 대한 제한을 적용하지 않는 .Net NuGet 버전이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="178c1-1636">**Get-AzApiManagementProduct** - API를 사용하는 제품에 대한 쿼리 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="178c1-1637">**New-AzApiManagementApiRevision** - 새 API 수정(https://github.com/Azure/azure-powershell/issues/9752 )을 만들 때 ApiRevisionDescription이 설정되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="178c1-1638">'PsApiManagementOAuth2AuthrozationServer' 모델의 오타가 'PsApiManagementOAuth2AuthorizationServer'로 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-1639">Az.Batch</span></span>
* <span data-ttu-id="178c1-1640">도움말 메시지 및 설명서에서 Windows를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-1641">Az.Cdn</span></span>
* <span data-ttu-id="178c1-1642">CDN 모듈 변환 도우미의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1643">Az.Compute</span></span>
* <span data-ttu-id="178c1-1644">VmssId가 New-AzVMConfig cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="178c1-1645">TerminateScheduledEvents 및 TerminateScheduledEventNotBeforeTimeoutInMinutes 매개 변수가 New-AzVmssConfig 및 Update-AzVmss에 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="178c1-1646">HyperVGeneration 속성이 VM 이미지 개체에 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="178c1-1647">Host 및 HostGroup 기능이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="178c1-1648">새 cmdlet:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="178c1-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="178c1-1649">HostId 매개 변수가 New-AzVMConfig 및 New-AzVM 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="178c1-1650">'Invoke-AzVMRunCommand' 설명서의 예제에서 올바른 매개 변수 이름을 사용하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="178c1-1651">'Set-AzVMDiskEncryptionExtension' 및 'Set-AzVmssDiskEncryptionExtension' 참조 설명서의 '-VolumeType' 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1652">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1653">'New-AzDataFactoryEncryptValue' 설명서에서 'Windows'를 대문자로 시작하도록 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="178c1-1654">ADF .Net SDK 버전이 4.1.2로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="178c1-1655">자체 호스팅 통합 런타임을 SSIS Integration Runtime의 프록시로 설정할 수 있도록 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' 및 'DataProxyStagingPath' 매개 변수가 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd에 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="178c1-1656">PSTriggerRun에서 트리거된 파이프라인, 메시지 및 속성을 표시하고, PSActivityRun에서 작업 유형을 표시하도록 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-1658">오류 또는 원격 예외에 대한 Get-DataLakeStoreDeletedItem 중단이 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1659">Az.EventHub</span></span>
* <span data-ttu-id="178c1-1660">#9658 문제 해결: Set-AzEventHubNetworkRuleSet의 VirtualNteworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="178c1-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="178c1-1661">#9558 문제 해결: Set-AzEventHubNamespace에서 PUT 대신 PATCH가 사용됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="178c1-1662">EnableKafka 매개 변수가 Set-AzEventHubNamespace cmdlet에 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="178c1-1663">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="178c1-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="178c1-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="178c1-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="178c1-1665">'Azure'가 모두 소문자인 설명서의 오타가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-1666">Az.Monitor</span></span>
* <span data-ttu-id="178c1-1667">도움말 설명서에서 잘못된 매개 변수 이름이 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1668">Az.Network</span></span>
* <span data-ttu-id="178c1-1669">New-AzPrivateLinkServiceIpConfig가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="178c1-1670">서버 쪽에서 사용되지 않으므로 'PublicIpAddress' 매개 변수가 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="178c1-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="178c1-1671">현재 IP 구성이 기본 구성인지 여부를 나타내는 하나의 선택적 'Primary' 매개 변수가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="178c1-1672">SDK의 요청 오류 예외 처리가 향상됨 - 이전의 SDK 예외가 올바르게 처리되지 않아 주요 오류 세부 정보가 표시되지 않은 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="178c1-1673">올바른 IPv6 접두사 길이를 확인하기 위해 Ipv6 IP 접두사에 대한 유효성 검사 논리가 조정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="178c1-1674">Get-AzVirtualNetworkSubnetConfig가 업데이트됨: 서브넷 리소스 ID별로 가져오도록 설정되는 매개 변수 세트가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="178c1-1675">AzNetworkServiceTag의 Location(위치) 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-1677">'New-AzOperationalInsightsLinuxSyslogDataSource'에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="178c1-1678">예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1678">Added example</span></span>
    - <span data-ttu-id="178c1-1679">'-Name' 매개 변수에 대한 설명이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="178c1-1680">New-AzOperationalInsightsWindowsEventDataSource에 대한 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="178c1-1681">New-AzOperationalInsightsWindowsEventDataSource의 -Name 매개 변수에 대한 설명이 변경됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1683">'Get-AzRecoveryServicesBackupJobDetail.md'가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1684">Az.Resources</span></span>
* <span data-ttu-id="178c1-1685">Microsoft 리소스에 대한 새 2019-05-10 API 버전 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="178c1-1686">변수, 리소스 및 속성에 대한 'copy.count = 0' 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="178c1-1687">'condition = false' 또는 'copy.count = 0'인 리소스가 완료 모드에서 삭제됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="178c1-1688">정책을 구독 수준에서 도움말 문서에 할당하는 예제가 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="178c1-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="178c1-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="178c1-1690">#9658 문제 해결: Set-AzServiceBusNetworkRuleSet의 VirtualNetworkRule 매개 변수에 대한 오타</span><span class="sxs-lookup"><span data-stu-id="178c1-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="178c1-1691">#9786 문제 해결: Listen(수신 대기) 전용 권한이 있는 규칙을 만들 수 없음</span><span class="sxs-lookup"><span data-stu-id="178c1-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="178c1-1692">큐 및 토픽에 대한 이름 가용성을 확인하는 새 'Test-AzServiceBusNameAvailability' 명령이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-1694">노드 유형 추가 cmdlet 버그 수정:</span><span class="sxs-lookup"><span data-stu-id="178c1-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="178c1-1695">서비스 패브릭 클러스터와 관련이 없는 다른 vmss가 리소스 그룹에 있을 때 발생하는 NullReferenceException 버그</span><span class="sxs-lookup"><span data-stu-id="178c1-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="178c1-1696">문제 해결: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="178c1-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="178c1-1697">virtualNetwork가 클러스터의 다른 리소스 그룹에 있을 때 cmdlet이 실패하는 버그가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="178c1-1698">문제 해결: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="178c1-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="178c1-1699">Add-AzServiceFabricApplicationCertificate cmdlet이 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="178c1-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1700">Az.Sql</span></span>
* <span data-ttu-id="178c1-1701">이전의 Auditing(감사) cmdlet에 대한 설명서가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1702">Az.Storage</span></span>
* <span data-ttu-id="178c1-1703">더 많은 시나리오를 cmdlet 예제에 추가하고 매개 변수 설명을 업데이트하여 Get/Close-AzStorageFileHandle에 대한 도움말이 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="178c1-1704">Blob 업로드 및 Blob 복사에서 StandardBlobTier가 지원됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="178c1-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="178c1-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="178c1-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="178c1-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="178c1-1707">Blob 복사에서 우선 순위 리하이드레이션이 지원됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="178c1-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="178c1-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-1709">Az.Websites</span></span>
* <span data-ttu-id="178c1-1710">Set-AzWebApp 및 Set-AzWebAppSlot에서 -AppSettings 매개 변수에 대한 설명이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="178c1-1711">2.5.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="178c1-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1712">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1713">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="178c1-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="178c1-1715">'Remove-AzApplicationInsightsApiKey' 설명서의 예제 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-1716">Az.Automation</span></span>
* <span data-ttu-id="178c1-1717">리소스 문자열의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-1719">NetworkRuleSet 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1720">Az.Compute</span></span>
* <span data-ttu-id="178c1-1721">VM 인스턴스 보기 개체의 누락된 속성(ComputerName, OsName, OsVersion 및 HyperVGeneration)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="178c1-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="178c1-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="178c1-1723">복제 매개 변수의 Remove-AzContainerRegistryReplication에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="178c1-1724">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9633 을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1725">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1726">ADF .Net SDK 버전을 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="178c1-1727">'Get-AzDataFactoryV2PipelineRun' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1728">Az.EventHub</span></span>
* <span data-ttu-id="178c1-1729">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="178c1-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="178c1-1730">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-1731">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-1732">인증서 정책에 대한 KeySize 지정을 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="178c1-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="178c1-1733">Az.LogicApp</span></span>
* <span data-ttu-id="178c1-1734">모든 맵 유형을 나열하도록 Get-AzIntegrationAccountMap 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="178c1-1735">필터링을 위해 새 MapType 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="178c1-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="178c1-1737">API 버전 2019-06-01(GA)에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1738">Az.Network</span></span>
* <span data-ttu-id="178c1-1739">프라이빗 엔드포인트 및 프라이빗 링크 서비스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="178c1-1740">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1740">New cmdlets</span></span>
        - <span data-ttu-id="178c1-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="178c1-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="178c1-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="178c1-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="178c1-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="178c1-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="178c1-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="178c1-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="178c1-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="178c1-1749">기능에 대한 새로운 명령이 업데이트됨: Virtualnetwork의 서브넷에 있는 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 플래그</span><span class="sxs-lookup"><span data-stu-id="178c1-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="178c1-1750">업데이트된 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="178c1-1751">이 서브넷의 프라이빗 엔드포인트에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateEndpointNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="178c1-1752">이 서브넷의 프라이빗 연결 서비스에 네트워크 정책을 적용할지 여부를 나타내는 선택적 매개 변수 -PrivateLinkServiceNetworkPoliciesFlag가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="178c1-1753">AzPrivateLinkService의 cmdlet 매개 변수 'ServiceName'이 이전 버전과의 호환성을 위해 별칭 'ServiceName'을 사용한 'Name'으로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="178c1-1754">네트워크 보안 규칙 구성에 ICMP 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="178c1-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="178c1-1755">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="178c1-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="178c1-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="178c1-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="178c1-1759">New-AzVirtualNetworkGatewayConnection에 대한 구성 가능한 매개 변수로 ConnectionProtocolType (Ikev1/Ikev2) 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="178c1-1760">LoadBalancerFrontendIpConfiguration에 PrivateIpAddressVersion 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="178c1-1761">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="178c1-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="178c1-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="178c1-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="178c1-1765">프로브에서 사용자 지정 포트를 지원하기 위한 Application Gateway New-AzApplicationGatewayProbeConfig 명령 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="178c1-1766">업데이트된 New-AzApplicationGatewayProbeConfig: 백 엔드 서버 검색에 사용되는 선택적 매개 변수 포트가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="178c1-1767">이 매개 변수는 Standard_V2 및 WAF_V2 SKU에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-1769">저장된 검색의 기본 버전이 1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="178c1-1770">사용자 지정 로그 null regex 처리가 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1772">'Get-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="178c1-1773">'Get-AzRecoveryServicesBackupContainer.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="178c1-1774">'Get-AzRecoveryServicesVault.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="178c1-1775">'Wait-AzRecoveryServicesBackupJob.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="178c1-1776">'Set-AzRecoveryServicesVaultContext.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="178c1-1777">'Get-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="178c1-1778">'Get-AzRecoveryServicesBackupRecoveryPoint.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="178c1-1779">'Restore-AzRecoveryServicesBackupItem.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="178c1-1780">Azure 파일 공유용 컨테이너를 등록 취소하기 위해 서비스 요청 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="178c1-1781">'Set-AzRecoveryServicesAsrAlertSetting.md' 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1782">Az.Resources</span></span>
- <span data-ttu-id="178c1-1783">'New-AzResourceGroupDeployment' 설명서에서 참조된 누락 cmdlet 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="178c1-1784">새 API 버전 2019-01-01을 사용하도록 정책 cmdlet 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="178c1-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="178c1-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="178c1-1786">SAS 토큰을 생성하기 위해 추가된 새로운 cmmdlet 추가: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="178c1-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="178c1-1787">'관리'만 지정된 경우 authorizationrules 권한에 대한 확인 및 오류 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1788">Az.Sql</span></span>
* <span data-ttu-id="178c1-1789">Set-AzSqlDatabaseSecondary cmdlet에 대한 누락된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="178c1-1790">이메일 주소를 제공하지 않고 설정된 취약성 평가 반복 검색 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="178c1-1791">경고 메시지의 작은 오타를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1792">Az.Storage</span></span>
* <span data-ttu-id="178c1-1793">'Get-AzStorageAccount'에 대한 참조 설명서의 예제를 업데이트하여 올바른 매개 변수 이름 사용</span><span class="sxs-lookup"><span data-stu-id="178c1-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="178c1-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="178c1-1794">Az.StorageSync</span></span>
* <span data-ttu-id="178c1-1795">Invoke-AzStorageSyncChangeDetection cmdlet을 추가하는 중입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="178c1-1796">TierFilesOlderThanDays를 기념하는 문제 9551 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-1797">Az.Websites</span></span>
* <span data-ttu-id="178c1-1798">Get-AzWebApp 및 Set-AzWebApp에서 일부 SiteConfig 속성을 반환하지 않은 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="178c1-1799">Get-AzDeletedWebApp 및 Restore-AzDeletedWebApp에 새 위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="178c1-1800">AzWebApp-IncludeSourceWebAppSlots을 사용하여 웹앱 슬롯을 복제하는 버그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="178c1-1801">2.4.0 - 2019년 7월</span><span class="sxs-lookup"><span data-stu-id="178c1-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1802">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1803">프로필 cmdlet에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="178c1-1804">생성된 cmdlet에서 환경 및 데이터 평면에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="178c1-1805">Windows PowerShell의 데이터 평면 cmdlet에대해 일부 경우 잘못된 엔드포인트가 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="178c1-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="178c1-1806">Az.Advisor</span></span>
* <span data-ttu-id="178c1-1807">Az.Advisor의 GA 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="178c1-1808">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="178c1-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-1810">문제 https://github.com/Azure/azure-powershell/issues/8671 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="178c1-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="178c1-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="178c1-1812">사용자 및 제품별 구독을 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="178c1-1813">범위 '/', '/ api, '/ api/echo api'를 사용하여 쿼리하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="178c1-1814">[https://github.com/Azure/azure-powershell/issues/9307](https://github.com/Azure/azure-powershell/issues/9307 ) 및 https://github.com/Azure/azure-powershell/issues/8432 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="178c1-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="178c1-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="178c1-1816">Apis를 가져올 때 'ApiVersion' 및 'ApiVersionSetId'를 지정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-1817">Az.Automation</span></span>
* <span data-ttu-id="178c1-1818">문자열 값을 처리하기 위해 Set-AzAutomationConnectionFieldValue cmdlet 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1819">Az.Compute</span></span>
* <span data-ttu-id="178c1-1820">New-AzImageConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-1821">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-1822">get activity runs, get pipeline runs, get trigger runs ADF cmdlet의 출력을 업데이트하여 Select-Object pipe를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="178c1-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="178c1-1823">Az.EventGrid</span></span>
* <span data-ttu-id="178c1-1824">'New-AzEventGridSubcription' 설명서의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1825">Az.IotHub</span></span>
* <span data-ttu-id="178c1-1826">권한 부여 정책 키를 다시 생성하기 위한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1827">Az.Network</span></span>
* <span data-ttu-id="178c1-1828">'RoutingPreference'를 공용 IP 태그에 추가함</span><span class="sxs-lookup"><span data-stu-id="178c1-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="178c1-1829">'Get-AzNetworkServiceTag' 참조 설명서의 예제 개선</span><span class="sxs-lookup"><span data-stu-id="178c1-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-1831">Get-AzPolicyState의 null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="178c1-1832">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/9446 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-1834">Get-AzOperationalInsightsDataSource에 반환된 CustomLog datasource 모델 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-1836">IaaSVMs에 대한 get-policy 명령 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1837">Az.Resources</span></span>
    - <span data-ttu-id="178c1-1838">Get-AzPolicyState -Top 매개 변수에 대한 도움말 텍스트 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="178c1-1839">Get-AzPolicyAlias에 대한 클라이언트 쪽 페이징 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="178c1-1840">Set-AzPolicyAssignment, -PolicyParameters 및 -PolicyParametersObject에 대한 새 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="178c1-1841">Policy cmdlet에 대한 몇 가지 문서 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="178c1-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="178c1-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="178c1-1843">문제 #4938 수정 - MaxSizeInMegabytes를 설정할 때 New-AzureRmServiceBusQueue가 BadRequest 반환</span><span class="sxs-lookup"><span data-stu-id="178c1-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1844">Az.Sql</span></span>
* <span data-ttu-id="178c1-1845">미리 보기 릴리스에서 공개 릴리스로 인스턴스 장애 조치(Failover) 그룹 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="178c1-1846">새 cmdlet으로 Azure SQL Server\Database Auditing을 지원하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="178c1-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="178c1-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="178c1-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="178c1-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="178c1-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="178c1-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="178c1-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="178c1-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="178c1-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="178c1-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="178c1-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="178c1-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="178c1-1853">취약성 평가 설정에서 이메일 제약 조건 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1854">Az.Storage</span></span>
* <span data-ttu-id="178c1-1855">다음 cmdlet에서 2개의 매개 변수 '-IndexDocument' 및 '-ErrorDocument404Path'를 필수에서 선택으로 변경하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="178c1-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="178c1-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="178c1-1857">예제를 추가하여 Get-AzStorageBlobContent의 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="178c1-1858">StorageException으로 cmdlet이 실패한 경우 자세한 오류 정보 표시</span><span class="sxs-lookup"><span data-stu-id="178c1-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="178c1-1859">Azure Files AAD DS 인증으로 스토리지 계정 생성 또는 업데이트 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="178c1-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="178c1-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="178c1-1862">파일 공유, 파일 디렉터리 또는 파일의 목록 지원 또는 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="178c1-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="178c1-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="178c1-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="178c1-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="178c1-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="178c1-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="178c1-1865">Az.StorageSync</span></span>
* <span data-ttu-id="178c1-1866">이 모듈은 이제 롤업 `Az` 모듈의 일부로 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="178c1-1867">2.3.2 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="178c1-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-1868">Az.Accounts</span></span>
* <span data-ttu-id="178c1-1869">함수 호출에 대해 일부 경우 잘못된 URL이 사용되는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="178c1-1870">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8983 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="178c1-1871">AzureRM에서 Az cmdlet으로의 별칭 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="178c1-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="178c1-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="178c1-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="178c1-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1874">Az.Compute</span></span>
* <span data-ttu-id="178c1-1875">New-AzVm 및 New-AzVmss 단순 매개 변수 집합은 이제 'ProximityPlacementGroup'매개 변수를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="178c1-1876">'New-AzVM' 참조 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="178c1-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="178c1-1877">Az.Dns</span></span>
* <span data-ttu-id="178c1-1878">'Set-AzDnsZone' 도움말 예제의 오타가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="178c1-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="178c1-1879">Az.EventGrid</span></span>
* <span data-ttu-id="178c1-1880">2019-06-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="178c1-1881">새 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-1881">New cmdlets:</span></span>
    - <span data-ttu-id="178c1-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="178c1-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="178c1-1883">새 Azure Event Grid 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="178c1-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="178c1-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="178c1-1885">Event Grid 도메인의 세부 정보를 가져오거나 현재 Azure 구독의 모든 Event Grid 도메인 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="178c1-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="178c1-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="178c1-1887">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="178c1-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="178c1-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="178c1-1889">Azure Event Grid 도메인에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="178c1-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="178c1-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="178c1-1891">Event Grid 도메인 이벤트를 게시하는 데 사용되는 공유 액세스 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="178c1-1892">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="178c1-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="178c1-1893">새 Azure Event Grid 도메인 토픽을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="178c1-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="178c1-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="178c1-1895">Event Grid 도메인 토픽의 세부 사항을 가져오거나, 현재 Azure의 특정 Event Grid 도메인 아래의 모든 Event Grid 도메인 토픽 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="178c1-1896">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="178c1-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="178c1-1897">기존 Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="178c1-1898">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="178c1-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="178c1-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="178c1-1900">새로운 Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="178c1-1901">새로운 Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 새 이벤트 구독을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="178c1-1902">기존 매개 변수(예: EndPointType, SubjectBeginsWith 등)를 재사용할 수 있도록 도메인 및 도메인 토픽에 대한 새로운 매개 변수 집합을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="178c1-1903">지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="178c1-1904">이벤트 구독 만료 날짜,</span><span class="sxs-lookup"><span data-stu-id="178c1-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="178c1-1905">고급 필터링 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="178c1-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="178c1-1906">대상으로 servicebusqueue에 대한 새 열거형을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="178c1-1907">-IncludedEventType 옵션에서 'All' 사용을 허용하지 않고 다음으로 대체함</span><span class="sxs-lookup"><span data-stu-id="178c1-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="178c1-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="178c1-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="178c1-1909">결과 페이지 매김 및 필터링을 지원하는 새로운 선택적 매개 변수(Top, ODataQuery 및 NextLink)를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="178c1-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="178c1-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="178c1-1911">Event Grid 도메인 및 Event Grid 도메인 토픽에 대한 파이핑을 지원하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="178c1-1912">Event Grid 도메인 이름 및 Event Grid 도메인 토픽 이름을 지정하기 위해 새로운 필수 매개 변수를 추가하여 이러한 리소스 아래에 기존 이벤트 구독을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="178c1-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="178c1-1915">변환 지원 및 새 연산자 자동 완성 값(RegEx)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="178c1-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="178c1-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="178c1-1917">새 자동 완성 값 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1918">Az.Network</span></span>
* <span data-ttu-id="178c1-1919">Microsoft Azure Virtual Network 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="178c1-1920">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1920">New cmdlets</span></span>
        - <span data-ttu-id="178c1-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="178c1-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="178c1-1922">AvailablePrivateEndpointType 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="178c1-1923">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1923">New cmdlets</span></span>
        - <span data-ttu-id="178c1-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="178c1-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="178c1-1925">PrivatePrivateLinkService 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="178c1-1926">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1926">New cmdlets</span></span>
        - <span data-ttu-id="178c1-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="178c1-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="178c1-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="178c1-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="178c1-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="178c1-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="178c1-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="178c1-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="178c1-1932">PrivateEndpoint 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="178c1-1933">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-1933">New cmdlets</span></span>
        - <span data-ttu-id="178c1-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="178c1-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="178c1-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="178c1-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="178c1-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="178c1-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="178c1-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="178c1-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="178c1-1938">기능에 대한 새로운 명령이 업데이트됨: VpnConnection 상의 UseLocalAzureIpAddress 플래그</span><span class="sxs-lookup"><span data-stu-id="178c1-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="178c1-1939">New-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="178c1-1940">Set-AzVpnConnection이 업데이트됨: 선택적 매개 변수 -UseLocalAzureIpAddress를 추가하여 로컬 Azure IP 주소가 연결을 시작하는 동안 소스 주소로 사용되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="178c1-1941">ExpressRoute 피어링에 읽기 전용 필드 PeeredConnections가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="178c1-1942">ExpressRoute에 읽기 전용 필드 GlobalReachEnabled가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="178c1-1943">ExpressRouteCircuit 모델에서 AllowGlobalReach 필드의 사용 중단을 부르는 호환성이 손상되는 변경 속성이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="178c1-1944">AzApplicationGatewayRedirectConfiguration cmdlet에서 TargetListenerID를 사용하는 중의 8756 오류 문제가 해결됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="178c1-1945">다시 쓰기 규칙 세트가 설정되지 못하게 하는 New-AzApplicationGatewayPathRuleConfig의 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="178c1-1946">NetworkInterfaceIpConfiguration에 VirtualNetworkTaps가 표시되는 방식이 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="178c1-1947">모든 파트를 나열하도록 Cortex Get cmdlet이 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="178c1-1948">ExpressRouteGateways, VpnGateway에 대한 VirtualHub 참조 생성 수정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="178c1-1949">AzureFirewall 및 NatGateway의 가용성 영역에 대한 지원 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="178c1-1950">Get-AzNetworkServiceTag cmdlet 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="178c1-1951">Azure Firewall에 대한 여러 공용 IP 주소에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="178c1-1952">New-AzFirewall cmdlet이 업데이트됨:</span><span class="sxs-lookup"><span data-stu-id="178c1-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="178c1-1953">하나 이상의 공용 IP 주소 개체를 허용하는 매개 변수 -PublicIpAddress 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="178c1-1954">Virtual Network 개체를 허용하는 매개 변수 -VirtualNetwork 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="178c1-1955">방화벽 개체에 AddPublicIpAddress 및 RemovePublicIpAddress 메서드 추가됨 - 공용 IP 주소 개체를 입력으로 허용</span><span class="sxs-lookup"><span data-stu-id="178c1-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="178c1-1956">매개 변수 -PublicIpName 및 -VirtualNetworkName이 더 이상 사용되지 않음</span><span class="sxs-lookup"><span data-stu-id="178c1-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="178c1-1957">기능에 대한 새로운 명령이 업데이트됨: VpnClient AAD 인증 옵션을 가상 네트워크 게이트웨이 리소스로 설정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="178c1-1958">New-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="178c1-1959">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 설정할 수 있도록 선택적 매개 변수 AadTenantUri, AadAudienceId, AadIssuerUri가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="178c1-1960">Set-AzVirtualNetworkGateway가 업데이트됨: 게이트웨이에서 VpnClient AAD 인증 옵션을 제거할 수 있도록 선택적인 스위치 매개 변수 RemoveAadAuthentication이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-1962">'New-AzureRmOperationalInsightsWorkspace' 명령에서 **pergb2018** 가격 책정 계층 사용</span><span class="sxs-lookup"><span data-stu-id="178c1-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-1963">Az.Resources</span></span>
* <span data-ttu-id="178c1-1964">추가 템플릿 내보내기 옵션 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="178c1-1965">Export-AzResourceGroup에 '-SkipResourceNameParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="178c1-1966">Export-AzResourceGroup에 '-SkipAllParameterization' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="178c1-1967">내보낸 리소스 필터링을 위해 Export-AzResourceGroup에 '-Resource' 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-1969">일부 경우 잘못된 지문을 가져오는 추가 인증서 ByExistingKeyVault 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-1970">Az.Sql</span></span>
* <span data-ttu-id="178c1-1971">Advanced Threat Protection 스토리지 엔드포인트 접미사 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="178c1-1972">Advanced Data Security가 Advanced Threat Protection 정책을 재정의하는 것을 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="178c1-1973">고객이 TDE 키를 추가하고 관리되는 인스턴스에 TDE 보호기를 설정할 수 있도록 Management.Sql용 새 Cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="178c1-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="178c1-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="178c1-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="178c1-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="178c1-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="178c1-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="178c1-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="178c1-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="178c1-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="178c1-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-1979">Az.Storage</span></span>
* <span data-ttu-id="178c1-1980">스토리지 계정 생성 시 종류 FileStorage 및 SkuName Premium_ZRS 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="178c1-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="178c1-1982">BLOB immutability cmdlet의 설명 명확화</span><span class="sxs-lookup"><span data-stu-id="178c1-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="178c1-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-1984">Az.Websites</span></span>
* <span data-ttu-id="178c1-1985">Get-AzWebAppCertificate를 클라이언트 대신 서버의 리소스 그룹별로 필터링하도록 최적화</span><span class="sxs-lookup"><span data-stu-id="178c1-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="178c1-1986">Get-AzWebAppSnapshot에 -UseDisasterRecovery 스위치 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="178c1-1987">2.2.0 - 2019년 6월</span><span class="sxs-lookup"><span data-stu-id="178c1-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="178c1-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-1988">Az.Cdn</span></span>
* <span data-ttu-id="178c1-1989">cmdlet에서 2019-04-15 API 버전 기반의 rulesEngine 기능을 지원하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-1990">Az.Compute</span></span>
* <span data-ttu-id="178c1-1991">작업을 시작하여 완료되기 전에 즉시 반환하는 `NoWait` 매개 변수가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="178c1-1992">다음 Cmdlet이 업데이트 되었습니다.   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="178c1-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-1993">Az.EventHub</span></span>
* <span data-ttu-id="178c1-1994">#9231 수정 - Get-AzEventHubNamespace에서 태그를 반환하지 않음</span><span class="sxs-lookup"><span data-stu-id="178c1-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="178c1-1995">#9230 수정 - Get-AzEventHubNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환함</span><span class="sxs-lookup"><span data-stu-id="178c1-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-1996">Az.Network</span></span>
* <span data-ttu-id="178c1-1997">Nat Gateway에 대한 ResourceId 및 InputObject 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="178c1-1998">ResourceId 및 InputObject에 대한 별칭 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-2000">Get-AzPolicyEvent에서 Null 참조 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-2002">IaaSVM 정책 최소 보존 기간(일)이 1에서 7로 변경됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="178c1-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="178c1-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="178c1-2004">#9182 문제 해결 - Get-AzServiceBusNamespace에서 ResourceGroupName 대신 ResourceGroup을 반환</span><span class="sxs-lookup"><span data-stu-id="178c1-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-2006">'Update-AzServiceFabricReliability' 오류 메시지의 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="178c1-2007">Service Fabric 명령줄에서 누락된 문자 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2008">Az.Sql</span></span>
* <span data-ttu-id="178c1-2009">Managed Instance에 대한 AutoDr을 지원하기 위해 New-AzureSqlInstance cmdlet에 대한 DnsZonePartner 매개 변수를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="178c1-2010">Get-AzSqlDatabaseSecureConnectionPolicy cmdlet 사용 중단</span><span class="sxs-lookup"><span data-stu-id="178c1-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="178c1-2011">Threat Detection(위협 탐지) cmdlet 이름을 Advanced Threat Protection으로 변경함</span><span class="sxs-lookup"><span data-stu-id="178c1-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="178c1-2012">새 AzSqlInstance -StorageSizeInGB 및 -LicenseType 매개 변수는 이제 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2013">Az.Websites</span></span>
* <span data-ttu-id="178c1-2014">-WebApp 속성에서 Set-AzWebApp 및 Set-AzWebAppSlot을 사용하면 태그가 제거되는 문제를 해결함</span><span class="sxs-lookup"><span data-stu-id="178c1-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="178c1-2015">2.1.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="178c1-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="178c1-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-2017">글로벌 및 API 범위에서 진단을 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="178c1-2018">**Get-AzApiManagementDiagnostic** - 글로벌 또는 API 범위가 구성된 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="178c1-2019">**New-AzApiManagementDiagnostic** - 글로벌 범위 또는 API 범위에서 새 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="178c1-2020">**New-AzApiManagementHttpMessageDiagnostic** - 기록할 Headers(헤더) 및 Body Bytes(본문 바이트 수) 크기에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="178c1-2021">**New-AzApiManagementPipelineDiagnosticSetting** - 게이트웨이로 들어오고 나가는 HTTP 메시지에 대한 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="178c1-2022">**New-AzApiManagementSamplingSetting** - 진단 요청/응답에 대한 샘플링 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="178c1-2023">**Remove-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="178c1-2024">**Set-AzApiManagementDiagnostic** - 글로벌 또는 API 범위에서 진단 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="178c1-2025">ApiManagement 서비스에서 캐시를 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="178c1-2026">**Get-AzApiManagementCache** - 식별자 또는 모든 캐시로 지정된 캐시의 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="178c1-2027">**New-AzApiManagementCache** - 특정 Azure 'region'(지역)에 새 'default'(기본) 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="178c1-2028">**Remove-AzApiManagementCache** - 캐시 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="178c1-2029">**Update-AzApiManagementCache** - 캐시 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="178c1-2030">API 스키마 관리하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="178c1-2031">**New-AzApiManagementSchema** - API에 대한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="178c1-2032">**Get-AzApiManagementSchema** - API에 구성된 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="178c1-2033">**Remove-AzApiManagementSchema** - API에 구성된 스키마 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="178c1-2034">**Set-AzApiManagementSchema** - API에 구성된 스키마 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="178c1-2035">사용자 토큰을 생성하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="178c1-2036">**New-AzApiManagementUserToken** - 기본적으로 8시간 동안 유효한 새 사용자 토큰을 생성합니다. 'GIT' 사용자에 대한 토큰은 이 cmdlet을 사용하여 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="178c1-2037">네트워크 상태를 검색하기 위한 새 cmdlet을 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="178c1-2038">**Get-AzApiManagementNetworkStatus** - API Management 서비스에서 사용하는 리소스의 네트워크 상태 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="178c1-2039">ApiManagement 서비스를 가상 네트워크에 배포하고 종속성이 손상되었는지 여부를 확인할 때 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="178c1-2040">**New-AzApiManagement** cmdlet에서 ApiManagement 서비스를 관리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="178c1-2041">새 '소비' SKU 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="178c1-2042">'소비' SKU에 대해 'EnableClientCertificate' 플래그를 설정하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="178c1-2043">새 **New-AzApiManagementSslSetting** cmdlet을 사용하면 'Backend(백 엔드)' 및 'Frontend'(프런트 엔드)에서 'TLS/SSL' 설정을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="178c1-2044">또한 ApiManagement 서비스의 'Frontend'에서 '3DES'와 같은 'Ciphers'와 'Http2'와 같은 'ServerProtocols'를 구성하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="178c1-2045">ApiManagement 서비스에서 'DeveloperPortal' 호스트 이름을 구성하기 위한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="178c1-2046">**Get-AzApiManagementSsoToken** cmdlet에서 'PsApiManagement' 개체를 입력으로 사용하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="178c1-2047">cmdlet에서 오류 메시지를 인라인으로 표시하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="178c1-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : 오류 코드: ValidationError 오류 메시지: 하나 이상의 필드에 잘못된 값이 있습니다. 오류 세부 정보:    [Code=ValidationError, Message=줄 3, 열 10의 'log-to-eventhub' 요소에 오류가 있습니다.: 로거를 찾지 못함, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="178c1-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="178c1-2049">**Export-AzApiManagementApi** cmdlet에서 API를 'OpenApi 3.0' 형식으로 내보내도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="178c1-2050">**Import-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="178c1-2051">'OpenApi 3.0' 문서 사양에서 API 가져오기</span><span class="sxs-lookup"><span data-stu-id="178c1-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="178c1-2052">문서('Swagger', 'Wadl', 'Wsdl', 'OpenApi')에 지정된 'PsApiManagementSchema' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="178c1-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="178c1-2053">문서에 지정된 'ServiceUrl' 속성 재정의</span><span class="sxs-lookup"><span data-stu-id="178c1-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="178c1-2054">**Get-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'(형식)의 정책을 반환하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="178c1-2055">**Set-AzApiManagementPolicy** cmdlet에서 'rawxml'을 사용하여 이스케이프된 비 Xml 'format'의 정책을 수락하고, 'xml'을 사용하여 이스케이프된 Xml 'format'의 정책을 수락하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="178c1-2056">**New-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="178c1-2057">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="178c1-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="178c1-2058">'ApiVersionSet'에서 API 만들기</span><span class="sxs-lookup"><span data-stu-id="178c1-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="178c1-2059">'SourceApiId' 및 'SourceApiRevision'을 사용하여 API 복제</span><span class="sxs-lookup"><span data-stu-id="178c1-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="178c1-2060">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="178c1-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="178c1-2061">**Set-AzApiManagementApi** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="178c1-2062">'OpenId' 권한 부여 서버를 사용하여 API 구성</span><span class="sxs-lookup"><span data-stu-id="178c1-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="178c1-2063">API를 'ApiVersionSet'으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="178c1-2064">API 범위에서 'SubscriptionRequired' 구성 가능</span><span class="sxs-lookup"><span data-stu-id="178c1-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="178c1-2065">**New-AzApiManagementRevision** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="178c1-2066">'SourceApiRevision'을 사용하여 기존 수정 버전 복제(태그, 제품, 작업 및 정책 복사).</span><span class="sxs-lookup"><span data-stu-id="178c1-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="178c1-2067">새 수정 버전은 부모의 'ApiId'를 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="178c1-2068">'ApiRevisionDescription' 제공</span><span class="sxs-lookup"><span data-stu-id="178c1-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="178c1-2069">API 복제 시 'ServiceUrl' 재정의</span><span class="sxs-lookup"><span data-stu-id="178c1-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="178c1-2070">**New-AzApiManagementIdentityProvider** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="178c1-2071">'Authority'를 사용하여 'AAD' 또는 'AADB2C' 구성</span><span class="sxs-lookup"><span data-stu-id="178c1-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="178c1-2072">'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' 및 'PasswordResetPolicy' 설정</span><span class="sxs-lookup"><span data-stu-id="178c1-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="178c1-2073">**New-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="178c1-2074">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="178c1-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="178c1-2075">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="178c1-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="178c1-2076">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="178c1-2077">**Set-AzApiManagementSubscription** cmdlet을 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="178c1-2078">'Scope' 및 'UserId'를 사용하여 새 SubscriptonModel 설명</span><span class="sxs-lookup"><span data-stu-id="178c1-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="178c1-2079">'ProductId' 및 'UserId'를 사용하여 이전 구독 모델 설명</span><span class="sxs-lookup"><span data-stu-id="178c1-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="178c1-2080">구독 수준에서 'AllowTracing'을 사용하도록 설정하는 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="178c1-2081">다음 cmdlet에서 'ResourceId'를 입력으로 수락하도록 업데이트했습니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="178c1-2082">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="178c1-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="178c1-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="178c1-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="178c1-2084">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="178c1-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="178c1-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="178c1-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="178c1-2086">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="178c1-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="178c1-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="178c1-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="178c1-2088">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="178c1-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="178c1-2089">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="178c1-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="178c1-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="178c1-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="178c1-2091">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="178c1-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="178c1-2092">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="178c1-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="178c1-2093">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="178c1-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2094">Az.Automation</span></span>
* <span data-ttu-id="178c1-2095">Get-AzAutomationJobOutputRecord에서 JSON 및 Text 레코드 값을 처리하도록 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="178c1-2096">문제 https://github.com/Azure/azure-powershell/issues/7977 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="178c1-2097">문제 https://github.com/Azure/azure-powershell/issues/8600 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="178c1-2098">Start-AzAutomationDscCompilationJob에서 완료될 때까지 기다리지 않고 작업을 바로 시작하도록 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="178c1-2099">문제 https://github.com/Azure/azure-powershell/issues/8347 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="178c1-2100">-Name을 사용하면 모든 노드를 반환하는 Get-AzAutomationDscNode 수정.</span><span class="sxs-lookup"><span data-stu-id="178c1-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="178c1-2101">이제 일치하는 노드만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2102">Az.Compute</span></span>
* <span data-ttu-id="178c1-2103">ProtectFromScaleIn 및 ProtectFromScaleSetAction 매개 변수를 Update-AzVmssVM cmdlet에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="178c1-2104">'East US'(미국 동부)가 지원되지 않는 경우 이제 New-AzVM wimple 매개 변수 집합에서 기본적으로 사용 가능한 위치를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2106">ADLS SDK에서 httpclient를 사용하도록 업데이트하고, 데이터 평면 테스트를 Azure 프레임워크와 통합합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-2107">Az.Monitor</span></span>
* <span data-ttu-id="178c1-2108">도움말 예제에서 잘못된 매개 변수 이름을 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2109">Az.Network</span></span>
* <span data-ttu-id="178c1-2110">DisableBgpRoutePropagation 플래그를 유효 경로 테이블 출력에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="178c1-2111">업데이트된 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="178c1-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="178c1-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="178c1-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="178c1-2113">New-AzApplicationGatewayTrustedRootCertificate 설명서에서 이중 파선을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2114">Az.Resources</span></span>
* <span data-ttu-id="178c1-2115">할당 거부를 검색하기 위한 새 Get-AzureRmDenyAssignment cmdlet을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2116">Az.Sql</span></span>
* <span data-ttu-id="178c1-2117">Advanced Threat Protection cmdlet의 이름을 Advanced Data Security로 변경하고, 취약성 평가를 기본적으로 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="178c1-2118">2.0.0 - 2019년 5월</span><span class="sxs-lookup"><span data-stu-id="178c1-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2119">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2120">사용자 이름/비밀번호 인증을 사용하여 ADFS 문제를 해결하도록 인증 라이브러리 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-2122">Bing Search 서비스에 대해서만 Bing 면책 조항을 표시하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="178c1-2123">계정 생성 실패 시 오류 개선.</span><span class="sxs-lookup"><span data-stu-id="178c1-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2124">Az.Compute</span></span>
* <span data-ttu-id="178c1-2125">근접 배치 그룹 기능</span><span class="sxs-lookup"><span data-stu-id="178c1-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="178c1-2126">다음과 같은 새 cmdlet을 추가했습니다.   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="178c1-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="178c1-2127">새 매개 변수 ProximityPlacementGroupId가 다음 cmdlet에 추가됩니다.   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="178c1-2128">New-AzGalleryImageVersion에 StorageAccountType 매개 변수가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="178c1-2129">New-AzGalleryImageVersion의 TargetRegion이 StorageAccountType를 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="178c1-2130">SkipShutdown 스위치 매개 변수가 Stop-AzVM 및 Stop-AzVmss에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="178c1-2131">주요 변경 내용</span><span class="sxs-lookup"><span data-stu-id="178c1-2131">Breaking changes</span></span>
    - <span data-ttu-id="178c1-2132">Set-AzVMBootDiagnostics이 Set-AzVMBootDiagnostic으로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="178c1-2133">Export-AzLogAnalyticThrottledRequests이 Export-AzLogAnalyticThrottledRequests로 변경되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="178c1-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="178c1-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="178c1-2135">Azure 배포 관리자 cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="178c1-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="178c1-2136">Az.Dns</span></span>
* <span data-ttu-id="178c1-2137">자동 DNS 이름 서버 위임</span><span class="sxs-lookup"><span data-stu-id="178c1-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="178c1-2138">DNS 영역 만들기 cmdlet은 추가 선택적 매개 변수로 부모 영역 이름을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="178c1-2139">새로 생성 된 자식 영역의 부모 영역에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="178c1-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="178c1-2141">Azure FrontDoor cmdlet의 일반적으로 사용 가능한 첫 번째 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="178c1-2142">'Waf'를 포함하도록 WAF cmdlet의 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="178c1-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="178c1-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-2143">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-2144">두 개의 cmdlet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="178c1-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="178c1-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="178c1-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="178c1-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="178c1-2147">Grant-AzHDInsightHttpServicesAccess를 대체할 새 cmdlet Set-AzHDInsightGatewayCredential을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="178c1-2148">reader 역할과 HDInsight 운영자 역할을 구분하도록 cmdlet Get-AzHDInsightJobOutput 업데이트:</span><span class="sxs-lookup"><span data-stu-id="178c1-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="178c1-2149">reader 역할을 가진 사용자는 'DefaultStorageAccountKey'매개 변수를 명시적으로 지정해야 합니다. 그렇지 않으면 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="178c1-2150">Hdinsight 운영자 역할을 가진 사용자를 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-2151">Az.Monitor</span></span>
* <span data-ttu-id="178c1-2152">SQR API(예약 쿼리 규칙)용 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="178c1-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="178c1-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="178c1-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="178c1-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="178c1-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="178c1-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="178c1-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="178c1-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="178c1-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="178c1-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="178c1-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="178c1-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="178c1-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="178c1-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="178c1-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="178c1-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="178c1-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="178c1-2164">SQR API에 대한 [자세한 내용](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules)</span><span class="sxs-lookup"><span data-stu-id="178c1-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="178c1-2165">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 cmdlet을 포함하도록 Az.Monitor.md가 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2166">Az.Network</span></span>
* <span data-ttu-id="178c1-2167">Nat 게이트웨이 리소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="178c1-2168">새로운 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2168">New cmdlets</span></span>
        - <span data-ttu-id="178c1-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="178c1-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="178c1-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="178c1-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="178c1-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="178c1-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="178c1-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="178c1-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="178c1-2173">다음 Cmdlet이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="178c1-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="178c1-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="178c1-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="178c1-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="178c1-2176">기능에 대한 새로운 명령이 업데이트됨: Brooklyn Gateway에서 사용자 지정 경로 설정/제거.</span><span class="sxs-lookup"><span data-stu-id="178c1-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="178c1-2177">New-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="178c1-2178">Set-AzVirtualNetworkGateway가 업데이트됨: 선택적 매개 변수 -CustomRoute를 추가하여 게이트웨이에서 설정할 사용자 지정 경로로 주소 접두사를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-2180">정책 평가 세부 정보 쿼리 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="178c1-2181">Get-AzPolicyState에 '-Expand'매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="178c1-2182">'-Expand PolicyEvaluationDetails' 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-2184">크로스 구독 Azure에서 Azure 사이트 복구 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="178c1-2185">Azure Site Recovery에 대한 호환성이 손상되는 변경 표시</span><span class="sxs-lookup"><span data-stu-id="178c1-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="178c1-2186">Azure Site Recovery 복구 계획 최종 실행 계획에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="178c1-2187">Azure에서 Azure에 대한 Azure Site Recovery 업데이트 네트워크 매핑 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="178c1-2188">관리 디스크에 대한 Azure에서 Azure에 대한 Azure Site Recovery 업데이트 보호 방향 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="178c1-2189">기타 사소한 수정.</span><span class="sxs-lookup"><span data-stu-id="178c1-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="178c1-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="178c1-2190">Az.Relay</span></span>
* <span data-ttu-id="178c1-2191">고객 관련 메시지의 철자 오류 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="178c1-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="178c1-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="178c1-2193">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2194">Az.Storage</span></span>
* <span data-ttu-id="178c1-2195">저장소 클라이언트 라이브러리 10.0.1로 업그레이드(이 SDK의 모든 개체의 네임스페이스가 'Microsoft.WindowsAzure.Storage. *'에서 'Microsoft.Azure.Storage.* '로 변경됨)</span><span class="sxs-lookup"><span data-stu-id="178c1-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="178c1-2196">새로운 API 버전 2019-04-01을 지원하기 위해 Microsoft.Azure.Management.Storage 11.0.0으로 업그레이드합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="178c1-2197">스토리지 생성 계정의 기본 스토리지 계정 종류가 'Storage'에서 'StorageV2'로 변경됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="178c1-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="178c1-2199">'StandardLRS'가 'Standard_LRS'로 변경되는 것과 같이 '-'을 추가하여 입력 SkuName과 정렬되도록 스토리지 계정 cmdlet 출력 Sku.Name을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="178c1-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="178c1-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="178c1-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="178c1-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2203">Az.Websites</span></span>
* <span data-ttu-id="178c1-2204">Get-AzWebApp에서 반환한 PSSite 개체에 대해 'Kind'속성이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="178c1-2205">Get-AzWebApp\* 메트릭 및 Get-AzAppServicePlanMetrics가 사용되지 않음으로 표시되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="178c1-2206">1.8.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="178c1-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="178c1-2207">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="178c1-2208">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="178c1-2209">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="178c1-2210">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="178c1-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="178c1-2211">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="178c1-2212">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="178c1-2213">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="178c1-2214">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2215">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2216">Mac에서 모듈을 올바르게 삭제하기 위해 Uninstall-AzureRm을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="178c1-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-2217">Az.Batch</span></span>
* <span data-ttu-id="178c1-2218">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-2219">Az.Cdn</span></span>
* <span data-ttu-id="178c1-2220">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-2222">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2223">Az.Compute</span></span>
* <span data-ttu-id="178c1-2224">디스크의 리소스 ID에 리소스 ID의 소문자 resourcegroups가 있는 경우 AEM 설치 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="178c1-2225">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="178c1-2226">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-2227">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-2228">NodeCount가 관리형 통합 런타임에 대해 Null이 아닌 경우 SsisProperties를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2230">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="178c1-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="178c1-2231">Az.EventGrid</span></span>
* <span data-ttu-id="178c1-2232">이벤트 구독 cmdlet 만들기/업데이트를 사용하기 전에 리소스를 만들어야 함을 나타내기 위해 엔드포인트의 도움말 텍스트가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-2233">Az.EventHub</span></span>
* <span data-ttu-id="178c1-2234">네임스페이스의 NetworkRuleSet에 대한 새 cmdlet가 추가되었습니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="178c1-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="178c1-2235">Az.HDInsight</span></span>
* <span data-ttu-id="178c1-2236">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-2237">Az.IotHub</span></span>
* <span data-ttu-id="178c1-2238">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-2239">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-2240">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="178c1-2241">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="178c1-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="178c1-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="178c1-2243">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="178c1-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="178c1-2244">Az.Media</span></span>
* <span data-ttu-id="178c1-2245">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-2246">Az.Monitor</span></span>
  * <span data-ttu-id="178c1-2247">GenV2(비 클래식) 메트릭 기반 경고 규칙에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="178c1-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="178c1-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="178c1-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="178c1-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="178c1-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="178c1-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="178c1-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="178c1-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="178c1-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="178c1-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="178c1-2253">모니터 SDK가 버전 0.22.0-preview로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2254">Az.Network</span></span>
* <span data-ttu-id="178c1-2255">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="178c1-2256">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="178c1-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="178c1-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="178c1-2258">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-2260">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="178c1-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="178c1-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="178c1-2262">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-2264">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="178c1-2265">Azure VM의 SQL용 테이블 형식이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="178c1-2266">AzureFileShare에서 위치를 가져오는 대체 메서드가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="178c1-2267">시간대에 따라 SchedulePolicy 개체의 ScheduleRunDays가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="178c1-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="178c1-2268">Az.RedisCache</span></span>
* <span data-ttu-id="178c1-2269">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2270">Az.Resources</span></span>
* <span data-ttu-id="178c1-2271">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2272">Az.Sql</span></span>
* <span data-ttu-id="178c1-2273">Monitor SDK의 종속성을 공용 코드로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="178c1-2274">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="178c1-2275">다중 열 분류 프로세스가 향상되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="178c1-2276">기본적으로 Get-AzSqlServerServiceObjective의 응답으로 SKU 속성(SKU 이름, 제품군, 용량)과 테이블 형식을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="178c1-2277">해당 지역에 기존 서버 없이 위치별로 Get-AzSqlServerServiceObjective를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="178c1-2278">관리형 인스턴스 생성 시 표준 시간대 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="178c1-2279">와일드 카드에 대한 설명서 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2280">Az.Websites</span></span>
* <span data-ttu-id="178c1-2281">실행 시 태그를 제거하지 않도록 Set-AzWebApp 및 Set-AzWebAppSlot를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="178c1-2282">복수 명사의 cmdlet가 단수로 업데이트되었고, 복수 이름이 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="178c1-2283">WebSites SDK가 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="178c1-2284">PSAppServicePlan에서 AdminSiteName 속성을 제거했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="178c1-2285">1.7.0 - 2019년 4월</span><span class="sxs-lookup"><span data-stu-id="178c1-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="178c1-2286">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="178c1-2287">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="178c1-2288">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="178c1-2289">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="178c1-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="178c1-2290">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="178c1-2291">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="178c1-2292">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="178c1-2293">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="178c1-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2294">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2295">매개 변수 AzureAnalysisServicesEndpointResourceId를 허용하도록 Add-AzEnvironment 및 Set-AzEnvironment 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="178c1-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="178c1-2297">데이터 평면 cmdlet에서 ServiceClient 사용 및 원본 인증 논리 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="178c1-2298">호환성이 손상되는 변경을 방지하기 위해 Add-AzureASAccount를 Connect-AzAccount의 래퍼로 만듦</span><span class="sxs-lookup"><span data-stu-id="178c1-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2299">Az.Automation</span></span>
* <span data-ttu-id="178c1-2300">포함에 대한 New-AzAutomationSoftwareUpdateConfiguration cmdlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="178c1-2301">이제 매개 변수 IncludedKbNumber 및 IncludedPackageNameMask가 작동함</span><span class="sxs-lookup"><span data-stu-id="178c1-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="178c1-2302">Azure 자동화 업데이트 관리 동적 그룹에 대한 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2303">Az.Compute</span></span>
* <span data-ttu-id="178c1-2304">New-AzDiskConfig 및 New-AzSnapshotConfig에 HyperVGeneration 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="178c1-2305">다른 테넌트의 갤러리 이미지를 사용하여 VM을 만들 수 있음</span><span class="sxs-lookup"><span data-stu-id="178c1-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="178c1-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="178c1-2307">후행 빈 인수를 추가한 New-AzContainerGroup의 -Command 매개 변수의 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-2308">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-2309">ADF .Net SDK 버전을 3.0.2로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="178c1-2310">RepoConfiguration 관련 설정에 대한 추가 매개 변수로 Set-AzDataFactoryV2 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2311">Az.Resources</span></span>
* <span data-ttu-id="178c1-2312">'-ResourceId' 또는 '-ResourceGroupName', '-Name' 및 '-ResourceType' 매개 변수를 제공할 때 'Get-AzResource'에 대한 공급자 처리 개선</span><span class="sxs-lookup"><span data-stu-id="178c1-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="178c1-2313">'Test-AzDeployment' 및 'Test-AzResourceGroupDeployment'에 대한 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="178c1-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="178c1-2314">배포 유효성 검사 외부에서 발생한 오류를 처리하고 그 대신 명령의 출력에 포함</span><span class="sxs-lookup"><span data-stu-id="178c1-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="178c1-2315">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="178c1-2316">배포 cmdlet 세트에 스크립트 및 작업 시나리오에서 프롬프트를 건너뛰는 '-IgnoreDynamicParameters' 스위치 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="178c1-2317">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/6856 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2318">Az.Sql</span></span>
* <span data-ttu-id="178c1-2319">데이터베이스 데이터 분류 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2320">Az.Storage</span></span>
* <span data-ttu-id="178c1-2321">매개 변수 -UseConnectedAccount를 사용하여 스토리지 컨텍스트를 만들 때 자세한 오류 보고(단, 로그인 Azure 계정 없이)</span><span class="sxs-lookup"><span data-stu-id="178c1-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="178c1-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="178c1-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="178c1-2323">관리 평면 API를 사용하여 지정한 스토리지 계정의 BLOB 서비스 속성 관리 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="178c1-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="178c1-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="178c1-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="178c1-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="178c1-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="178c1-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="178c1-2328">BLOB 및 파일 업로드/다운로드 cmdlet에 대한 -AsJob 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="178c1-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="178c1-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="178c1-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="178c1-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="178c1-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="178c1-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="178c1-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="178c1-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="178c1-2333">1.6.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="178c1-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="178c1-2334">마지막 주 릴리스 이후의 주요 사항</span><span class="sxs-lookup"><span data-stu-id="178c1-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="178c1-2335">`Az` 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="178c1-2336">`Az` 모듈에 대한 자세한 내용은 https://aka.ms/azps-announce 를 방문하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="178c1-2337">Location, ResourceGroup 및 ResourceName 완성자가 추가되었습니다(https://azure.microsoft.com/blog/completers-in-azure-powershell/ ).</span><span class="sxs-lookup"><span data-stu-id="178c1-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="178c1-2338">와일드카드 지원이 Az.Compute 및 Az.Network에 대한 Get cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="178c1-2339">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="178c1-2340">Python 2 Runbook 지원이 Az.Automation에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="178c1-2341">Az.LogicApp: 통합 계정 어셈블리 및 일괄 처리 구성을 위한 새로운 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2342">Az.Automation</span></span>
* <span data-ttu-id="178c1-2343">Azure 자동화 업데이트 관리에서 변경된 지원 기능은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="178c1-2344">동적 그룹화</span><span class="sxs-lookup"><span data-stu-id="178c1-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="178c1-2345">사전 스크립트</span><span class="sxs-lookup"><span data-stu-id="178c1-2345">Pre-Post script</span></span>
    * <span data-ttu-id="178c1-2346">다시 부팅 설정</span><span class="sxs-lookup"><span data-stu-id="178c1-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2347">Az.Compute</span></span>
* <span data-ttu-id="178c1-2348">Get-AzVmBootDiagnosticsData의 경로 확인 문제가 해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="178c1-2349">Compute 클라이언트 라이브러리가 25.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-2350">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-2351">와일드카드 지원이 KeyVault cmdlet에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2352">Az.Network</span></span>
* <span data-ttu-id="178c1-2353">Azure Firewall에 대한 위협 인텔리전스 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="178c1-2354">Application Gateway 방화벽 정책의 최상위 수준 리소스 및 사용자 지정 규칙이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-2356">인스턴트 RP를 지원하기 위해 SnapshotRetentionInDays가 Azure VM 정책에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="178c1-2357">컨테이너 등록을 취소하는 파이프 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2358">Az.Resources</span></span>
* <span data-ttu-id="178c1-2359">Get-AzResource 및 Get-AzResourceGroup에 대한 와일드카드 지원을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="178c1-2360">ARM에 대한 일반 호출을 수행할 때 사용되는 자격 증명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2361">Az.Sql</span></span>
* <span data-ttu-id="178c1-2362">위협 탐지의 cmdlet 매개 변수(ExcludeDetectionType)가 DetectionType에서 string[]으로 변경되어 새 DetectionType이 추가되면 이후의 증명이 되고 자동 완성도 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2363">Az.Storage</span></span>
* <span data-ttu-id="178c1-2364">스토리지 계정에 대한 관리 정책 가져오기/설정/제거를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="178c1-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="178c1-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="178c1-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="178c1-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="178c1-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="178c1-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="178c1-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="178c1-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="178c1-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2371">Az.Websites</span></span>
* <span data-ttu-id="178c1-2372">'New-AzWebApp -IncludeSourceWebAppSlots'를 사용하여 모든 슬롯의 복제를 중단하는 ARM 템플릿 버그가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="178c1-2373">1.5.0 - 2019년 3월</span><span class="sxs-lookup"><span data-stu-id="178c1-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2374">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2375">'Register-AzModule' 명령을 추가하여 AutoRest 생성 cmdlet을 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="178c1-2376">Connect-AzAccount 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2377">Az.Automation</span></span>
* <span data-ttu-id="178c1-2378">몇몇 Azure Automation cmdlet에서 특정 월별 일정을 검색할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="178c1-2379">상위 20개 노드를 반환하도록 Get-AzAutomationDscNode를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="178c1-2380">이제 모든 노드 반환</span><span class="sxs-lookup"><span data-stu-id="178c1-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-2381">Az.Cdn</span></span>
* <span data-ttu-id="178c1-2382">사용자 지정 도메인 Https 사용/사용 안 함에 대한 새 Powershell cmdlet이 추가되었으며 기존의 것은 사용되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2383">Az.Compute</span></span>
* <span data-ttu-id="178c1-2384">Get cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-2385">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-2386">ADF.Net SDK 버전이 3.0.1로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="178c1-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="178c1-2387">Az.LogicApp</span></span>
* <span data-ttu-id="178c1-2388">첫 결과 페이지 검색 시에만 ListWorkflows 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2389">Az.Network</span></span>
* <span data-ttu-id="178c1-2390">Network cmdlet에 와일드 카드 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-2392">Azure VM 지원에 SQL 서버가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="178c1-2393">SDK 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2393">SDK Update</span></span>
* <span data-ttu-id="178c1-2394">VMappContainer 체크 인 Get-ProtectableItem 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="178c1-2395">Get ProtectableItem의 매개 변수로 Name과 ServerName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2396">Az.Resources</span></span>
* <span data-ttu-id="178c1-2397">`-TemplateObject` 매개 변수를 추가하여 cmdlet을 배포</span><span class="sxs-lookup"><span data-stu-id="178c1-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="178c1-2398">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2933 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="178c1-2399">`Get-AzResource`의 결과를 `Set-AzResource`(으)로 파이프할 때 발생하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="178c1-2400">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8240 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="178c1-2401">실행 시 JSON 데이터 형식 문제 해결 `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="178c1-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="178c1-2402">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7930 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2403">Az.Sql</span></span>
* <span data-ttu-id="178c1-2404">AuditingEndpointsCommunicator를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="178c1-2405">새 진단 설정을 생성할 때 에지 사례의 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2406">Az.Storage</span></span>
* <span data-ttu-id="178c1-2407">스토리지 계정      - New-AzStorageAccount를 생성할 때 종류 BlockBlobStorage를 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="178c1-2408">1.4.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="178c1-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="178c1-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="178c1-2410">사용되지 않는 AddAzureASAccount cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2411">Az.Automation</span></span>
* <span data-ttu-id="178c1-2412">Import-AzAutomationDscNodeConfiguration 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="178c1-2413">Import-AzAutomationDscConfiguration cmdlet 구성 이름 유효성 검사 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="178c1-2414">Import-AzAutomationDscConfiguration cmdlet 오류 처리 개선</span><span class="sxs-lookup"><span data-stu-id="178c1-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-2416">리소스의 하위 도메인을 지정하는 데 사용되는 New-AzCognitiveServicesAccount에 대한 새 선택적 매개 변수로 CustomSubdomainName이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2417">Az.Compute</span></span>
* <span data-ttu-id="178c1-2418">ID 매개 변수 집합 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="178c1-2419">Name 매개 변수를 제공하지 않으면 Get-AzVMExtension이 설치된 모든 확장을 열거하도록 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="178c1-2420">Update-AzImage cmdlet에 태그 및 ResourceId 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="178c1-2421">인스턴스 ID가 없는 Get-AzVmssVM과 InstanceView를 사용하면 인스턴스 보기가 있는 VMSS VM을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2423">ADL 삭제된 항목 열거 및 복원에 대한 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="178c1-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="178c1-2424">Az.EventHub</span></span>
* <span data-ttu-id="178c1-2425">Eventhub의 CaptureDescription 클래스에서 빈 보관을 건너뛰는 새 부울 속성 SkipEmptyArchives가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-2426">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-2427">Set-AzKeyVaultSecret 태그 지정 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="178c1-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="178c1-2428">Az.LogicApp</span></span>
* <span data-ttu-id="178c1-2429">통합 계정에 대한 기본 sku 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="178c1-2430">XSLT 2.0, XSLT 3.0, Liquid 맵 형식 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="178c1-2431">통합 계정 어셈블리에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="178c1-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="178c1-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="178c1-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="178c1-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="178c1-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="178c1-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="178c1-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="178c1-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="178c1-2436">통합 계정 일괄 처리 구성에 대한 새 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="178c1-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="178c1-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="178c1-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="178c1-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="178c1-2441">논리 앱 SDK를 버전 4.1.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="178c1-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-2442">Az.Monitor</span></span>
* <span data-ttu-id="178c1-2443">Get-AzMetric에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2444">Az.Network</span></span>
* <span data-ttu-id="178c1-2445">Add-AzApplicationGatewayCustomError에 대한 도움말 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="178c1-2447">New 및 Get ApplicationInsights 데이터 소스에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="178c1-2448">지정된 작업 영역에 대한 특정 또는 전체 ApplicationInsights 데이터 원본 가져오기를 지원하기 위한 새로운 'ApplicationInsights' 종류가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="178c1-2449">지정된 Application-Insights 리소스 매개 변수(구독 ID, resourceGroupName 및 이름)별로 데이터 원본을 만들기 위한 New-AzOperationalInsightsApplicationInsightsDataSource cmdlet이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2450">Az.Resources</span></span>
* <span data-ttu-id="178c1-2451">문제 https://github.com/Azure/azure-powershell/issues/8166 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="178c1-2452">문제 https://github.com/Azure/azure-powershell/issues/8235 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="178c1-2453">문제 https://github.com/Azure/azure-powershell/issues/6219 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="178c1-2454">KeyCredentials 반복 만들기를 방지하기 위해 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2455">Az.Sql</span></span>
* <span data-ttu-id="178c1-2456">SQL DB 하이퍼스케일에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="178c1-2457">복원 요청에서 불필요한 속성을 설정하여 복원이 실패할 수 있는 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2458">Az.Websites</span></span>
* <span data-ttu-id="178c1-2459">Get-AzWebAppSlotMetrics 내 올바른 예제</span><span class="sxs-lookup"><span data-stu-id="178c1-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="178c1-2460">1.3.0 - 2019년 2월</span><span class="sxs-lookup"><span data-stu-id="178c1-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2461">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2462">ClientRuntime 최신 버전 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="178c1-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="178c1-2464">Az.AnalysisServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="178c1-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2465">Az.Compute</span></span>
* <span data-ttu-id="178c1-2466">AEM 확장: UltraSSD 및 P60, P70, P80 디스크에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="178c1-2467">Set-AzVMBootDiagnostics에 대한 도움말 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="178c1-2468">Update-AzImage에 대한 도움말 및 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="178c1-2470">Az.RecoveryServices 모듈의 전반적인 가용성.</span><span class="sxs-lookup"><span data-stu-id="178c1-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2471">Az.Resources</span></span>
* <span data-ttu-id="178c1-2472">리소스 그룹 관련 태그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="178c1-2473">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8166 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="178c1-2474">`Get-AzureRmRoleAssignment`이(가) -ErrorAction을 준수하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="178c1-2475">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8235 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2476">Az.Sql</span></span>
* <span data-ttu-id="178c1-2477">AzSqlDatabaseBackupShortTermRetentionPolicy 가져오기/설정하기 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="178c1-2478">SQL cmdlet을 실행할 경우 Azure 계정에 로그인되어 있지 않은 것이 nullref 예외를 초래하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="178c1-2479">Get-AzSqlCapability의 nullref 예외 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="178c1-2480">1.2.1 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="178c1-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2481">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2482">올바른 인증 버전을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="178c1-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="178c1-2484">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="178c1-2486">업데이트된 인증 종속성을 사용하여 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="178c1-2487">1.2.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="178c1-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2488">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2489">Windows PowerShell 5.1 전용 대화형 사용자 이름/암호 인증 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="178c1-2490">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="178c1-2491">Uninstall-AzureRm 관련 PS Core에 경고 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="178c1-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="178c1-2492">Az.Aks</span></span>
* <span data-ttu-id="178c1-2493">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="178c1-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2494">Az.Automation</span></span>
* <span data-ttu-id="178c1-2495">Python 2 Runbook에 대한 지원이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="178c1-2496">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="178c1-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="178c1-2497">Az.Cdn</span></span>
* <span data-ttu-id="178c1-2498">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2499">Az.Compute</span></span>
* <span data-ttu-id="178c1-2500">Invoke-AzVMReimage cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="178c1-2501">Set-AzVmss에 TempDisk 매개 변수 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="178c1-2502">New-AzVM 경고 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="178c1-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="178c1-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="178c1-2504">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="178c1-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="178c1-2505">Az.DataFactory</span></span>
* <span data-ttu-id="178c1-2506">ADF.Net SDK 버전이 3.0.0으로 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2508">MSI를 사용할 때 ADLS 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="178c1-2509">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7462 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="178c1-2510">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-2511">Az.IotHub</span></span>
* <span data-ttu-id="178c1-2512">Add-IotHubRoutingEndpoint cmdlet에 인코딩 형식을 추가하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="178c1-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-2513">Az.KeyVault</span></span>
* <span data-ttu-id="178c1-2514">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2515">Az.Network</span></span>
* <span data-ttu-id="178c1-2516">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2517">Az.Resources</span></span>
* <span data-ttu-id="178c1-2518">'New-AzADAppCredential' 및 'New-AzADSpCredential' 참조 설명서의 잘못된 예제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="178c1-2519">리소스 그룹 배포 cmdlet 실행 전 '-TemplateFile' 매개 변수 경로가 확인되지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="178c1-2520">Az.Resources: New-AzureRmPolicyDefinition -Mode 기본값에 대한 올바른 설명서</span><span class="sxs-lookup"><span data-stu-id="178c1-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="178c1-2521">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/7522 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="178c1-2522">Az.Resources: 문제 https://github.com/Azure/azure-powershell/issues/5747 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="178c1-2523">'PSResourceGroupDeployment' 개체의 서식 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="178c1-2524">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/2123 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-2526">인증서가 VMSS 모델에 추가되었는데도 예외가 발생할 경우 롤백합니다. 이는 버그 https://github.com/Azure/service-fabric-issues/issues/932 를 수정하기 위함입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="178c1-2527">일부 오류 메시지를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2527">Fix some error messages.</span></span>
* <span data-ttu-id="178c1-2528">Az로의 마이그레이션을 통해서는 작동하지 않는 New-AzServiceFabriCluster를 위해 기본값 ARM 템플릿을 가진 클러스터 만들기를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="178c1-2529">확장에서 클러스터 id를 확인하여 클러스터에 해당하는 VMSS에만 추가되도록 클러스터/애플리케이션 인증서 추가를 수정하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="178c1-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="178c1-2530">Az.SignalR</span></span>
* <span data-ttu-id="178c1-2531">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2532">Az.Sql</span></span>
* <span data-ttu-id="178c1-2533">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="178c1-2534">가능한 값을 가진 LicenseType 매개 변수에 대한 매개 변수 설명이 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="178c1-2535">유일하게 업데이트된 속성인데 작동하지 않는 관리되는 인스턴스 ID의 업데이트 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="178c1-2536">관리되는 인스턴스에서의 사용자 지정 데이터 정렬에 대한 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2537">Az.Storage</span></span>
* <span data-ttu-id="178c1-2538">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="178c1-2539">Premium Storage 계정이 클래식 로깅/메트릭을 지원하지 않기 때문에, Premium Storage 계정의 클래식 로깅/메트릭을 가져올/설정할 때 상세한 오류 메시지를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="178c1-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="178c1-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="178c1-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="178c1-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="178c1-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="178c1-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="178c1-2543">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2544">Az.Websites</span></span>
* <span data-ttu-id="178c1-2545">잘못된 온라인 도움말 URL 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="178c1-2546">앱이 ASE에 호스팅되면 'New-AzWebAppSSLBinding'을 수정하여 올바른 resourcegroup+location에 인증서를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="178c1-2547">'New-AzWebAppSSLBinding'을 수정하여 SSL 인증서를 앱에 바인딩하는 데 붙는 태그를 덮어쓰지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="178c1-2548">1.1.0 - 2019년 1월</span><span class="sxs-lookup"><span data-stu-id="178c1-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="178c1-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2549">Az.Accounts</span></span>
* <span data-ttu-id="178c1-2550">Enable-AzureRmAlias에 'Local' 범위 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2551">Az.Compute</span></span>
* <span data-ttu-id="178c1-2552">이름이 Restart/Start/Stop/Remove/Set-AzVM과 Save-AzVMImage에 설정된 ID 매개 변수에서 선택 사항이 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="178c1-2553">도움말 파일의 ID에 대한 설명이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="178c1-2554">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2556">SDK 수정을 위해 데이터 평면의 SDK 버전을 1.1.14로 업데이트하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="178c1-2557">getfilestatus 및 liststatus에 대한 음수 acesstime 및 modificationtime 수정, 비동기 취소 토큰 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="178c1-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="178c1-2558">Az.EventGrid</span></span>
* <span data-ttu-id="178c1-2559">2019-01-01 API 버전을 사용하도록 업데이트되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="178c1-2560">2019-01-01 API 버전에서 새 시나리오를 지원하도록 다음 cmdlet을 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="178c1-2561">New-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="178c1-2562">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="178c1-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="178c1-2563">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="178c1-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="178c1-2564">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="178c1-2565">Update-AzureRmEventGridSubscription: 지정을 위한 새로운 선택적 매개 변수를 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="178c1-2566">이벤트 Time-to-Live</span><span class="sxs-lookup"><span data-stu-id="178c1-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="178c1-2567">이벤트에 대한 최대 배달 시도</span><span class="sxs-lookup"><span data-stu-id="178c1-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="178c1-2568">배달 못한 편지의 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="178c1-2569">New-AzureRmEventGridSubscription 및 Update-AzureRmEventGridSubscription cmdlet의 EndpointType 옵션에 새 열거형 값(즉, storageQueue 및 hybridConnection)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="178c1-2570">이벤트 구독을 생성 또는 업데이트할 때 사용자가 직접 조치를 취해야 할 경우 경고 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="178c1-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="178c1-2571">Az.IotHub</span></span>
* <span data-ttu-id="178c1-2572">최신 버전의 Azure IotHub SDK로 업데이트됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="178c1-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="178c1-2573">Az.LogicApp</span></span>
* <span data-ttu-id="178c1-2574">지정된 이름이 없는 모든 Get-AzLogicApp 목록</span><span class="sxs-lookup"><span data-stu-id="178c1-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2575">Az.Resources</span></span>
* <span data-ttu-id="178c1-2576">'Get-AzResource'에 '-ODataQuery'및 '-ResourceId' 매개 변수를 제공할 때 매개 변수 집합 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="178c1-2577">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/7875 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="178c1-2578">New/Set-AzPolicyDefinition에서 -Custom 매개 변수 처리 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="178c1-2579">New-AzDeployment 설명서에서 오타 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="178c1-2580">'New-AzADUser'에 '-MailNickname'매개 변수가 필수 항목으로 지정됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="178c1-2581">자세한 내용은 여기 https://github.com/Azure/azure-powershell/issues/8220 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="178c1-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="178c1-2582">Az.SignalR</span></span>
* <span data-ttu-id="178c1-2583">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2584">Az.Sql</span></span>
* <span data-ttu-id="178c1-2585">Storage 관리 클라이언트 종속성을 일반적인 SDK 구현으로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="178c1-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2586">Az.Storage</span></span>
* <span data-ttu-id="178c1-2587">Sas Token, OAuth 또는 Anonymous를 사용하여 스토리지 컨텍스트의 StorageAccountName을 실제 스토리지 계정 이름으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="178c1-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="178c1-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="178c1-2589">'-FullUri' 매개 변수를 사용하여 Blob 스냅샷 개체의 Sas Token을 생성하고 반환된 Uri를 스냅샷 Uri로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="178c1-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="178c1-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2591">Az.Websites</span></span>
* <span data-ttu-id="178c1-2592">'Get-AzDeletedWebApp'의 날짜 구문 분석 버그를 수정했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="178c1-2593">Az.Accounts 모듈을 사용할 때의 이전 버전과의 호환성 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="178c1-2594">1.0.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="178c1-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="178c1-2595">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-2595">General</span></span>

- <span data-ttu-id="178c1-2596">Az 모듈 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="178c1-2597">각 모듈에 대 한 온라인 도움말</span><span class="sxs-lookup"><span data-stu-id="178c1-2597">Online help for each module</span></span>
- <span data-ttu-id="178c1-2598">자세한 내용과 로드맵은 [Az 알림 페이지](https://aka.ms/azps-announce)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="178c1-2599">AzureRM에서 마이그레이션하는 것에 대한 정보는 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="178c1-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="178c1-2600">Az.Accounts</span></span>
- <span data-ttu-id="178c1-2601">Az.Profile에서 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="178c1-2602">프로필 및 컨텍스트 형식에 대한 표 형식 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="178c1-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="178c1-2604">#7002에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2604">Fixes for #7002</span></span>
- <span data-ttu-id="178c1-2605">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="178c1-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="178c1-2606">Az.Batch</span></span>
- <span data-ttu-id="178c1-2607">`PSComputeNode`의 새로운 `NodeAgentInformation` 속성을 통해 풀의 각 VM에서 실행 중인 Azure Batch 노드 에이전트의 버전을 확인하는 기능이 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="178c1-2608">`PSDataDisk`에 대한 `Caching` 기본 값은 이제 `None` 대신 `ReadWrite`입니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="178c1-2609">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="178c1-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="178c1-2610">Az.Billing</span></span>
- <span data-ttu-id="178c1-2611">청구, 소비 및 UsageAggregates cmdlet 결합 cmdlet에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="178c1-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="178c1-2613">New-AzureRmCognitiveServicesAccount 작업에서 사용 가능한 SkuName 및 Typem에 대한 완성자 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="178c1-2614">Get-AzCognitiveServicesAccountSkus에서 GetSkusWithAccountParamSetName 매개 변수 집합을 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="178c1-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="178c1-2616">ManagedIdentity 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="178c1-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="178c1-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="178c1-2618">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="178c1-2620">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="178c1-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="178c1-2621">Az.Monitor</span></span>
- <span data-ttu-id="178c1-2622">Az.Monitor 이름 변경 및 기타 사소한 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="178c1-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="178c1-2623">Az.KeyVault</span></span>
- <span data-ttu-id="178c1-2624">출력 형식에서 사용되지 않는 'PurgeDisabled' 속성 제거</span><span class="sxs-lookup"><span data-stu-id="178c1-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="178c1-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="178c1-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="178c1-2626">Az.MachineLearningCompute 모듈의 cmdlet 포함</span><span class="sxs-lookup"><span data-stu-id="178c1-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="178c1-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="178c1-2627">Az.Media</span></span>
- <span data-ttu-id="178c1-2628">New-AzMediaService에서 사용되지 않는 -Tags 별칭이 제거됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="178c1-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2629">Az.Network</span></span>
<span data-ttu-id="178c1-2630">Application Gateway에서 RewriteRuleSets를 구성하는 것에 대한 지원이 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="178c1-2631">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="178c1-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="178c1-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="178c1-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="178c1-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="178c1-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="178c1-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="178c1-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="178c1-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="178c1-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="178c1-2640">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="178c1-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="178c1-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="178c1-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="178c1-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="178c1-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="178c1-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="178c1-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="178c1-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="178c1-2646">New-AzureRmApplicationGatewayUrlPathMapConfig로 ID를 사용하여 Application Gateway에 KeyVault 지원을 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="178c1-2647">선택적 매개 변수를 사용하도록 cmdlet이 업데이트됨 -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="178c1-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="178c1-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="178c1-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="178c1-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="178c1-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="178c1-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="178c1-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="178c1-2651">New-AzApplicationGateway cmdlet이 선택적 매개 변수를 사용하도록 업데이트됨 -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="178c1-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="178c1-2652">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="178c1-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="178c1-2654">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="178c1-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="178c1-2655">Az.Profile</span></span>
- <span data-ttu-id="178c1-2656">Az.Accounts에 모듈 이름이 변경됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="178c1-2658">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="178c1-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2659">Az.Resources</span></span>
- <span data-ttu-id="178c1-2660">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="178c1-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="178c1-2662">일반 이름과 지문으로 지정 인증서 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="178c1-2663">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="178c1-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="178c1-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="178c1-2665">SIgnalR에 대한 PowerShell cmdlet에 대한 일반 공급</span><span class="sxs-lookup"><span data-stu-id="178c1-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="178c1-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2666">Az.Sql</span></span>
- <span data-ttu-id="178c1-2667">위협 탐지의 cmdlet에 새로운 Data_Exfiltration 및 Unsafe_Action 검색 유형 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="178c1-2668">Sql 감사 cmdlet에 대한 설명서 예제 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="178c1-2669">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="178c1-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2670">Az.Storage</span></span>
- <span data-ttu-id="178c1-2671">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="178c1-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2672">Az.Websites</span></span>
- <span data-ttu-id="178c1-2673">부수적인 호환성이 손상되는 변경에 대한 자세한 내용은 [마이그레이션 가이드](https://aka.ms/azps-migration-guide)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="178c1-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="178c1-2674">0.7.0 - 2018년 12월</span><span class="sxs-lookup"><span data-stu-id="178c1-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="178c1-2675">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-2675">General</span></span>

* <span data-ttu-id="178c1-2676">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="178c1-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2677">Az.Compute</span></span>

* <span data-ttu-id="178c1-2678">`New-AzVm(ss)` cmdlet에 대한 간단한 매개 변수 집합에 UltraSSD 및 갤러리 이미지에 대한 지원을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="178c1-2680">ADLS 계정의 도메인의 후행 슬래시를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="178c1-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="178c1-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="178c1-2682">일부 끊어진 링크 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="178c1-2683">New-AzureRmFrontDoor 및 Set-AzureRmFrontDoor 아티클에서 New-AzureRmFrontDoorHealthProbeSettingObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="178c1-2684">New-AzureRmFrontDoorManagedRuleObject 아티클에서 New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet 아티클에 대한 링크가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="178c1-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="178c1-2686">Azure File Share 복원 작업에 클라이언트 측 유효성 검사가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="178c1-2687">afs 복원의 경우 storageAccountName 및 storageAccountResourceGroupName을 선택적으로 만들었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="178c1-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2688">Az.Resources</span></span>

* <span data-ttu-id="178c1-2689">https://github.com/Azure/azure-powershell/issues/7679 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="178c1-2690">기본 관리자를 요청할 때 구독 범위가 제공되는 경우 Get-AzureRmRoleAssignment를 업데이트하여 구독 범위를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="178c1-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2691">Az.Sql</span></span>

* <span data-ttu-id="178c1-2692">AzureRM에서 Az 전환 예정에 대한 사소한 변경</span><span class="sxs-lookup"><span data-stu-id="178c1-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="178c1-2693">DotNet 코어에서 Get-AzureRmSqlDatabaseVulnerabilityAssessment를 사용하는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="178c1-2694">SQL 감사 cmdlet과 관련된 도움말 메시지의 설명서가 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="178c1-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2695">Az.Storage</span></span>

* <span data-ttu-id="178c1-2696">New-AzureRmStorageAccount에 -EnableHierarchicalNamespace 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="178c1-2697">파일 복사 cmdlet이 -DestContext 입력이 없을 때 대상의 원본 컨텍스트를 다시 사용할 수 없는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="178c1-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="178c1-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="178c1-2699">고정적인 웹 사이트 구성 지원</span><span class="sxs-lookup"><span data-stu-id="178c1-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="178c1-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="178c1-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="178c1-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="178c1-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="178c1-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2702">Az.Websites</span></span>

* <span data-ttu-id="178c1-2703">Set-AzureRmWebApp 및 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="178c1-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="178c1-2704">Windows 및 Linux 컨테이너 응용 프로그램에 탑재할 Azure Storage 경로를 지정하기 위해 새 매개 변수(-AzureStoragePath)가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="178c1-2705">새 cmdlet New-AzureRmWebAppAzureStoragePath의 출력을 매개 변수로 사용하여 Azure Storage 경로를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="178c1-2706">0.6.1 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="178c1-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="178c1-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="178c1-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="178c1-2708">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="178c1-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="178c1-2709">Az.Automation</span></span>
* <span data-ttu-id="178c1-2710">Azure Automation cmdlet 기반 Swagger</span><span class="sxs-lookup"><span data-stu-id="178c1-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="178c1-2711">업데이트 관리 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="178c1-2712">소스 제어 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="178c1-2713">Remove-AzureRmAutomationHybridWorkerGroup cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="178c1-2714">DSC 노드 등록 명령 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="178c1-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2715">Az.Compute</span></span>
* <span data-ttu-id="178c1-2716">SystemAssigned ID에 대한 ID 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="178c1-2717">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="178c1-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="178c1-2719">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="178c1-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="178c1-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="178c1-2721">마켓플레이스 cmdlet에 대한 예제 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="178c1-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2722">Az.Network</span></span>
* <span data-ttu-id="178c1-2723">New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="178c1-2724">지원되는 AzureFirewall 네트워크 프로토콜에 ICMP 다시 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="178c1-2725">Test-AzureRmNetworkWatcherConnectivity cmdlet을 업데이트하여 대상 ID, 주소 및 포트 유효성 검사를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="178c1-2726">VirtualNetwork 맵의 메모리 사용 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="178c1-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="178c1-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="178c1-2728">보호된 파일 공유에 대한 정책을 수정하는 것에 대해 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="178c1-2729">정책 표준 시간대를 대문자로 변환했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="178c1-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="178c1-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="178c1-2731">New-AzureRmRecoveryServicesAsrProtectableItem의 예제 정정</span><span class="sxs-lookup"><span data-stu-id="178c1-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="178c1-2732">형식 매핑 문제에 대한 종속성 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="178c1-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="178c1-2733">Az.Relay</span></span>
* <span data-ttu-id="178c1-2734">선택적 매개 변수 -KeyValue를 New-AzureRmRelayKey cmdlet에 추가하여 사용자가 KeyValue를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="178c1-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2735">Az.Resources</span></span>
* <span data-ttu-id="178c1-2736">`New-AzureRmPolicyAssignment` 및 `Set-AzureRmPolicyAssignment`의 자원 ID 관련 매개 변수에 대한 도움말 문서를 업데이트함</span><span class="sxs-lookup"><span data-stu-id="178c1-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="178c1-2737">-Metadata를 사용하는 New-AzureRmPolicyDefinition에 대한 예제 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="178c1-2738">NetStandard의 태그 키에서 대소문자 보존을 허용하도록 수정: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="178c1-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="178c1-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-2740">향후 호환성이 손상되는 변경에 대한 사용 중단 메시지 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="178c1-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2741">Az.Sql</span></span>
* <span data-ttu-id="178c1-2742">Azure Sql Database Managed Instance 및 Azure Sql Managed Database에 CRUD 작업을 위한 새 cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="178c1-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="178c1-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="178c1-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="178c1-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="178c1-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="178c1-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="178c1-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="178c1-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="178c1-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="178c1-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="178c1-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="178c1-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="178c1-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="178c1-2751">서버 또는 데이터베이스에서 확장 감사 정책 관리를 활성화했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="178c1-2752">새 매개 변수(PredicateExpression)가 감사 로그 필터링을 사용하도록 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="178c1-2753">Cmdlet이 레거시 클라이언트 대신 SQL 클라이언트를 사용하도록 수정되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="178c1-2754">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="178c1-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="178c1-2755">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="178c1-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="178c1-2756">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="178c1-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="178c1-2757">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="178c1-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="178c1-2758">스토리지 계정 이름 매개 변수가 설정된 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings를 사용할 때의 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="178c1-2759">0.5.0 - 2018년 11월</span><span class="sxs-lookup"><span data-stu-id="178c1-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="178c1-2760">일반</span><span class="sxs-lookup"><span data-stu-id="178c1-2760">General</span></span>
* <span data-ttu-id="178c1-2761">많은 핵심 cmdlet에 Resource Completers를 추가하여 대화형으로 cmdlet을 호출할 때 기존 리소스 이름을 탭으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="178c1-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="178c1-2762">Az.Profile</span></span>
* <span data-ttu-id="178c1-2763">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="178c1-2764">Connect-AzAccount cmdlet의 매개 변수 TenantId 이름을 Tenant로 바꾸고 TenantId의 별칭을 추가합니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="178c1-2765">Connect-AzAccount의 업데이트된 TenantId 설명</span><span class="sxs-lookup"><span data-stu-id="178c1-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="178c1-2766">테넌트 도메인을 제공할 때 실패한 로그인에 대한 오류 메시지 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="178c1-2767">테넌트에 구독이 없는 계정의 컨텍스트 이름 충돌 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="178c1-2768">MSI를 사용할 때 DataLake 엔드포인트 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="178c1-2769">연결되지 않은 경우 'Disconnect-AzAccount'가 throw하는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-2771">Get-AzCognitiveServicesAccountSkus 작업을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2772">Az.Compute</span></span>
* <span data-ttu-id="178c1-2773">Add-AzVmssVMDataDisk 및 Remove-AzVmssVMDataDisk cmdlet를 추가합니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="178c1-2774">Get-AzVMImage는 AutomaticOSUpgradeProperties를 표시합니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="178c1-2775">수정된 SetAzVMChefExtension -BootstrapOptions 및 -JsonAttribute option 값이 json 형식으로 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2777">DataLake 패키지를 1.1.10으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="178c1-2778">기본 동시성을 다중 스레드 작업에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="178c1-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="178c1-2779">Az.Insights</span></span>
* <span data-ttu-id="178c1-2780">해결된 문제 #7267(자동 크기 조정 영역)</span><span class="sxs-lookup"><span data-stu-id="178c1-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="178c1-2781">열거된 매개 변수를 제대로 설정하지 않은 새 자동 크기 조정 규칙을 만드는 데 문제가 있습니다(이를 항상 기본값으로 설정함).</span><span class="sxs-lookup"><span data-stu-id="178c1-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="178c1-2782">해결된 문제 # 7513[자세한 정보] Set-AzDiagnosticSetting은 설정을 생성하는 동안 범주를 명시적으로 지정해야 합니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="178c1-2783">이제 cmdlet은 생성 중에 사용할 범주를 명시적으로 표시할 필요가 없습니다. 즉, 문서화된대로 작동합니다</span><span class="sxs-lookup"><span data-stu-id="178c1-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2784">Az.Network</span></span>
* <span data-ttu-id="178c1-2785">다음 cmdlet에 대해 PeeringType을 필수 매개 변수로 변경했습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="178c1-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="178c1-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="178c1-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="178c1-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="178c1-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="178c1-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="178c1-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="178c1-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="178c1-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="178c1-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="178c1-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="178c1-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="178c1-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="178c1-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="178c1-2793">추가된 정책 재구성 cmdlet</span><span class="sxs-lookup"><span data-stu-id="178c1-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2794">Az.Resources</span></span>
* <span data-ttu-id="178c1-2795">https://github.com/Azure/azure-powershell/issues/7402 에 대한 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="178c1-2796">'Get-AzResource'에 대해 '-ResourceId' 매개 변수를 사용하여 리소스 나열 허용</span><span class="sxs-lookup"><span data-stu-id="178c1-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="178c1-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="178c1-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="178c1-2798">마이그레이션 상태를 알 수 있도록 PSServiceBusMigrationConfigurationAttributes에 MigrationState 읽기 전용 속성 추가.</span><span class="sxs-lookup"><span data-stu-id="178c1-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="178c1-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="178c1-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="178c1-2800">Linux Vmss에 인증서 추가 수정.</span><span class="sxs-lookup"><span data-stu-id="178c1-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="178c1-2801">Add-AzServiceFabricClusterCertificate 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="178c1-2802">새 인증서(Azure/service-fabric-issues#932)에서 올바른 지문을 사용.</span><span class="sxs-lookup"><span data-stu-id="178c1-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="178c1-2803">올바르게 예외 표시(Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="178c1-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="178c1-2804">Vmss CreateOrUpdate 작업을 시작하기 전에 'Update-AzServiceFabricDurability'를 수정하여 클러스터 구성 업데이트.</span><span class="sxs-lookup"><span data-stu-id="178c1-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="178c1-2805">0.4.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="178c1-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="178c1-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="178c1-2806">Az.Profile</span></span>
* <span data-ttu-id="178c1-2807">CloudShell에서 Get-AzSubscription을 사용하여 문제를 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="178c1-2808">ClientRuntime의 최신 버전을 사용하도록 일반적인 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2809">Az.Compute</span></span>
* <span data-ttu-id="178c1-2810">'New-AzVm'에 대해 간단한 매개 변수를 사용하는 경우 가속화된 네트워킹을 설정하기 위해 새 크기가 VM 크기의 허용 목록에 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="178c1-2811">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="178c1-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="178c1-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="178c1-2813">Virtual Network 규칙에 대한 지원 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="178c1-2814">Get-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 가져오거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="178c1-2815">Add-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 가상 네트워크 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="178c1-2816">Set-AzDataLakeStoreVirtualNetworkRule: 지정된 Data Lake Store 계정에 지정된 가상 네트워크 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="178c1-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Azure Data Lake Store 가상 네트워크 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2818">Az.Network</span></span>
* <span data-ttu-id="178c1-2819">Test-AzNetworkWatcherConnectivity cmdlet을 업데이트하고, 백 엔드에 프로토콜 값을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="178c1-2820">모든 cmdlet에 ResourceName 인수 완성자가 추가되었습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2821">Az.Resources</span></span>
* <span data-ttu-id="178c1-2822">(기본 프로필에 구독이 없고 범위가 지정되지 않은 경우) 시나리오에서 의미 있는 예외를 추가하여 Get-AzRoleDefinition이 인식할 수 없는 예외를 throw하는 문제를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="178c1-2823">또한 기본 매개 변수 집합을 'RoleDefinitionNameParameterSet'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="178c1-2824">0.3.0 - 2018년 10월</span><span class="sxs-lookup"><span data-stu-id="178c1-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="178c1-2825">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="178c1-2825">Azure.Storage</span></span>
* <span data-ttu-id="178c1-2826">대상에 메타데이터가 있을 때 Blob/파일이 메타 데이터를 복사하지 않는 문제 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="178c1-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="178c1-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="178c1-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="178c1-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="178c1-2829">특정 위치의 스토리지 리소스 사용을 지원하고 글로벌 스토리지 리소스 사용 가져오기는 더 이상 사용되지 않는다는 경고 메시지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="178c1-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="178c1-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="178c1-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="178c1-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="178c1-2832">기존 계정이 없는 Get-AzCognitiveServicesAccountSkus를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="178c1-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="178c1-2833">Az.Compute</span></span>
* <span data-ttu-id="178c1-2834">Get-AzVM -ResourceGroupName <rg>가 필요한 경우 50개가 넘는 결과를 반환하도록 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="178c1-2835">'SimpleParameterSet' 예제가 New-AzVmss cmdlet 도움말에 추가됨</span><span class="sxs-lookup"><span data-stu-id="178c1-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="178c1-2836">Azure Disk Encryption 진행률 메시지의 오타를 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="178c1-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="178c1-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="178c1-2838">ADF.Net SDK 버전을 2.3.0으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="178c1-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="178c1-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="178c1-2839">Az.Network</span></span>
* <span data-ttu-id="178c1-2840">NetworkProfile 기능 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="178c1-2841">추가된 새 cmdlet은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2841">new cmdlets added</span></span>
    - <span data-ttu-id="178c1-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="178c1-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="178c1-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="178c1-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="178c1-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="178c1-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="178c1-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="178c1-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="178c1-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="178c1-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="178c1-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="178c1-2848">서브넷 모델에 서비스 연결 링크 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="178c1-2849">New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="178c1-2850">Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig cmdlet 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="178c1-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="178c1-2851">Az.RedisCache</span></span>
* <span data-ttu-id="178c1-2852">모든 문자열을 Size 매개 변수로 진행되도록 허용</span><span class="sxs-lookup"><span data-stu-id="178c1-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="178c1-2853">PSArgumentCompleter 팝업에 P5 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="178c1-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="178c1-2854">Az.Resources</span></span>
* <span data-ttu-id="178c1-2855">-Mode 매개 변수를 Set-AzPolicyDefinition에 추가</span><span class="sxs-lookup"><span data-stu-id="178c1-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="178c1-2856">사용자가 포함된 Origin 작업에서 Get-AzProviderOperation commandlet 버그 수정</span><span class="sxs-lookup"><span data-stu-id="178c1-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="178c1-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="178c1-2857">Az.Sql</span></span>
* <span data-ttu-id="178c1-2858">일부 백업 cmdlet이 현재 azure 구독을 인식하지 않는 문제 해결</span><span class="sxs-lookup"><span data-stu-id="178c1-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="178c1-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="178c1-2859">Az.Websites</span></span>
* <span data-ttu-id="178c1-2860">새 cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 컨테이너 지속적인 배포 Webhook URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="178c1-2861">새 cmdlet New-AzWebAppContainerPSSession 및 Enter-WebAppContainerPSSession -  windows 컨테이너 앱에 PowerShell 원격 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="178c1-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="178c1-2862">0.2.0 - 2018년 9월</span><span class="sxs-lookup"><span data-stu-id="178c1-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="178c1-2863">초기 릴리스</span><span class="sxs-lookup"><span data-stu-id="178c1-2863">Initial Release</span></span>