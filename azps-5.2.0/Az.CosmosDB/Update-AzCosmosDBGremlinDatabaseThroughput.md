---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323658"
---
# <span data-ttu-id="f7876-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="f7876-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="f7876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7876-102">SYNOPSIS</span></span>
<span data-ttu-id="f7876-103">CosmosDB Gremlin 데이터베이스의 데이터당 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f7876-104">구문</span><span class="sxs-lookup"><span data-stu-id="f7876-104">SYNTAX</span></span>

### <span data-ttu-id="f7876-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f7876-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7876-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7876-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7876-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7876-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7876-108">설명</span><span class="sxs-lookup"><span data-stu-id="f7876-108">DESCRIPTION</span></span>
<span data-ttu-id="f7876-109">CosmosDB Gremlin 데이터베이스의 데이터당 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f7876-110">예제</span><span class="sxs-lookup"><span data-stu-id="f7876-110">EXAMPLES</span></span>

### <span data-ttu-id="f7876-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f7876-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="f7876-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7876-112">PARAMETERS</span></span>

### <span data-ttu-id="f7876-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7876-113">-AccountName</span></span>
<span data-ttu-id="f7876-114">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7876-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f7876-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f7876-116">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f7876-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7876-117">-Confirm</span></span>
<span data-ttu-id="f7876-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7876-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7876-119">-DefaultProfile</span></span>
<span data-ttu-id="f7876-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7876-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7876-121">-InputObject</span></span>
<span data-ttu-id="f7876-122">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="f7876-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7876-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f7876-123">-Name</span></span>
<span data-ttu-id="f7876-124">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-124">Database name.</span></span>

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

### <span data-ttu-id="f7876-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7876-125">-ParentObject</span></span>
<span data-ttu-id="f7876-126">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="f7876-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f7876-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7876-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7876-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-128">Name of resource group.</span></span>

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

### <span data-ttu-id="f7876-129">-Throughput</span><span class="sxs-lookup"><span data-stu-id="f7876-129">-Throughput</span></span>
<span data-ttu-id="f7876-130">Gremlin 데이터베이스(RU/s)의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="f7876-131">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-131">Default value is 400.</span></span>

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

### <span data-ttu-id="f7876-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7876-132">-WhatIf</span></span>
<span data-ttu-id="f7876-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f7876-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7876-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7876-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7876-135">CommonParameters</span></span>
<span data-ttu-id="f7876-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f7876-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7876-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7876-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7876-138">입력</span><span class="sxs-lookup"><span data-stu-id="f7876-138">INPUTS</span></span>

### <span data-ttu-id="f7876-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f7876-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f7876-140">출력</span><span class="sxs-lookup"><span data-stu-id="f7876-140">OUTPUTS</span></span>

### <span data-ttu-id="f7876-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f7876-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f7876-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f7876-142">NOTES</span></span>

## <span data-ttu-id="f7876-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7876-143">RELATED LINKS</span></span>