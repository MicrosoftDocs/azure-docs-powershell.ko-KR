---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 1b8bcbdeb797aea0faa5e9b3a0b5cb1e36b0f1b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214205"
---
# <span data-ttu-id="23877-101">Get-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="23877-101">Get-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="23877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23877-102">SYNOPSIS</span></span>
<span data-ttu-id="23877-103">CosmosDB Gremlin 그래프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23877-103">Gets the CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="23877-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23877-104">SYNTAX</span></span>

### <span data-ttu-id="23877-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="23877-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinGraph -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="23877-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23877-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinGraph [-Name <String>] -ParentObject <PSGremlinDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23877-107">설명은</span><span class="sxs-lookup"><span data-stu-id="23877-107">DESCRIPTION</span></span>
<span data-ttu-id="23877-108">**AzCosmosDBGremlinGraph** Cmdlet은 CosmosDB Gremlin 그래프 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23877-108">The **Get-AzCosmosDBGremlinGraph** cmdlet gets the CosmosDB Gremlin Graph properties.</span></span>

## <span data-ttu-id="23877-109">예제의</span><span class="sxs-lookup"><span data-stu-id="23877-109">EXAMPLES</span></span>

### <span data-ttu-id="23877-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="23877-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetPropertiesResource
```

<span data-ttu-id="23877-111">리소스 개체에는 IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23877-111">Resource Object contains IndexingPolicy, PartitionKey, DefaultTtl, UniqueKeyPolicy, ConflictResolutionPolicy, _rid, _ts, _etag.</span></span>

## <span data-ttu-id="23877-112">변수</span><span class="sxs-lookup"><span data-stu-id="23877-112">PARAMETERS</span></span>

### <span data-ttu-id="23877-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="23877-113">-AccountName</span></span>
<span data-ttu-id="23877-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23877-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23877-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23877-115">-DatabaseName</span></span>
<span data-ttu-id="23877-116">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23877-116">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23877-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23877-117">-DefaultProfile</span></span>
<span data-ttu-id="23877-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23877-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23877-119">-이름</span><span class="sxs-lookup"><span data-stu-id="23877-119">-Name</span></span>
<span data-ttu-id="23877-120">Gremlin 그래프 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23877-120">Gremlin Graph Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23877-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="23877-121">-ParentObject</span></span>
<span data-ttu-id="23877-122">Gremlin Database 개체.</span><span class="sxs-lookup"><span data-stu-id="23877-122">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23877-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23877-123">-ResourceGroupName</span></span>
<span data-ttu-id="23877-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23877-124">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23877-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23877-125">CommonParameters</span></span>
<span data-ttu-id="23877-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23877-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23877-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23877-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23877-128">입력</span><span class="sxs-lookup"><span data-stu-id="23877-128">INPUTS</span></span>

### <span data-ttu-id="23877-129">CosmosDB. PSGremlinDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="23877-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="23877-130">출력</span><span class="sxs-lookup"><span data-stu-id="23877-130">OUTPUTS</span></span>

### <span data-ttu-id="23877-131">CosmosDB. PSGremlinGraphGetResults/.</span><span class="sxs-lookup"><span data-stu-id="23877-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

### <span data-ttu-id="23877-132">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="23877-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="23877-133">상속자</span><span class="sxs-lookup"><span data-stu-id="23877-133">NOTES</span></span>

## <span data-ttu-id="23877-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23877-134">RELATED LINKS</span></span>