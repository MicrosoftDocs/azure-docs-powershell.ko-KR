---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlContainer.md
ms.openlocfilehash: afdd1296b01a6798d9253b7b21d15ba66f924c34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048373"
---
# <span data-ttu-id="4f16a-101">New-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="4f16a-101">New-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="4f16a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f16a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f16a-103">새 CosmosDB Sql 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-103">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="4f16a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f16a-104">SYNTAX</span></span>

### <span data-ttu-id="4f16a-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4f16a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>] [-PartitionKeyVersion <Int32>]
 -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f16a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f16a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlContainer -Name <String> [-IndexingPolicy <PSSqlIndexingPolicy>]
 [-PartitionKeyVersion <Int32>] -PartitionKeyKind <String> -PartitionKeyPath <String[]> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>] [-UniqueKeyPolicy <PSSqlUniqueKeyPolicy>]
 [-ConflictResolutionPolicyMode <String>] [-ConflictResolutionPolicyPath <String>]
 [-ConflictResolutionPolicyProcedure <String>] [-ConflictResolutionPolicy <PSSqlConflictResolutionPolicy>]
 -ParentObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f16a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4f16a-107">DESCRIPTION</span></span>
<span data-ttu-id="4f16a-108">새 CosmosDB Sql 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-108">Creates a new CosmosDB Sql Container.</span></span>

## <span data-ttu-id="4f16a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4f16a-109">EXAMPLES</span></span>

### <span data-ttu-id="4f16a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f16a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlContainer -AccountName myAccountName -DatabaseName myDatabaseName -ResourceGroupName myRgName -Name myContainerName -PartitionKeyPath /a/b/c -PartitionKeyKind Hash

Name     : myContainerName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName/contain
           ers/myContainerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="4f16a-111">변수</span><span class="sxs-lookup"><span data-stu-id="4f16a-111">PARAMETERS</span></span>

### <span data-ttu-id="4f16a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4f16a-112">-AccountName</span></span>
<span data-ttu-id="4f16a-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4f16a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4f16a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4f16a-115">자동 크기 조정을 사용 하는 경우 최대 처리량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-116">-확인</span><span class="sxs-lookup"><span data-stu-id="4f16a-116">-Confirm</span></span>
<span data-ttu-id="4f16a-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-118">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="4f16a-118">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="4f16a-119">PSSqlConflictResolutionPolicy 형식의 ConflictResolutionPolicy 개체는 제공 되는 경우 컨테이너의 ConflictResolutionPolicy로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-119">ConflictResolutionPolicy Object of type PSSqlConflictResolutionPolicy, when provided this is set as the ConflictResolutionPolicy of the container.</span></span>

```yaml
Type: PSSqlConflictResolutionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-120">-ConflictResolutionPolicyMode</span><span class="sxs-lookup"><span data-stu-id="4f16a-120">-ConflictResolutionPolicyMode</span></span>
<span data-ttu-id="4f16a-121">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-121">Can have the values: LastWriterWins, Custom, Manual.</span></span>
<span data-ttu-id="4f16a-122">ConflictResolutionPolicy 매개 변수와 함께 제공 된 경우이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-122">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="4f16a-123">-ConflictResolutionPolicyPath</span><span class="sxs-lookup"><span data-stu-id="4f16a-123">-ConflictResolutionPolicyPath</span></span>
<span data-ttu-id="4f16a-124">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-124">To be provided when the type is LastWriterWins.</span></span>
<span data-ttu-id="4f16a-125">ConflictResolutionPolicy 매개 변수와 함께 제공 된 경우이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-125">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="4f16a-126">-ConflictResolutionPolicyProcedure</span><span class="sxs-lookup"><span data-stu-id="4f16a-126">-ConflictResolutionPolicyProcedure</span></span>
<span data-ttu-id="4f16a-127">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-127">To be provided when the type is custom.</span></span>
<span data-ttu-id="4f16a-128">ConflictResolutionPolicy 매개 변수와 함께 제공 된 경우이는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-128">If provided along with ConflictResolutionPolicy parameter, it is ignored.</span></span>

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

### <span data-ttu-id="4f16a-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f16a-129">-DatabaseName</span></span>
<span data-ttu-id="4f16a-130">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-130">Database name.</span></span>

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

### <span data-ttu-id="4f16a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f16a-131">-DefaultProfile</span></span>
<span data-ttu-id="4f16a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f16a-133">-IndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f16a-133">-IndexingPolicy</span></span>
<span data-ttu-id="4f16a-134">CosmosDB Sqlindexingpolicy 유형의 인덱싱 정책 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-134">Indexing Policy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlIndexingPolicy.</span></span>

```yaml
Type: PSSqlIndexingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-135">-이름</span><span class="sxs-lookup"><span data-stu-id="4f16a-135">-Name</span></span>
<span data-ttu-id="4f16a-136">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-136">Container name.</span></span>

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

### <span data-ttu-id="4f16a-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4f16a-137">-ParentObject</span></span>
<span data-ttu-id="4f16a-138">Sql 데이터베이스 개체.</span><span class="sxs-lookup"><span data-stu-id="4f16a-138">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-139">-파티션 형식</span><span class="sxs-lookup"><span data-stu-id="4f16a-139">-PartitionKeyKind</span></span>
<span data-ttu-id="4f16a-140">분할에 사용 되는 알고리즘의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-140">The kind of algorithm used for partitioning.</span></span>
<span data-ttu-id="4f16a-141">사용할 수 있는 값은 다음과 같습니다. ' Hash ', ' Range '</span><span class="sxs-lookup"><span data-stu-id="4f16a-141">Possible values include: 'Hash', 'Range'</span></span>

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

### <span data-ttu-id="4f16a-142">-PartitionKeyPath</span><span class="sxs-lookup"><span data-stu-id="4f16a-142">-PartitionKeyPath</span></span>
<span data-ttu-id="4f16a-143">파티션 키 경로 (예: '/address/zipcode ').</span><span class="sxs-lookup"><span data-stu-id="4f16a-143">Partition Key Path, e.g., '/address/zipcode'.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-144">-파티션 버전</span><span class="sxs-lookup"><span data-stu-id="4f16a-144">-PartitionKeyVersion</span></span>
<span data-ttu-id="4f16a-145">파티션 키 정의 버전</span><span class="sxs-lookup"><span data-stu-id="4f16a-145">The version of the partition key definition</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f16a-146">-ResourceGroupName</span></span>
<span data-ttu-id="4f16a-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-147">Name of resource group.</span></span>

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

### <span data-ttu-id="4f16a-148">-처리량</span><span class="sxs-lookup"><span data-stu-id="4f16a-148">-Throughput</span></span>
<span data-ttu-id="4f16a-149">SQL 컨테이너 (과)의 처리량입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-149">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="4f16a-150">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-150">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-151">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="4f16a-151">-TtlInSeconds</span></span>
<span data-ttu-id="4f16a-152">기본 Ttl (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-152">Default Ttl in seconds.</span></span>
<span data-ttu-id="4f16a-153">값이 누락 되거나-1로 설정 되어 있으면 항목이 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-153">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="4f16a-154">값이 n으로 설정 된 경우 항목은 마지막으로 수정한 시간 이후 n 초 후에 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-154">If the value is set to n, items will expire n seconds after last modified time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-155">-UniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="4f16a-155">-UniqueKeyPolicy</span></span>
<span data-ttu-id="4f16a-156">UniqueKeyPolicy. CosmosDB. PSSqlUniqueKeyPolicy의 형식 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-156">UniqueKeyPolicy Object of type Microsoft.Azure.Commands.CosmosDB.PSSqlUniqueKeyPolicy.</span></span>

```yaml
Type: PSSqlUniqueKeyPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f16a-157">-WhatIf</span></span>
<span data-ttu-id="4f16a-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f16a-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f16a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f16a-160">CommonParameters</span></span>
<span data-ttu-id="4f16a-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f16a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f16a-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f16a-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f16a-163">입력</span><span class="sxs-lookup"><span data-stu-id="4f16a-163">INPUTS</span></span>

### <span data-ttu-id="4f16a-164">CosmosDB. PSSqlIndexingPolicy</span><span class="sxs-lookup"><span data-stu-id="4f16a-164">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlIndexingPolicy</span></span>

### <span data-ttu-id="4f16a-165">CosmosDB. PSSqlUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="4f16a-165">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

### <span data-ttu-id="4f16a-166">CosmosDB. PSSqlConflictResolutionPolicy/.</span><span class="sxs-lookup"><span data-stu-id="4f16a-166">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

### <span data-ttu-id="4f16a-167">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="4f16a-167">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="4f16a-168">출력</span><span class="sxs-lookup"><span data-stu-id="4f16a-168">OUTPUTS</span></span>

### <span data-ttu-id="4f16a-169">CosmosDB. PSSqlDatabaseGetResults/.</span><span class="sxs-lookup"><span data-stu-id="4f16a-169">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="4f16a-170">CosmosDB (ConflictingResourceException).</span><span class="sxs-lookup"><span data-stu-id="4f16a-170">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4f16a-171">상속자</span><span class="sxs-lookup"><span data-stu-id="4f16a-171">NOTES</span></span>

## <span data-ttu-id="4f16a-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f16a-172">RELATED LINKS</span></span>