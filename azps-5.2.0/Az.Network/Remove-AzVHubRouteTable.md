---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324050"
---
# <span data-ttu-id="536a9-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="536a9-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="536a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="536a9-102">SYNOPSIS</span></span>
<span data-ttu-id="536a9-103">VirtualHub와 연결된 허브 경로 테이블 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="536a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="536a9-104">SYNTAX</span></span>

### <span data-ttu-id="536a9-105">ByVHubRouteTableName(기본값)</span><span class="sxs-lookup"><span data-stu-id="536a9-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="536a9-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="536a9-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="536a9-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="536a9-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="536a9-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="536a9-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="536a9-109">설명</span><span class="sxs-lookup"><span data-stu-id="536a9-109">DESCRIPTION</span></span>
<span data-ttu-id="536a9-110">지정된 가상 허브와 연결된 지정된 허브 경로 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="536a9-111">예제</span><span class="sxs-lookup"><span data-stu-id="536a9-111">EXAMPLES</span></span>

### <span data-ttu-id="536a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="536a9-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="536a9-113">이 명령은 가상 허브의 허브 경로 테이블을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="536a9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="536a9-114">PARAMETERS</span></span>

### <span data-ttu-id="536a9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="536a9-115">-AsJob</span></span>
<span data-ttu-id="536a9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="536a9-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="536a9-117">-DefaultProfile</span></span>
<span data-ttu-id="536a9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="536a9-119">-Force</span></span>
<span data-ttu-id="536a9-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="536a9-121">-InputObject</span></span>
<span data-ttu-id="536a9-122">제거할 vhubroutetable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="536a9-123">-Name</span></span>
<span data-ttu-id="536a9-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="536a9-125">-ParentObject</span></span>
<span data-ttu-id="536a9-126">이 리소스의 부모 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="536a9-127">-ParentResourceName</span></span>
<span data-ttu-id="536a9-128">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="536a9-129">-PassThru</span></span>
<span data-ttu-id="536a9-130">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-130">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="536a9-131">-ResourceGroupName</span></span>
<span data-ttu-id="536a9-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="536a9-133">-ResourceId</span></span>
<span data-ttu-id="536a9-134">제거할 vhubroutetable 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="536a9-135">-Confirm</span></span>
<span data-ttu-id="536a9-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="536a9-137">-WhatIf</span></span>
<span data-ttu-id="536a9-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="536a9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="536a9-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="536a9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="536a9-140">CommonParameters</span></span>
<span data-ttu-id="536a9-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="536a9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="536a9-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="536a9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="536a9-143">입력</span><span class="sxs-lookup"><span data-stu-id="536a9-143">INPUTS</span></span>

### <span data-ttu-id="536a9-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="536a9-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="536a9-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="536a9-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="536a9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="536a9-146">System.String</span></span>

## <span data-ttu-id="536a9-147">출력</span><span class="sxs-lookup"><span data-stu-id="536a9-147">OUTPUTS</span></span>

### <span data-ttu-id="536a9-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="536a9-148">System.Boolean</span></span>

## <span data-ttu-id="536a9-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="536a9-149">NOTES</span></span>

## <span data-ttu-id="536a9-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="536a9-150">RELATED LINKS</span></span>

[<span data-ttu-id="536a9-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="536a9-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="536a9-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="536a9-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="536a9-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="536a9-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="536a9-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="536a9-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)