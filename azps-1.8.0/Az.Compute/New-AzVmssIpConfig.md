---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: acb4496cc9413d6b056b56fe4dbb80a99dee0706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869001"
---
# <span data-ttu-id="6f120-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f120-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="6f120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f120-102">SYNOPSIS</span></span>
<span data-ttu-id="6f120-103">VMSS의 네트워크 인터페이스에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="6f120-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f120-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f120-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f120-105">DESCRIPTION</span></span>
<span data-ttu-id="6f120-106">**AzVmssIpConfig** CMDLET은 Vmss (가상 컴퓨터 확장 집합)의 네트워크 인터페이스에 대 한 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6f120-107">이 cmdlet의 구성을 Add-AzVmssNetworkInterfaceConfiguration cmdlet의 *IPConfiguration* 매개 변수로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="6f120-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6f120-108">EXAMPLES</span></span>

### <span data-ttu-id="6f120-109">예제 1: VMSS 인터페이스에 대 한 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6f120-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="6f120-110">이 명령은 ContosoVmssInterface02 이라는 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="6f120-111">이 명령은 $SubnetId에 저장 되어 있는 이전에 정의 된 서브넷 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="6f120-112">명령은 나중에 **AzVmssNetworkInterfaceConfiguration 추가** 를 사용 하기 위해 $IPConfiguration 변수에 구성 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="6f120-113">예제 2: NAT 풀 설정을 포함 하는 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="6f120-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="6f120-114">이 명령은 ContosoVmssInterface03 이라는 IP 구성 개체를 만든 다음 나중에 사용 하기 위해이를 $IPConfiguration 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="6f120-115">이 명령은 $SubnetId에 저장 되어 있는 이전에 정의 된 서브넷 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="6f120-116">명령은 나중에 사용 하기 위해 $IPConfiguration 변수의 구성 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="6f120-117">명령에서 *LoadBalancerInboundNatPoolsId* 및 *LoadBalancerBackendAddressPoolsId* 매개 변수에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="6f120-118">변수</span><span class="sxs-lookup"><span data-stu-id="6f120-118">PARAMETERS</span></span>

### <span data-ttu-id="6f120-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="6f120-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="6f120-120">부하 분산 장치의 백 엔드 주소 풀에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="6f120-121">확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 백엔드 주소 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="6f120-122">여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f120-123">-DefaultProfile</span></span>
<span data-ttu-id="6f120-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f120-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="6f120-125">-DnsSetting</span></span>
<span data-ttu-id="6f120-126">PublicIP 주소에 적용 되는 dns 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="6f120-127">PublicIP 주소에 적용 될 Dns 설정의 도메인 이름 레이블</span><span class="sxs-lookup"><span data-stu-id="6f120-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="6f120-128">도메인 이름 레이블과 vm 인덱스의 연결은 만들 공용 IP 주소 리소스의 도메인 이름 레이블이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-129">-Id</span><span class="sxs-lookup"><span data-stu-id="6f120-129">-Id</span></span>
<span data-ttu-id="6f120-130">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="6f120-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="6f120-131">-IpTag</span></span>
<span data-ttu-id="6f120-132">Ip 태그 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="6f120-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="6f120-134">부하 분산 장치의 들어오는 NAT (network address translation) 풀에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="6f120-135">확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 들어오는 NAT 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="6f120-136">여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="6f120-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="6f120-138">부하 분산 장치의 들어오는 NAT 풀에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="6f120-139">확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 들어오는 NAT 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="6f120-140">여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-141">-이름</span><span class="sxs-lookup"><span data-stu-id="6f120-141">-Name</span></span>
<span data-ttu-id="6f120-142">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-143">-기본</span><span class="sxs-lookup"><span data-stu-id="6f120-143">-Primary</span></span>
<span data-ttu-id="6f120-144">네트워크 인터페이스에 둘 이상의 IP 구성이 있는 경우 기본 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="6f120-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6f120-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="6f120-146">Ip 구성을 IPv4 또는 IPv6 중 하나로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="6f120-147">기본값은 IPv4로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="6f120-148">사용할 수 있는 값은 ' IPv4 ' 및 ' IPv6 '입니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="6f120-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6f120-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="6f120-150">공용 IP 주소의 유휴 시간 제한</span><span class="sxs-lookup"><span data-stu-id="6f120-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6f120-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="6f120-152">PublicIP 주소 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="6f120-153">-PublicIPPrefix</span></span>
<span data-ttu-id="6f120-154">공용 IP 접두사의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="6f120-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6f120-155">-SubnetId</span></span>
<span data-ttu-id="6f120-156">구성에서 VMSS 네트워크 인터페이스를 만드는 서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f120-157">-확인</span><span class="sxs-lookup"><span data-stu-id="6f120-157">-Confirm</span></span>
<span data-ttu-id="6f120-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f120-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f120-159">-WhatIf</span></span>
<span data-ttu-id="6f120-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f120-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f120-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f120-162">CommonParameters</span></span>
<span data-ttu-id="6f120-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f120-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f120-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f120-165">입력</span><span class="sxs-lookup"><span data-stu-id="6f120-165">INPUTS</span></span>

### <span data-ttu-id="6f120-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f120-166">System.String</span></span>

### <span data-ttu-id="6f120-167">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="6f120-167">System.String[]</span></span>

### <span data-ttu-id="6f120-168">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="6f120-168">System.Int32</span></span>

### <span data-ttu-id="6f120-169">Microsoft VirtualMachineScaleSetIpTag []을 (를)</span><span class="sxs-lookup"><span data-stu-id="6f120-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="6f120-170">출력</span><span class="sxs-lookup"><span data-stu-id="6f120-170">OUTPUTS</span></span>

### <span data-ttu-id="6f120-171">VirtualMachineScaleSetIPConfiguration를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f120-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="6f120-172">상속자</span><span class="sxs-lookup"><span data-stu-id="6f120-172">NOTES</span></span>

## <span data-ttu-id="6f120-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f120-173">RELATED LINKS</span></span>

[<span data-ttu-id="6f120-174">추가-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f120-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

