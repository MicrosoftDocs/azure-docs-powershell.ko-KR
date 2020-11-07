---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: d1ec777d6574aa34a6b19fa7cdc94d9c349dbc48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869653"
---
# <span data-ttu-id="157e5-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="157e5-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="157e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="157e5-102">SYNOPSIS</span></span>
<span data-ttu-id="157e5-103">Azure 가상 WAN을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="157e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="157e5-104">SYNTAX</span></span>

### <span data-ttu-id="157e5-105">ByVirtualWanName (기본값)</span><span class="sxs-lookup"><span data-stu-id="157e5-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="157e5-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="157e5-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="157e5-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="157e5-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="157e5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="157e5-108">DESCRIPTION</span></span>
<span data-ttu-id="157e5-109">Azure 가상 WAN을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="157e5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="157e5-110">EXAMPLES</span></span>

### <span data-ttu-id="157e5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="157e5-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="157e5-112">이 예제에서는 리소스 그룹에 가상 WAN을 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="157e5-113">가상 WAN을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="157e5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="157e5-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="157e5-115">이 예제에서는 리소스 그룹에 가상 WAN을 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="157e5-116">이 삭제는 New-AzVirtualWan에서 반환 된 가상 wan 개체를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="157e5-117">가상 WAN을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="157e5-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="157e5-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="157e5-119">이 예제에서는 리소스 그룹에 가상 WAN을 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="157e5-120">이 삭제는 New-AzVirtualWan에서 반환 된 가상 wan 리소스 id를 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="157e5-121">가상 WAN을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="157e5-122">변수</span><span class="sxs-lookup"><span data-stu-id="157e5-122">PARAMETERS</span></span>

### <span data-ttu-id="157e5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157e5-123">-DefaultProfile</span></span>
<span data-ttu-id="157e5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="157e5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="157e5-125">-Force</span></span>
<span data-ttu-id="157e5-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="157e5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="157e5-127">-InputObject</span></span>
<span data-ttu-id="157e5-128">삭제할 가상 wan 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="157e5-129">-이름</span><span class="sxs-lookup"><span data-stu-id="157e5-129">-Name</span></span>
<span data-ttu-id="157e5-130">가상 wan 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157e5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="157e5-131">-PassThru</span></span>
<span data-ttu-id="157e5-132">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="157e5-133">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="157e5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157e5-134">-ResourceGroupName</span></span>
<span data-ttu-id="157e5-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157e5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="157e5-136">-ResourceId</span></span>
<span data-ttu-id="157e5-137">삭제할 가상 wan의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157e5-138">-확인</span><span class="sxs-lookup"><span data-stu-id="157e5-138">-Confirm</span></span>
<span data-ttu-id="157e5-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="157e5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="157e5-140">-WhatIf</span></span>
<span data-ttu-id="157e5-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="157e5-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="157e5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157e5-143">CommonParameters</span></span>
<span data-ttu-id="157e5-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="157e5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157e5-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157e5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157e5-146">입력</span><span class="sxs-lookup"><span data-stu-id="157e5-146">INPUTS</span></span>

### <span data-ttu-id="157e5-147">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="157e5-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="157e5-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="157e5-148">System.String</span></span>

## <span data-ttu-id="157e5-149">출력</span><span class="sxs-lookup"><span data-stu-id="157e5-149">OUTPUTS</span></span>

### <span data-ttu-id="157e5-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="157e5-150">System.Boolean</span></span>

## <span data-ttu-id="157e5-151">상속자</span><span class="sxs-lookup"><span data-stu-id="157e5-151">NOTES</span></span>

## <span data-ttu-id="157e5-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="157e5-152">RELATED LINKS</span></span>

[<span data-ttu-id="157e5-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="157e5-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="157e5-154">새로운 AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="157e5-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="157e5-155">업데이트-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="157e5-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)