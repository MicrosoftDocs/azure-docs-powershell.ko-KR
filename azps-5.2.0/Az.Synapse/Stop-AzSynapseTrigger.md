---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327410"
---
# <span data-ttu-id="1d17e-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="1d17e-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="1d17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d17e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d17e-103">작업 영역의 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="1d17e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d17e-104">SYNTAX</span></span>

### <span data-ttu-id="1d17e-105">StopByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d17e-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d17e-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="1d17e-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d17e-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d17e-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d17e-108">설명</span><span class="sxs-lookup"><span data-stu-id="1d17e-108">DESCRIPTION</span></span>
<span data-ttu-id="1d17e-109">**Stop-AzSynapseTrigger** cmdlet은 작업 영역의 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="1d17e-110">트리거가 '시작' 상태이면 cmdlet은 트리거를 중지하고 더 이상 파이프라인을 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="1d17e-111">트리거가 이미 '중지됨' 상태인 경우 이 cmdlet은 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="1d17e-112">예제</span><span class="sxs-lookup"><span data-stu-id="1d17e-112">EXAMPLES</span></span>

### <span data-ttu-id="1d17e-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d17e-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="1d17e-114">작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="1d17e-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="1d17e-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="1d17e-116">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="1d17e-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="1d17e-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="1d17e-118">파이프라인을 통해 작업 영역 ContosoWorkspace에서 ContosoTrigger라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="1d17e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d17e-119">PARAMETERS</span></span>

### <span data-ttu-id="1d17e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d17e-120">-AsJob</span></span>
<span data-ttu-id="1d17e-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1d17e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d17e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d17e-122">-DefaultProfile</span></span>
<span data-ttu-id="1d17e-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d17e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d17e-124">-InputObject</span></span>
<span data-ttu-id="1d17e-125">트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d17e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1d17e-126">-Name</span></span>
<span data-ttu-id="1d17e-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d17e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d17e-128">-PassThru</span></span>
<span data-ttu-id="1d17e-129">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1d17e-130">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1d17e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d17e-131">-WorkspaceName</span></span>
<span data-ttu-id="1d17e-132">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d17e-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1d17e-133">-WorkspaceObject</span></span>
<span data-ttu-id="1d17e-134">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d17e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d17e-135">-Confirm</span></span>
<span data-ttu-id="1d17e-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d17e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d17e-137">-WhatIf</span></span>
<span data-ttu-id="1d17e-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1d17e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d17e-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d17e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d17e-140">CommonParameters</span></span>
<span data-ttu-id="1d17e-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d17e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d17e-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d17e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d17e-143">입력</span><span class="sxs-lookup"><span data-stu-id="1d17e-143">INPUTS</span></span>

### <span data-ttu-id="1d17e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1d17e-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1d17e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span><span class="sxs-lookup"><span data-stu-id="1d17e-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="1d17e-146">출력</span><span class="sxs-lookup"><span data-stu-id="1d17e-146">OUTPUTS</span></span>

### <span data-ttu-id="1d17e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d17e-147">System.Boolean</span></span>

## <span data-ttu-id="1d17e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d17e-148">NOTES</span></span>

## <span data-ttu-id="1d17e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d17e-149">RELATED LINKS</span></span>