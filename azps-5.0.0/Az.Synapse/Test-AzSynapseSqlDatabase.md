---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215145"
---
# <span data-ttu-id="29fcc-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="29fcc-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="29fcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="29fcc-103">Synapse Analytics SQL 데이터베이스가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="29fcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="29fcc-104">SYNTAX</span></span>

### <span data-ttu-id="29fcc-105">TestByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="29fcc-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29fcc-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29fcc-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29fcc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="29fcc-107">DESCRIPTION</span></span>
<span data-ttu-id="29fcc-108">**AzSynapseSqlDatabase** Cmdlet은 SYNAPSE Analytics SQL 데이터베이스의 존재 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="29fcc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="29fcc-109">EXAMPLES</span></span>

### <span data-ttu-id="29fcc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="29fcc-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="29fcc-111">이 명령은 지정 된 SQL 데이터베이스가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="29fcc-112">변수</span><span class="sxs-lookup"><span data-stu-id="29fcc-112">PARAMETERS</span></span>

### <span data-ttu-id="29fcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fcc-113">-DefaultProfile</span></span>
<span data-ttu-id="29fcc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29fcc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="29fcc-115">-Name</span></span>
<span data-ttu-id="29fcc-116">Synapse SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-116">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fcc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fcc-117">-ResourceGroupName</span></span>
<span data-ttu-id="29fcc-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fcc-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="29fcc-119">-WorkspaceName</span></span>
<span data-ttu-id="29fcc-120">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29fcc-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="29fcc-121">-WorkspaceObject</span></span>
<span data-ttu-id="29fcc-122">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29fcc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fcc-123">CommonParameters</span></span>
<span data-ttu-id="29fcc-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29fcc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fcc-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="29fcc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fcc-126">입력</span><span class="sxs-lookup"><span data-stu-id="29fcc-126">INPUTS</span></span>

### <span data-ttu-id="29fcc-127">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="29fcc-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="29fcc-128">출력</span><span class="sxs-lookup"><span data-stu-id="29fcc-128">OUTPUTS</span></span>

### <span data-ttu-id="29fcc-129">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="29fcc-129">System.Boolean</span></span>

## <span data-ttu-id="29fcc-130">상속자</span><span class="sxs-lookup"><span data-stu-id="29fcc-130">NOTES</span></span>

## <span data-ttu-id="29fcc-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29fcc-131">RELATED LINKS</span></span>