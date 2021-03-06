---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015392"
---
# Update-AzVmss

## SYNOPSIS
VMSS의 상태를 업데이트합니다.

## 구문

### DefaultParameter(기본값)
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Update-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set) 상태를 로컬 VMSS 개체의 상태로 업데이트합니다.

## 예제

### 예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트합니다.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

이 명령은 그룹001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS의 상태를 로컬 VMSS 개체의 상태로 $LocalVMSS.

## 매개 변수

### -AsJob
백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.

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

### -AutomaticOSUpgrade
최신 버전의 이미지를 사용할 수 있을 때 롤링 스타일로 집합 인스턴스의 크기 조정에 OS 업그레이드를 자동으로 적용해야 하는지 여부를 설정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
VM의 상태 변경으로 인해 자동 복구가 일시 중단되는 시간입니다. 상태 변경이 완료된 후에 유예 시간이 시작됩니다. 이렇게 하면 조기 또는 우발적 복구를 방지할 수 있습니다. 시간 기간은 ISO 8601 형식으로 지정해야 합니다. 허용되는 최소 유예 기간은 PT30M(30분)입니다. 이는 기본값입니다. 허용되는 최대 유예 기간은 90분(PT90M)입니다.

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

### -BootDiagnosticsEnabled
가상 머신 확장 집합에서 부팅 진단을 사용하도록 설정해야 하는지 여부입니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
콘솔 출력 및 스크린샷을 배치하는 데 사용할 저장소 계정의 URI입니다.

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

### -CustomData
사용자 지정 데이터의 base-64 인코딩된 문자열을 지정합니다.
가상 머신의 파일로 저장되는 이진 배열로 디코딩됩니다.
이진 배열의 최대 길이는 65535 바이트입니다. <br>
VM에 클라우드-init를 사용하는 경우 만들기 중에 [Cloud-init를 사용하여 Linux VM을 사용자 지정하는 방법을 참조합니다.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -DisableAutoRollback
자동 OS 업그레이드 정책에 대한 자동 롤백 사용하지 않도록 설정

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
이 cmdlet은 Linux OS에 대한 암호 인증을 사용하지 않도록 설정하고 있습니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
가상 머신 확장 집합에서 자동 복구를 사용하도록 설정하거나 사용하지 않도록 설정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
VMSS의 Windows 가상 머신이 자동 업데이트를 사용하도록 설정되어 있는지 여부를 나타냅니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
이 매개 변수는 요청에서 사용자가 가상 머신 확장 집합에 대한 호스트 암호화를 사용하도록 설정하거나 사용하지 않도록 설정할 수 있습니다. 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityId
가상 머신 확장 집합과 연결된 사용자 ID 목록을 지정합니다.
사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
가상 머신 확장 집합에 사용되는 ID 유형을 지정합니다.
'SystemAssignedUserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.
'None' 형식은 가상 머신 확장 집합에서 ID를 제거합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- 없음

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceId
이미지 참조 ID를 지정합니다.

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

### -ImageReferenceOffer
VMImage(가상 머신 이미지) 제품 유형을 지정합니다.
이미지 제안을 얻은 경우 Get-AzVMImageOffer cmdlet을 사용 합니다.

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

### -ImageReferencePublisher
VMImage의 게시자의 이름을 지정합니다.
퍼블리셔를 얻지 위해 Get-AzVMImagePublisher cmdlet을 사용 합니다.

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

### -ImageReferenceSku
VMImage SKU를 지정합니다.
SKUS를 얻지 위해 Get-AzVMImageSku cmdlet을 사용 합니다.

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

### -ImageReferenceVersion
VMImage 버전을 지정합니다.
최신 버전을 사용하기 위해 특정 버전 대신 최신 값을 지정합니다.

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

### -ImageUri
사용자 이미지에 대한 Blob URI를 지정합니다.
VMSS는 사용자 이미지의 동일한 컨테이너에 운영 체제 디스크를 만듭니다.

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

### -LicenseType
라이선스 시나리오를 가져오기 위한 라이선스 유형을 지정합니다.

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

### -ManagedDiskStorageAccountType
관리 디스크에 대한 저장소 계정 유형을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- StandardLRS
- PremiumLRS

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

### -MaxBatchInstancePercent
한 번의 일괄 처리로 롤링 업그레이드를 통해 동시에 업그레이드되는 총 가상 머신 인스턴스의 최대 백분율입니다.
이전 또는 향후 일괄 처리에서 최대의 이상한 인스턴스이기 때문에 일괄 처리의 인스턴스 백분율이 감소하여 더 높은 안정성을 보장할 수 있습니다.
값을 지정하지 않으면 20으로 설정됩니다.

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

### -MaxPrice
우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정합니다. 이 가격은 미국 달러입니다. 이 가격은 VM 크기에 대한 현재 낮은 우선 순위 가격과 비교됩니다. 또한 가격은 우선 순위가 낮은 VM/VMSS를 만들/업데이트할 때 비교하며, maxPrice가 현재 낮은 우선 순위 가격보다 큰 경우 작업이 성공합니다. 현재 낮은 우선 순위 가격이 VM/VMSS를 생성한 후 maxPrice를 초과하는 경우, maxPrice는 우선 순위가 낮은 VM/VMSS를 지우는 데도 사용됩니다. 가능한 값은 0보다 큰 소수점 값입니다. 예: 0.01538입니다.  -1은 가격상의 이유로 우선 순위가 낮은 VM/VMSS를 아 내지 말아야 한다고 나타냅니다. 또한 기본 최대 가격은 사용자가 제공하지 않는 경우 -1입니다.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
업그레이드가 중단되기 전에 가상 머신 상태 확인에 의해 위태로울 수 있는 확장 집합의 총 가상 머신 인스턴스의 최대 백분율입니다.
이 제약 조건은 일괄 처리를 시작하기 전에 검사됩니다.
값을 지정하지 않으면 20으로 설정됩니다.

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

### -MaxUnhealthyUpgradedInstancePercent
업그레이드된 가상 머신 인스턴스의 최대 백분율은 상태가 상태가 나타남을 찾을 수 있습니다.
이 검사는 각 일괄 처리가 업그레이드된 후에 진행됩니다.
이 백분율을 초과하면 롤링 업데이트가 중단됩니다.
값을 지정하지 않으면 20으로 설정됩니다.

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

### -OsDiskCaching
운영 체제 디스크의 캐싱 모드를 지정합니다. 이 매개 변수에 대해 허용되는 값은 다음입니다.
- 없음
- ReadOnly
- ReadWrite 기본값은 ReadWrite입니다.
캐싱 값을 변경하면 cmdlet이 가상 머신을 다시 시작합니다.
이 설정은 디스크의 일관성 및 성능에 영향을 미치게 됩니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
OS 디스크에서 WriteAccelerator를 사용하도록 설정하거나 사용하지 않도록 설정해야 하는지 여부를 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overprovision
cmdlet이 VMSS를 오버프로비전하는지 여부를 나타냅니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
모든 가상 머신에 대한 업데이트를 한 일괄 처리로 완료하고 다음 일괄 처리를 시작하는 사이의 대기 시간입니다.
시간 기간은 ISO 8601 형식으로 지정해야 합니다.
기본값은 0초(PT0S)입니다.

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

### -PlanName
계획 이름을 지정합니다.

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

### -PlanProduct
계획 제품을 지정합니다.

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

### -PlanPromotionCode
계획 프로모션 코드를 지정합니다.

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

### -PlanPublisher
계획 게시자를 지정합니다.

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

### -ProvisionVMAgent
VMSS의 Windows 가상 머신에서 가상 머신 에이전트를 프로비전해야 하는지 여부를 나타냅니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
이 확장 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.

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

### -ResourceGroupName
VMSS가 속한 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
가상 머신 확장 집합의 크기 조정 시 따라야 할 규칙입니다.  가능한 값은 'Default', 'OldestVM' 및 'NewestVM'입니다.  가상 머신 확장 집합이 확장될 때 '기본값'은 크기 조정 집합이 영역 전체에 분산됩니다.  그런 다음 오류 도메인에서 가능한 한 균형이 조정됩니다.  각 장애 도메인 내에서 제거를 위해 선택한 가상 머신은 확장으로부터 보호되지 않는 가장 최근의 컴퓨터입니다.  가상 머신 확장 집합이 확장되는 경우 'OldestVM'은 확장으로부터 보호되지 않는 가장 오래된 가상 머신을 제거하기 위해 선택됩니다.  zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.  각 영역 내에서 보호되지 않는 가장 오래된 가상 머신은 제거를 위해 선택됩니다.  가상 머신 확장 집합이 확장되는 경우 'NewestVM'은 확장으로부터 보호되지 않는 가장 최근 가상 머신을 제거하기 위해 선택됩니다.  zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.  각 영역 내에서 보호되지 않는 가장 새로운 가상 머신은 제거를 위해 선택됩니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
단일 배치 그룹을 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVM
확장이 추가 오버프로비전된 VM에서 실행되지 않는지 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
VMSS의 인스턴스 수를 지정합니다.

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

### -SkuName
VMSS의 모든 인스턴스의 크기를 지정합니다.

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

### -SkuTier
VMSS의 계층을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 표준
- 기본

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

### -Tag
해시 테이블의 형태로 키 값 쌍입니다. 예: @{key0="value0";key1=$null;key2="value2"}

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

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
구성 가능한 시간(분) 삭제되는 Virtual Machine은 이벤트가 자동 승인(시간 제한)되기 전에 예약된 종료 이벤트를 승인해야 합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
예약된 종료 이벤트를 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 지정합니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Windows OS의 표준 시간대를 지정합니다. 예: \" 태평양 표준시 \" 입니다. <br>
가능한 값은 [](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) [TimeZoneInfo.GetSystemTimeZones에서](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)TimeZoneInfo.Id 표준 시간대에서 값으로 사용할 수 있습니다.

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

### -UltraSSDEnabled
가상 머신 확장 집합에 저장소 계정 유형이 있는 하나 이상의 관리되는 데이터 디스크를 UltraSSD_LRS 수 있는 플래그입니다.
저장소 계정 유형이 있는 UltraSSD_LRS 이 속성을 사용하도록 설정한 경우 VMSS에 추가할 수 있습니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
확장 집합에서 가상 머신으로 업그레이드 모드를 지정했습니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 자동 번역
- 수동
- 롤링

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
VMSS에 대한 운영 체제 디스크를 저장하는 데 사용되는 컨테이너 URL을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
로컬 VMSS 개체를 지정합니다.
VMSS 개체를 얻으면 Get-AzVmss cmdlet을 사용합니다.
이 가상 머신 개체에는 VMSS에 대한 업데이트된 상태가 포함되어 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
이 cmdlet이 만드는 VMSS의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Boolean

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## 참고 사항

## 관련 링크

[Get-AzVmss](./Get-AzVmss.md)

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[다시 시작-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)


