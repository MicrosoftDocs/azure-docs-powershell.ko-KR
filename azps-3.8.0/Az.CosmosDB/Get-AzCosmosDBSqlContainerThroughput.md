---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 61acd388dabcfe71c83d282d032e9d4bb688d88b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044109"
---
# <span data-ttu-id="a5356-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="a5356-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="a5356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5356-102">SYNOPSIS</span></span>
<span data-ttu-id="a5356-103">CosmosDB Sql 컨테이너에 해당 하는 처리량 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="a5356-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5356-104">SYNTAX</span></span>

### <span data-ttu-id="a5356-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5356-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5356-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5356-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5356-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5356-107">DESCRIPTION</span></span>
<span data-ttu-id="a5356-108">**AzCosmosDBSqlContainerThroughput** Cmdlet은 CosmosDB Sql 컨테이너에 해당 하는 처리량 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="a5356-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5356-109">EXAMPLES</span></span>

### <span data-ttu-id="a5356-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a5356-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="a5356-111">변수</span><span class="sxs-lookup"><span data-stu-id="a5356-111">PARAMETERS</span></span>

### <span data-ttu-id="a5356-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5356-112">-AccountName</span></span>
<span data-ttu-id="a5356-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a5356-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5356-114">-DatabaseName</span></span>
<span data-ttu-id="a5356-115">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-115">Database name.</span></span>

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

### <span data-ttu-id="a5356-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5356-116">-DefaultProfile</span></span>
<span data-ttu-id="a5356-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5356-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5356-118">-InputObject</span></span>
<span data-ttu-id="a5356-119">Sql 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="a5356-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5356-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a5356-120">-Name</span></span>
<span data-ttu-id="a5356-121">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-121">Container name.</span></span>

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

### <span data-ttu-id="a5356-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5356-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5356-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-123">Name of resource group.</span></span>

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

### <span data-ttu-id="a5356-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5356-124">CommonParameters</span></span>
<span data-ttu-id="a5356-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5356-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5356-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5356-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5356-127">입력</span><span class="sxs-lookup"><span data-stu-id="a5356-127">INPUTS</span></span>

### <span data-ttu-id="a5356-128">않아야</span><span class="sxs-lookup"><span data-stu-id="a5356-128">None</span></span>

## <span data-ttu-id="a5356-129">출력</span><span class="sxs-lookup"><span data-stu-id="a5356-129">OUTPUTS</span></span>

### <span data-ttu-id="a5356-130">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="a5356-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a5356-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a5356-131">NOTES</span></span>

## <span data-ttu-id="a5356-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5356-132">RELATED LINKS</span></span>