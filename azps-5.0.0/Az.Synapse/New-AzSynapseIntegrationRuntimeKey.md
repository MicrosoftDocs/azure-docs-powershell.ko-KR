---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217934"
---
# <span data-ttu-id="7f367-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="7f367-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="7f367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f367-102">SYNOPSIS</span></span>
<span data-ttu-id="7f367-103">자체 호스팅 통합 런타임 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="7f367-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f367-104">SYNTAX</span></span>

### <span data-ttu-id="7f367-105">NewByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7f367-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f367-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f367-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f367-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f367-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f367-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f367-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f367-109">설명은</span><span class="sxs-lookup"><span data-stu-id="7f367-109">DESCRIPTION</span></span>
<span data-ttu-id="7f367-110">Cmdlet **AzSynapseIntegrationRuntimeKey** 는 ' KeyName ' 매개 변수에 의해 지정 된 키 이름을 사용 하 여 통합 런타임 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="7f367-111">이전 키가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="7f367-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7f367-112">EXAMPLES</span></span>

### <span data-ttu-id="7f367-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f367-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="7f367-114">Cmdlet은 ' test-selfhost-ir ' 이라는 통합 런타임에 대 한 ' authKey2 ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="7f367-115">변수</span><span class="sxs-lookup"><span data-stu-id="7f367-115">PARAMETERS</span></span>

### <span data-ttu-id="7f367-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f367-116">-DefaultProfile</span></span>
<span data-ttu-id="7f367-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f367-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7f367-118">-Force</span></span>
<span data-ttu-id="7f367-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7f367-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f367-120">-InputObject</span></span>
<span data-ttu-id="7f367-121">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7f367-122">-KeyName</span></span>
<span data-ttu-id="7f367-123">자체 호스팅 통합 런타임의 인증 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-124">-이름</span><span class="sxs-lookup"><span data-stu-id="7f367-124">-Name</span></span>
<span data-ttu-id="7f367-125">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f367-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f367-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f367-128">-ResourceId</span></span>
<span data-ttu-id="7f367-129">Synapse 통합 런타임의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f367-130">-WorkspaceName</span></span>
<span data-ttu-id="7f367-131">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7f367-132">-WorkspaceObject</span></span>
<span data-ttu-id="7f367-133">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f367-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7f367-134">-Confirm</span></span>
<span data-ttu-id="7f367-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f367-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f367-136">-WhatIf</span></span>
<span data-ttu-id="7f367-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f367-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f367-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f367-139">CommonParameters</span></span>
<span data-ttu-id="7f367-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f367-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f367-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7f367-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f367-142">입력</span><span class="sxs-lookup"><span data-stu-id="7f367-142">INPUTS</span></span>

### <span data-ttu-id="7f367-143">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="7f367-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7f367-144">Synapse. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="7f367-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7f367-145">출력</span><span class="sxs-lookup"><span data-stu-id="7f367-145">OUTPUTS</span></span>

### <span data-ttu-id="7f367-146">Synapse. PSIntegrationRuntimeKeys/.</span><span class="sxs-lookup"><span data-stu-id="7f367-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="7f367-147">상속자</span><span class="sxs-lookup"><span data-stu-id="7f367-147">NOTES</span></span>

## <span data-ttu-id="7f367-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f367-148">RELATED LINKS</span></span>