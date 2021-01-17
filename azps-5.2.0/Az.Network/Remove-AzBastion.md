---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327459"
---
# <span data-ttu-id="a012c-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="a012c-101">Remove-AzBastion</span></span>

## <span data-ttu-id="a012c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a012c-102">SYNOPSIS</span></span>
<span data-ttu-id="a012c-103">배스션 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="a012c-104">구문</span><span class="sxs-lookup"><span data-stu-id="a012c-104">SYNTAX</span></span>

### <span data-ttu-id="a012c-105">ByResourceGroupName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a012c-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a012c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a012c-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a012c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a012c-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a012c-108">설명</span><span class="sxs-lookup"><span data-stu-id="a012c-108">DESCRIPTION</span></span>
<span data-ttu-id="a012c-109">배스션 리소스를 제거합니다. Example1은 ResourceGroupName 및 ResourceName을 사용하여 bastion을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="a012c-110">Example2는 파이프라인과 함께 해당 개체를 사용하여 bastion을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="a012c-111">Example3은 해당 개체를 사용하여 bastion을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="a012c-112">예제</span><span class="sxs-lookup"><span data-stu-id="a012c-112">EXAMPLES</span></span>

### <span data-ttu-id="a012c-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a012c-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="a012c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a012c-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="a012c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="a012c-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="a012c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a012c-116">PARAMETERS</span></span>

### <span data-ttu-id="a012c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a012c-117">-Confirm</span></span>
<span data-ttu-id="a012c-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a012c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a012c-119">-DefaultProfile</span></span>
<span data-ttu-id="a012c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a012c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a012c-121">-Force</span></span>
<span data-ttu-id="a012c-122">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a012c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a012c-123">-InputObject</span></span>
<span data-ttu-id="a012c-124">삭제할 Bastion 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a012c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a012c-125">-Name</span></span>
<span data-ttu-id="a012c-126">삭제할 배스션 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a012c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a012c-127">-PassThru</span></span>
<span data-ttu-id="a012c-128">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a012c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a012c-129">-ResourceGroupName</span></span>
<span data-ttu-id="a012c-130">bastion이 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a012c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a012c-131">-ResourceId</span></span>
<span data-ttu-id="a012c-132">삭제할 Bastion에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a012c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a012c-133">-WhatIf</span></span>
<span data-ttu-id="a012c-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a012c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a012c-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a012c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a012c-136">CommonParameters</span></span>
<span data-ttu-id="a012c-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a012c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a012c-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a012c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a012c-139">입력</span><span class="sxs-lookup"><span data-stu-id="a012c-139">INPUTS</span></span>

### <span data-ttu-id="a012c-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="a012c-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="a012c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a012c-141">System.String</span></span>

## <span data-ttu-id="a012c-142">출력</span><span class="sxs-lookup"><span data-stu-id="a012c-142">OUTPUTS</span></span>

### <span data-ttu-id="a012c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a012c-143">System.Boolean</span></span>

## <span data-ttu-id="a012c-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a012c-144">NOTES</span></span>

## <span data-ttu-id="a012c-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a012c-145">RELATED LINKS</span></span>
[<span data-ttu-id="a012c-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="a012c-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="a012c-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="a012c-147">New-AzBastion</span></span>](./New-AzBastion.md)