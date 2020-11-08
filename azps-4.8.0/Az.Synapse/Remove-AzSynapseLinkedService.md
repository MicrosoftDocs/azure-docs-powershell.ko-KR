---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseLinkedService.md
ms.openlocfilehash: ca493914cc91d16566fddcebed5367fa81be1d2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056629"
---
# <span data-ttu-id="0eb1b-101">Remove-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="0eb1b-101">Remove-AzSynapseLinkedService</span></span>

## <span data-ttu-id="0eb1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb1b-103">작업 영역에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-103">Removes a linked service from workspace.</span></span>

## <span data-ttu-id="0eb1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0eb1b-104">SYNTAX</span></span>

### <span data-ttu-id="0eb1b-105">RemoveByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0eb1b-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb1b-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="0eb1b-106">RemoveByObject</span></span>
```
Remove-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eb1b-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="0eb1b-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseLinkedService -InputObject <PSLinkedServiceResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb1b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0eb1b-108">DESCRIPTION</span></span>
<span data-ttu-id="0eb1b-109">**AzSynapseLinkedService** cmdlet은 작업 영역에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-109">The **Remove-AzSynapseLinkedService** cmdlet removes a linked service from workspace.</span></span>

## <span data-ttu-id="0eb1b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0eb1b-110">EXAMPLES</span></span>

### <span data-ttu-id="0eb1b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0eb1b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="0eb1b-112">이 명령은 ContosoWorkspace 이라는 작업 영역에서 ContosoLinkedService 이라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-112">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0eb1b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0eb1b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="0eb1b-114">이 명령은 ContosoWorkspace ~ 파이프라인 이라는 작업 영역에서 ContosoLinkedService 이라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-114">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="0eb1b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="0eb1b-115">Example 3</span></span>
```powershell
PS C:\> $linkedService = Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
PS C:\> $linkedService | Remove-AzSynapseLinkedService
```

<span data-ttu-id="0eb1b-116">이 명령은 ContosoWorkspace ~ 파이프라인 이라는 작업 영역에서 ContosoLinkedService 이라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-116">This command removes the linked service named ContosoLinkedService from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0eb1b-117">변수</span><span class="sxs-lookup"><span data-stu-id="0eb1b-117">PARAMETERS</span></span>

### <span data-ttu-id="0eb1b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0eb1b-118">-AsJob</span></span>
<span data-ttu-id="0eb1b-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0eb1b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0eb1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb1b-120">-DefaultProfile</span></span>
<span data-ttu-id="0eb1b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0eb1b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0eb1b-122">-InputObject</span></span>
<span data-ttu-id="0eb1b-123">연결 된 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-123">The linked service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb1b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="0eb1b-124">-Name</span></span>
<span data-ttu-id="0eb1b-125">연결 된 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-125">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb1b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0eb1b-126">-PassThru</span></span>
<span data-ttu-id="0eb1b-127">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0eb1b-128">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0eb1b-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0eb1b-129">-WorkspaceName</span></span>
<span data-ttu-id="0eb1b-130">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb1b-131">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0eb1b-131">-WorkspaceObject</span></span>
<span data-ttu-id="0eb1b-132">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb1b-133">-확인</span><span class="sxs-lookup"><span data-stu-id="0eb1b-133">-Confirm</span></span>
<span data-ttu-id="0eb1b-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb1b-135">-WhatIf</span></span>
<span data-ttu-id="0eb1b-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eb1b-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb1b-138">CommonParameters</span></span>
<span data-ttu-id="0eb1b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb1b-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb1b-141">입력</span><span class="sxs-lookup"><span data-stu-id="0eb1b-141">INPUTS</span></span>

### <span data-ttu-id="0eb1b-142">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0eb1b-143">Synapse. PSLinkedServiceResource/.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-143">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="0eb1b-144">출력</span><span class="sxs-lookup"><span data-stu-id="0eb1b-144">OUTPUTS</span></span>

### <span data-ttu-id="0eb1b-145">Synapse. PSLinkedServiceResource/.</span><span class="sxs-lookup"><span data-stu-id="0eb1b-145">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="0eb1b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="0eb1b-146">NOTES</span></span>

## <span data-ttu-id="0eb1b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0eb1b-147">RELATED LINKS</span></span>