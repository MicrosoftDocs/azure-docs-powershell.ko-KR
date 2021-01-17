---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370763"
---
# <span data-ttu-id="a1a19-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1a19-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="a1a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1a19-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a19-103">VMSS에 네트워크 인터페이스 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="a1a19-104">구문</span><span class="sxs-lookup"><span data-stu-id="a1a19-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1a19-105">설명</span><span class="sxs-lookup"><span data-stu-id="a1a19-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a19-106">**Add-AzVmssNetworkInterfaceConfiguration** cmdlet은 VMSS(Virtual Machine Scale Set)에 네트워크 인터페이스 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a1a19-107">예제</span><span class="sxs-lookup"><span data-stu-id="a1a19-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a19-108">예제 1: VMSS에 네트워크 인터페이스 구성 추가</span><span class="sxs-lookup"><span data-stu-id="a1a19-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="a1a19-109">이 명령은 VMSS에 네트워크 인터페이스 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="a1a19-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1a19-110">PARAMETERS</span></span>

### <span data-ttu-id="a1a19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a19-111">-DefaultProfile</span></span>
<span data-ttu-id="a1a19-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a19-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="a1a19-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="a1a19-114">DNS 설정에 대한 DNS 서버 IP 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a19-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="a1a19-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="a1a19-116">네트워크 인터페이스가 가속화된 네트워킹을 사용할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="a1a19-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="a1a19-117">-EnableIPForwarding</span></span>
<span data-ttu-id="a1a19-118">이 NIC에서 IP 전달을 사용하도록 설정하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="a1a19-119">-Id</span><span class="sxs-lookup"><span data-stu-id="a1a19-119">-Id</span></span>
<span data-ttu-id="a1a19-120">가상 머신의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a19-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1a19-121">-IpConfiguration</span></span>
<span data-ttu-id="a1a19-122">네트워크 인터페이스의 IP 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a19-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a1a19-123">-Name</span></span>
<span data-ttu-id="a1a19-124">네트워크 인터페이스 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a19-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1a19-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a1a19-126">네트워크 보안 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="a1a19-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="a1a19-127">-Primary</span></span>
<span data-ttu-id="a1a19-128">네트워크 인터페이스 구성에서 만든 네트워크 인터페이스가 가상 머신의 기본 NIC(네트워크 정보 센터)가 될지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a19-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1a19-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a1a19-130">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="a1a19-131">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a19-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1a19-132">-Confirm</span></span>
<span data-ttu-id="a1a19-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a19-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a19-134">-WhatIf</span></span>
<span data-ttu-id="a1a19-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a1a19-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1a19-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a19-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a19-137">CommonParameters</span></span>
<span data-ttu-id="a1a19-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a1a19-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a19-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1a19-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a19-140">입력</span><span class="sxs-lookup"><span data-stu-id="a1a19-140">INPUTS</span></span>

### <span data-ttu-id="a1a19-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1a19-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a1a19-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a1a19-142">System.String</span></span>

### <span data-ttu-id="a1a19-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1a19-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a1a19-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a1a19-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="a1a19-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a1a19-145">System.String[]</span></span>

## <span data-ttu-id="a1a19-146">출력</span><span class="sxs-lookup"><span data-stu-id="a1a19-146">OUTPUTS</span></span>

### <span data-ttu-id="a1a19-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1a19-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a1a19-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a1a19-148">NOTES</span></span>

## <span data-ttu-id="a1a19-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1a19-149">RELATED LINKS</span></span>

[<span data-ttu-id="a1a19-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a1a19-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)