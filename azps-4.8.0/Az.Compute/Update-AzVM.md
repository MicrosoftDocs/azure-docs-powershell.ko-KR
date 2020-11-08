---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214211"
---
# <span data-ttu-id="8bc5d-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-101">Update-AzVM</span></span>

## <span data-ttu-id="8bc5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc5d-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc5d-103">Azure 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="8bc5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8bc5d-104">SYNTAX</span></span>

### <span data-ttu-id="8bc5d-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8bc5d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc5d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bc5d-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc5d-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8bc5d-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc5d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8bc5d-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc5d-109">**업데이트 AzVM** Cmdlet은 Azure 가상 컴퓨터의 상태를 가상 컴퓨터 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="8bc5d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8bc5d-110">EXAMPLES</span></span>

### <span data-ttu-id="8bc5d-111">예제 1: 가상 컴퓨터 업데이트</span><span class="sxs-lookup"><span data-stu-id="8bc5d-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="8bc5d-112">이 명령은 ResourceGroup11에서 가상 머신 ($VirtualMachine)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="8bc5d-113">이 명령은 $VirtualMachine 변수에 저장 된 가상 컴퓨터 개체를 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8bc5d-114">가상 컴퓨터 개체를 가져오려면 **AzVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="8bc5d-115">변수</span><span class="sxs-lookup"><span data-stu-id="8bc5d-115">PARAMETERS</span></span>

### <span data-ttu-id="8bc5d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bc5d-116">-AsJob</span></span>
<span data-ttu-id="8bc5d-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8bc5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc5d-118">-DefaultProfile</span></span>
<span data-ttu-id="8bc5d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc5d-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="8bc5d-120">-HostId</span></span>
<span data-ttu-id="8bc5d-121">호스트의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-121">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc5d-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="8bc5d-122">-EncryptionAtHost</span></span>
<span data-ttu-id="8bc5d-123">EncryptionAtHost 속성은 사용자가 가상 컴퓨터 또는 가상 컴퓨터 크기 집합에 대 한 호스트 암호화를 사용 하거나 사용 하지 않도록 요청할 때 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="8bc5d-124">이렇게 하면 호스트 자체의 리소스/임시 디스크를 포함 하 여 모든 디스크에 대 한 암호화가 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc5d-125">-Id</span><span class="sxs-lookup"><span data-stu-id="8bc5d-125">-Id</span></span>
<span data-ttu-id="8bc5d-126">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc5d-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="8bc5d-127">-IdentityId</span></span>
<span data-ttu-id="8bc5d-128">가상 컴퓨터와 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="8bc5d-129">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 Id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="8bc5d-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8bc5d-130">-IdentityType</span></span>
<span data-ttu-id="8bc5d-131">가상 컴퓨터에 사용 되는 id 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="8bc5d-132">유효한 값은 SystemAssigned, UserAssigned, SystemAssignedUserAssigned 및 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="8bc5d-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="8bc5d-133">-MaxPrice</span></span>
<span data-ttu-id="8bc5d-134">우선 순위가 낮은 VM/VMSS에 대해 지불할 최대 가격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="8bc5d-135">이 가격은 미국 달러입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-135">This price is in US Dollars.</span></span> <span data-ttu-id="8bc5d-136">이 가격은 VM 크기에 대 한 현재의 낮은 우선 순위 가격과 비교 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="8bc5d-137">또한 우선 순위가 낮은 VM/VMSS의 생성/업데이트가 수행 될 때 가격이 비교 되 고 maxPrice가 현재 낮은 우선 순위의 가격 보다 더 큰 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="8bc5d-138">MaxPrice는 VM/VMSS를 만든 후 현재 낮은 우선 순위의 가격이 maxPrice를 초과 하는 경우 우선 순위가 낮은 VM/VMSS를 제거 하는 데도 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="8bc5d-139">가능한 값은 다음과 같습니다. 0 보다 큰 10 진수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="8bc5d-140">예: 0.01538.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-140">Example: 0.01538.</span></span>  <span data-ttu-id="8bc5d-141">-1은 낮은 우선 순위의 VM/VMSS가 가격 이유로 제거 되어서는 안 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="8bc5d-142">또한 기본 최대 가격은 사용자가 제공 하지 않는 경우-1입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-142">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc5d-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8bc5d-143">-NoWait</span></span>
<span data-ttu-id="8bc5d-144">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8bc5d-145">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8bc5d-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8bc5d-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="8bc5d-147">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="8bc5d-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="8bc5d-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="8bc5d-149">이 가상 컴퓨터에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="8bc5d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc5d-150">-ResourceGroupName</span></span>
<span data-ttu-id="8bc5d-151">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc5d-152">태그</span><span class="sxs-lookup"><span data-stu-id="8bc5d-152">-Tag</span></span>
<span data-ttu-id="8bc5d-153">이름-값 쌍 집합을 사용 하 여 리소스 및 리소스 그룹에 태그를 지정할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="8bc5d-154">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="8bc5d-155">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="8bc5d-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="8bc5d-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="8bc5d-157">VM에서 저장소 계정 유형이 UltraSSD_LRS 하나 이상의 관리 되는 데이터 디스크를 포함 하는 기능을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="8bc5d-158">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="8bc5d-159">-VM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-159">-VM</span></span>
<span data-ttu-id="8bc5d-160">로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="8bc5d-161">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="8bc5d-162">이 가상 컴퓨터 개체에는 가상 컴퓨터에 대 한 업데이트 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc5d-163">-확인</span><span class="sxs-lookup"><span data-stu-id="8bc5d-163">-Confirm</span></span>
<span data-ttu-id="8bc5d-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc5d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc5d-165">-WhatIf</span></span>
<span data-ttu-id="8bc5d-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc5d-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="8bc5d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc5d-168">CommonParameters</span></span>
<span data-ttu-id="8bc5d-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc5d-170">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc5d-171">입력</span><span class="sxs-lookup"><span data-stu-id="8bc5d-171">INPUTS</span></span>

### <span data-ttu-id="8bc5d-172">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8bc5d-172">System.String</span></span>

### <span data-ttu-id="8bc5d-173">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8bc5d-174">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8bc5d-174">System.Boolean</span></span>

## <span data-ttu-id="8bc5d-175">출력</span><span class="sxs-lookup"><span data-stu-id="8bc5d-175">OUTPUTS</span></span>

### <span data-ttu-id="8bc5d-176">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="8bc5d-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8bc5d-177">상속자</span><span class="sxs-lookup"><span data-stu-id="8bc5d-177">NOTES</span></span>

## <span data-ttu-id="8bc5d-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bc5d-178">RELATED LINKS</span></span>

[<span data-ttu-id="8bc5d-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8bc5d-180">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8bc5d-181">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8bc5d-182">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8bc5d-183">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8bc5d-184">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="8bc5d-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="8bc5d-185">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8bc5d-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

