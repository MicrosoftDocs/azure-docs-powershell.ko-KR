---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332222"
---
# <span data-ttu-id="6eacf-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eacf-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="6eacf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eacf-102">SYNOPSIS</span></span>
<span data-ttu-id="6eacf-103">Front Door 부하 균형 조정기 제거</span><span class="sxs-lookup"><span data-stu-id="6eacf-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="6eacf-104">구문</span><span class="sxs-lookup"><span data-stu-id="6eacf-104">SYNTAX</span></span>

### <span data-ttu-id="6eacf-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6eacf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eacf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eacf-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eacf-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eacf-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eacf-108">설명</span><span class="sxs-lookup"><span data-stu-id="6eacf-108">DESCRIPTION</span></span>
<span data-ttu-id="6eacf-109">**Remove-AzFrontDoor** cmdlet은 현재 구독에서 Front Door 부하 균형 조정기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="6eacf-110">예제</span><span class="sxs-lookup"><span data-stu-id="6eacf-110">EXAMPLES</span></span>

### <span data-ttu-id="6eacf-111">예제 1: 현재 구독의 리소스 그룹 "rg1"에서 "frontdoor1"을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="6eacf-112">현재 구독의 리소스 그룹 "rg1"에서 "frontdoor1"을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="6eacf-113">예제 2: 현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="6eacf-114">현재 구독에서 리소스 그룹 "rg1"의 모든 FrontDoors를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="6eacf-115">예제 3: 현재 구독에서 모든 FrontDoors를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="6eacf-116">현재 구독에서 모든 FrontDoors를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="6eacf-117">예제 4: 현재 구독에서 이름이 "frontdoor1"인 모든 FrontDoors를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="6eacf-118">현재 구독에서 이름이 "frontdoor1"인 모든 FrontDoors를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="6eacf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eacf-119">PARAMETERS</span></span>

### <span data-ttu-id="6eacf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eacf-120">-DefaultProfile</span></span>
<span data-ttu-id="6eacf-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eacf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eacf-122">-InputObject</span></span>
<span data-ttu-id="6eacf-123">삭제할 Front Door 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6eacf-124">-Name</span></span>
<span data-ttu-id="6eacf-125">삭제할 Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-125">The name of the Front Door to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eacf-126">-PassThru</span></span>
<span data-ttu-id="6eacf-127">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="6eacf-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="6eacf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eacf-128">-ResourceGroupName</span></span>
<span data-ttu-id="6eacf-129">Front Door가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-129">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eacf-130">-ResourceId</span></span>
<span data-ttu-id="6eacf-131">삭제할 Front Door의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6eacf-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eacf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eacf-132">-Confirm</span></span>
<span data-ttu-id="6eacf-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eacf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eacf-134">-WhatIf</span></span>
<span data-ttu-id="6eacf-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6eacf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eacf-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eacf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eacf-137">CommonParameters</span></span>
<span data-ttu-id="6eacf-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6eacf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eacf-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6eacf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eacf-140">입력</span><span class="sxs-lookup"><span data-stu-id="6eacf-140">INPUTS</span></span>

### <span data-ttu-id="6eacf-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6eacf-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="6eacf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6eacf-142">System.String</span></span>

## <span data-ttu-id="6eacf-143">출력</span><span class="sxs-lookup"><span data-stu-id="6eacf-143">OUTPUTS</span></span>

### <span data-ttu-id="6eacf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6eacf-144">System.Boolean</span></span>

## <span data-ttu-id="6eacf-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6eacf-145">NOTES</span></span>

## <span data-ttu-id="6eacf-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eacf-146">RELATED LINKS</span></span>

<span data-ttu-id="6eacf-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6eacf-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>