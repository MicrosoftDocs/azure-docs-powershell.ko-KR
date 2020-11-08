---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216315"
---
# <span data-ttu-id="9c1a0-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9c1a0-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="9c1a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1a0-103">Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9c1a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c1a0-104">SYNTAX</span></span>

### <span data-ttu-id="9c1a0-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9c1a0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c1a0-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c1a0-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c1a0-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c1a0-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c1a0-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c1a0-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c1a0-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9c1a0-109">DESCRIPTION</span></span>
<span data-ttu-id="9c1a0-110">**업데이트 AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="9c1a0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9c1a0-111">EXAMPLES</span></span>

### <span data-ttu-id="9c1a0-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9c1a0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="9c1a0-113">이 명령은 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="9c1a0-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9c1a0-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="9c1a0-115">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9c1a0-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="9c1a0-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="9c1a0-117">이 명령은 파이프라인을 통해 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="9c1a0-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="9c1a0-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="9c1a0-119">이 명령은 리소스 ID를 사용 하 여 Azure Synapse Analytics SQL 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="9c1a0-120">변수</span><span class="sxs-lookup"><span data-stu-id="9c1a0-120">PARAMETERS</span></span>

### <span data-ttu-id="9c1a0-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c1a0-121">-AsJob</span></span>
<span data-ttu-id="9c1a0-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9c1a0-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c1a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1a0-123">-DefaultProfile</span></span>
<span data-ttu-id="9c1a0-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c1a0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c1a0-125">-InputObject</span></span>
<span data-ttu-id="9c1a0-126">일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="9c1a0-127">-Name</span></span>
<span data-ttu-id="9c1a0-128">Synapse SQL 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c1a0-129">-PassThru</span></span>
<span data-ttu-id="9c1a0-130">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="9c1a0-131">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9c1a0-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="9c1a0-132">-PerformanceLevel</span></span>
<span data-ttu-id="9c1a0-133">SQL 풀에 할당할 SQL 서비스 계층 및 성능 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="9c1a0-134">예를 DW2000c.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c1a0-135">-ResourceGroupName</span></span>
<span data-ttu-id="9c1a0-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c1a0-137">-ResourceId</span></span>
<span data-ttu-id="9c1a0-138">Synapse SQL 풀의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-139">태그</span><span class="sxs-lookup"><span data-stu-id="9c1a0-139">-Tag</span></span>
<span data-ttu-id="9c1a0-140">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-141">-버전</span><span class="sxs-lookup"><span data-stu-id="9c1a0-141">-Version</span></span>
<span data-ttu-id="9c1a0-142">Synapse SQL 풀의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="9c1a0-143">예를 들면 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-143">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9c1a0-144">-WorkspaceName</span></span>
<span data-ttu-id="9c1a0-145">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9c1a0-146">-WorkspaceObject</span></span>
<span data-ttu-id="9c1a0-147">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c1a0-148">-확인</span><span class="sxs-lookup"><span data-stu-id="9c1a0-148">-Confirm</span></span>
<span data-ttu-id="9c1a0-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c1a0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c1a0-150">-WhatIf</span></span>
<span data-ttu-id="9c1a0-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c1a0-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c1a0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1a0-153">CommonParameters</span></span>
<span data-ttu-id="9c1a0-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1a0-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1a0-156">입력</span><span class="sxs-lookup"><span data-stu-id="9c1a0-156">INPUTS</span></span>

### <span data-ttu-id="9c1a0-157">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9c1a0-158">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9c1a0-159">출력</span><span class="sxs-lookup"><span data-stu-id="9c1a0-159">OUTPUTS</span></span>

### <span data-ttu-id="9c1a0-160">Synapse. PSSynapseSqlPool/.</span><span class="sxs-lookup"><span data-stu-id="9c1a0-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9c1a0-161">상속자</span><span class="sxs-lookup"><span data-stu-id="9c1a0-161">NOTES</span></span>

## <span data-ttu-id="9c1a0-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c1a0-162">RELATED LINKS</span></span>