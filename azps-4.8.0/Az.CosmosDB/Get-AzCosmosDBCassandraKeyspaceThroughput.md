---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212394"
---
# <span data-ttu-id="7e8e1-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="7e8e1-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="7e8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8e1-103">Cassandra Keyspace의 처리 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="7e8e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e8e1-104">SYNTAX</span></span>

### <span data-ttu-id="7e8e1-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e8e1-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e8e1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e8e1-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e8e1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7e8e1-107">DESCRIPTION</span></span>
<span data-ttu-id="7e8e1-108">**AzCosmosDBCassandraKeyspaceThroughput** cmdlet은 지정 된 Keyspace에 해당 하는 처리 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="7e8e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7e8e1-109">EXAMPLES</span></span>

### <span data-ttu-id="7e8e1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e8e1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="7e8e1-111">변수</span><span class="sxs-lookup"><span data-stu-id="7e8e1-111">PARAMETERS</span></span>

### <span data-ttu-id="7e8e1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7e8e1-112">-AccountName</span></span>
<span data-ttu-id="7e8e1-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7e8e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8e1-114">-DefaultProfile</span></span>
<span data-ttu-id="7e8e1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e8e1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e8e1-116">-InputObject</span></span>
<span data-ttu-id="7e8e1-117">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="7e8e1-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8e1-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7e8e1-118">-Name</span></span>
<span data-ttu-id="7e8e1-119">Cassandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e8e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e8e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="7e8e1-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-121">Name of resource group.</span></span>

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

### <span data-ttu-id="7e8e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8e1-122">CommonParameters</span></span>
<span data-ttu-id="7e8e1-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8e1-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8e1-125">입력</span><span class="sxs-lookup"><span data-stu-id="7e8e1-125">INPUTS</span></span>

### <span data-ttu-id="7e8e1-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7e8e1-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7e8e1-127">출력</span><span class="sxs-lookup"><span data-stu-id="7e8e1-127">OUTPUTS</span></span>

### <span data-ttu-id="7e8e1-128">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="7e8e1-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="7e8e1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7e8e1-129">NOTES</span></span>

## <span data-ttu-id="7e8e1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e8e1-130">RELATED LINKS</span></span>