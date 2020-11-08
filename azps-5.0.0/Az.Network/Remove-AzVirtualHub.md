---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHub.md
ms.openlocfilehash: 116cffabc942572db48d6f86b469a954bccbc1c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218100"
---
# <span data-ttu-id="e419b-101">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e419b-101">Remove-AzVirtualHub</span></span>

## <span data-ttu-id="e419b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e419b-102">SYNOPSIS</span></span>
<span data-ttu-id="e419b-103">Azure VirtualHub 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-103">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e419b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e419b-104">SYNTAX</span></span>

### <span data-ttu-id="e419b-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e419b-105">ByVirtualHubName (Default)</span></span>
```
Remove-AzVirtualHub -ResourceGroupName <String> -Name <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e419b-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e419b-106">ByVirtualHubResourceId</span></span>
```
Remove-AzVirtualHub -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e419b-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e419b-107">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHub -InputObject <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e419b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e419b-108">DESCRIPTION</span></span>
<span data-ttu-id="e419b-109">Azure VirtualHub 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-109">Removes an Azure VirtualHub resource.</span></span>

## <span data-ttu-id="e419b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e419b-110">EXAMPLES</span></span>

### <span data-ttu-id="e419b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e419b-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="e419b-112">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-112">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e419b-113">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-113">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e419b-114">그런 다음 해당 ResourceGroupName 및 Context.resourcename을 사용 하 여 가상 허브를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-114">It then deletes the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="e419b-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="e419b-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Remove-AzVirtualHub -InputObject $virtualHub
```

<span data-ttu-id="e419b-116">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-116">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e419b-117">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-117">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e419b-118">그런 다음 입력 개체를 사용 하 여 가상 허브를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-118">It then deletes the virtual hub using an input object.</span></span> <span data-ttu-id="e419b-119">입력 개체는 PSVirtualHub 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-119">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="e419b-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="e419b-120">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Remove-AzVirtualHub
```

<span data-ttu-id="e419b-121">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-121">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="e419b-122">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-122">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="e419b-123">그런 다음 AzVirtualHub의 출력을 사용 하 여 powershell 파이핑을 사용 하 여 가상 허브를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-123">It then deletes the virtual hub using powershell piping using output from Get-AzVirtualHub.</span></span>

## <span data-ttu-id="e419b-124">변수</span><span class="sxs-lookup"><span data-stu-id="e419b-124">PARAMETERS</span></span>

### <span data-ttu-id="e419b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e419b-125">-AsJob</span></span>
<span data-ttu-id="e419b-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e419b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e419b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e419b-127">-DefaultProfile</span></span>
<span data-ttu-id="e419b-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e419b-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e419b-129">-Force</span></span>
<span data-ttu-id="e419b-130">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e419b-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e419b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e419b-131">-InputObject</span></span>
<span data-ttu-id="e419b-132">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-132">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e419b-133">-이름</span><span class="sxs-lookup"><span data-stu-id="e419b-133">-Name</span></span>
<span data-ttu-id="e419b-134">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-134">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e419b-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e419b-135">-PassThru</span></span>
<span data-ttu-id="e419b-136">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-136">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e419b-137">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-137">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e419b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e419b-138">-ResourceGroupName</span></span>
<span data-ttu-id="e419b-139">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e419b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e419b-140">-ResourceId</span></span>
<span data-ttu-id="e419b-141">수정할 가상 허브의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-141">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e419b-142">-확인</span><span class="sxs-lookup"><span data-stu-id="e419b-142">-Confirm</span></span>
<span data-ttu-id="e419b-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e419b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e419b-144">-WhatIf</span></span>
<span data-ttu-id="e419b-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e419b-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e419b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e419b-147">CommonParameters</span></span>
<span data-ttu-id="e419b-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e419b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e419b-149">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e419b-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e419b-150">입력</span><span class="sxs-lookup"><span data-stu-id="e419b-150">INPUTS</span></span>

### <span data-ttu-id="e419b-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e419b-151">System.String</span></span>

### <span data-ttu-id="e419b-152">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e419b-152">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e419b-153">출력</span><span class="sxs-lookup"><span data-stu-id="e419b-153">OUTPUTS</span></span>

### <span data-ttu-id="e419b-154">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e419b-154">System.Boolean</span></span>

## <span data-ttu-id="e419b-155">상속자</span><span class="sxs-lookup"><span data-stu-id="e419b-155">NOTES</span></span>

## <span data-ttu-id="e419b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e419b-156">RELATED LINKS</span></span>

[<span data-ttu-id="e419b-157">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e419b-157">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)

[<span data-ttu-id="e419b-158">새로운 AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e419b-158">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="e419b-159">업데이트-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e419b-159">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)