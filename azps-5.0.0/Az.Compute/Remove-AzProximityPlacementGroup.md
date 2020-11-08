---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 52804fab4cad0f0c0fcd56dd16a255daef626354
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218755"
---
# <span data-ttu-id="4a019-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4a019-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="4a019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a019-102">SYNOPSIS</span></span>
<span data-ttu-id="4a019-103">근접 배치 그룹 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="4a019-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a019-104">SYNTAX</span></span>

### <span data-ttu-id="4a019-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="4a019-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a019-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4a019-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a019-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4a019-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a019-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4a019-108">DESCRIPTION</span></span>
<span data-ttu-id="4a019-109">이 cmdlet은 근접 배치 그룹 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="4a019-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4a019-110">EXAMPLES</span></span>

### <span data-ttu-id="4a019-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4a019-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="4a019-112">이 명령은 지정 된 근접 배치 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-112">This command removes the given proximity placement group.</span></span>

### <span data-ttu-id="4a019-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4a019-113">Example 2</span></span>

<span data-ttu-id="4a019-114">이 명령은 지정 된 근접 배치 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-114">This command removes the given proximity placement group.</span></span> <span data-ttu-id="4a019-115">생성</span><span class="sxs-lookup"><span data-stu-id="4a019-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzProximityPlacementGroup -Name 'AgentPool01' -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="4a019-116">변수</span><span class="sxs-lookup"><span data-stu-id="4a019-116">PARAMETERS</span></span>

### <span data-ttu-id="4a019-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a019-117">-AsJob</span></span>
<span data-ttu-id="4a019-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4a019-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a019-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a019-119">-DefaultProfile</span></span>
<span data-ttu-id="4a019-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a019-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4a019-121">-Force</span></span>
<span data-ttu-id="4a019-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4a019-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a019-123">-InputObject</span></span>
<span data-ttu-id="4a019-124">PS 근사 배치 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="4a019-124">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a019-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4a019-125">-Name</span></span>
<span data-ttu-id="4a019-126">근접 배치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-126">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a019-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a019-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a019-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a019-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a019-129">-ResourceId</span></span>
<span data-ttu-id="4a019-130">근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-130">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="4a019-131">-확인</span><span class="sxs-lookup"><span data-stu-id="4a019-131">-Confirm</span></span>
<span data-ttu-id="4a019-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a019-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a019-133">-WhatIf</span></span>
<span data-ttu-id="4a019-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a019-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a019-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a019-136">CommonParameters</span></span>
<span data-ttu-id="4a019-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a019-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a019-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a019-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a019-139">입력</span><span class="sxs-lookup"><span data-stu-id="4a019-139">INPUTS</span></span>

### <span data-ttu-id="4a019-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a019-140">System.String</span></span>

### <span data-ttu-id="4a019-141">PSProximityPlacementGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="4a019-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="4a019-142">출력</span><span class="sxs-lookup"><span data-stu-id="4a019-142">OUTPUTS</span></span>

### <span data-ttu-id="4a019-143">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="4a019-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4a019-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4a019-144">NOTES</span></span>

## <span data-ttu-id="4a019-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a019-145">RELATED LINKS</span></span>