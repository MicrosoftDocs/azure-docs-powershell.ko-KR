---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042101"
---
# <span data-ttu-id="40f1e-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="40f1e-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="40f1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="40f1e-103">수동 플랫폼 업데이트 도메인 워크에서 서비스 패브릭 가상 컴퓨터 크기 조정 집합의 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="40f1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40f1e-104">SYNTAX</span></span>

### <span data-ttu-id="40f1e-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="40f1e-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40f1e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="40f1e-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40f1e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="40f1e-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40f1e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="40f1e-108">DESCRIPTION</span></span>
<span data-ttu-id="40f1e-109">수동 플랫폼 업데이트 도메인 워크를 강제로 실행 하 여 서비스 패브릭 가상 머신 크기 조정 집합의 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="40f1e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="40f1e-110">EXAMPLES</span></span>

### <span data-ttu-id="40f1e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="40f1e-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="40f1e-112">이 명령은 리소스 그룹 이름 및 크기 조정 집합 이름에 지정 된 가상 컴퓨터 크기 조정 집합에 대해 UD 0에서 서비스 패브릭 업데이트 워크를 강제로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="40f1e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="40f1e-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="40f1e-114">이 명령은 VM scale set 개체에 지정 된 가상 컴퓨터 배율 집합에 대해 UD 1의 서비스 패브릭 업데이트 워크를 강제로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="40f1e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="40f1e-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="40f1e-116">이 명령은 리소스 id로 지정 된 가상 컴퓨터 크기 조정 집합에 대해 UD 2의 서비스 패브릭 업데이트 워크를 강제로 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="40f1e-117">변수</span><span class="sxs-lookup"><span data-stu-id="40f1e-117">PARAMETERS</span></span>

### <span data-ttu-id="40f1e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40f1e-118">-AsJob</span></span>
<span data-ttu-id="40f1e-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="40f1e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40f1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f1e-120">-DefaultProfile</span></span>
<span data-ttu-id="40f1e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f1e-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="40f1e-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="40f1e-123">수동 복구 워크가 요청 된 플랫폼 업데이트 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f1e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f1e-124">-ResourceGroupName</span></span>
<span data-ttu-id="40f1e-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f1e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40f1e-126">-ResourceId</span></span>
<span data-ttu-id="40f1e-127">가상 컴퓨터 크기 집합에 대 한 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f1e-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="40f1e-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="40f1e-129">로컬 가상 컴퓨터 확장 집합 개체</span><span class="sxs-lookup"><span data-stu-id="40f1e-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40f1e-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="40f1e-130">-VMScaleSetName</span></span>
<span data-ttu-id="40f1e-131">가상 머신 크기 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40f1e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="40f1e-132">-Confirm</span></span>
<span data-ttu-id="40f1e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f1e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f1e-134">-WhatIf</span></span>
<span data-ttu-id="40f1e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f1e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f1e-137">CommonParameters</span></span>
<span data-ttu-id="40f1e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f1e-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40f1e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f1e-140">입력</span><span class="sxs-lookup"><span data-stu-id="40f1e-140">INPUTS</span></span>

### <span data-ttu-id="40f1e-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40f1e-141">System.String</span></span>

### <span data-ttu-id="40f1e-142">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="40f1e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="40f1e-143">출력</span><span class="sxs-lookup"><span data-stu-id="40f1e-143">OUTPUTS</span></span>

### <span data-ttu-id="40f1e-144">PSRecoveryWalkResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="40f1e-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="40f1e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="40f1e-145">NOTES</span></span>

## <span data-ttu-id="40f1e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40f1e-146">RELATED LINKS</span></span>