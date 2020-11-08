---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1d470870d27001a07302240dba1abd7e56153d0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044107"
---
# <span data-ttu-id="c5e87-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="c5e87-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="c5e87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e87-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e87-103">MongoDB 데이터베이스의 CosmosDB 처리량 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="c5e87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5e87-104">SYNTAX</span></span>

### <span data-ttu-id="c5e87-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5e87-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5e87-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5e87-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5e87-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c5e87-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e87-108">**AzCosmosDBMongoDBDatabaseThroughput** Cmdlet은 MongoDB 데이터베이스의 처리량 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="c5e87-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5e87-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e87-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5e87-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="c5e87-111">변수</span><span class="sxs-lookup"><span data-stu-id="c5e87-111">PARAMETERS</span></span>

### <span data-ttu-id="c5e87-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5e87-112">-AccountName</span></span>
<span data-ttu-id="c5e87-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c5e87-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e87-114">-DefaultProfile</span></span>
<span data-ttu-id="c5e87-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5e87-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5e87-116">-InputObject</span></span>
<span data-ttu-id="c5e87-117">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="c5e87-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e87-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c5e87-118">-Name</span></span>
<span data-ttu-id="c5e87-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-119">Database name.</span></span>

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

### <span data-ttu-id="c5e87-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e87-120">-ResourceGroupName</span></span>
<span data-ttu-id="c5e87-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-121">Name of resource group.</span></span>

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

### <span data-ttu-id="c5e87-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e87-122">CommonParameters</span></span>
<span data-ttu-id="c5e87-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5e87-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e87-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5e87-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e87-125">입력</span><span class="sxs-lookup"><span data-stu-id="c5e87-125">INPUTS</span></span>

### <span data-ttu-id="c5e87-126">않아야</span><span class="sxs-lookup"><span data-stu-id="c5e87-126">None</span></span>

## <span data-ttu-id="c5e87-127">출력</span><span class="sxs-lookup"><span data-stu-id="c5e87-127">OUTPUTS</span></span>

### <span data-ttu-id="c5e87-128">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="c5e87-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c5e87-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c5e87-129">NOTES</span></span>

## <span data-ttu-id="c5e87-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5e87-130">RELATED LINKS</span></span>