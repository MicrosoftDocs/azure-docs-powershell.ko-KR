---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048682"
---
# <span data-ttu-id="06cbe-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="06cbe-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="06cbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="06cbe-103">탄력적 풀 및 해당 속성 값의 탄력적 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="06cbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06cbe-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06cbe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06cbe-105">DESCRIPTION</span></span>
<span data-ttu-id="06cbe-106">**AzSqlElasticPoolDatabase** cmdlet은 탄력적 풀 및 해당 속성 값의 탄력적 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="06cbe-107">Azure SQL 데이터베이스에서 탄력적 데이터베이스의 이름을 지정 하 여 해당 데이터베이스에 대 한 속성 값을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="06cbe-108">예제의</span><span class="sxs-lookup"><span data-stu-id="06cbe-108">EXAMPLES</span></span>

### <span data-ttu-id="06cbe-109">예제 1: 탄력적 풀의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="06cbe-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="06cbe-110">이 명령은 ElasticPool01 이라는 탄력적 풀의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="06cbe-111">예제 2: 필터링을 사용 하 여 탄력적 풀의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="06cbe-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="06cbe-112">이 명령은 "Database"로 시작 하는 ElasticPool01 이라는 탄력적 풀의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="06cbe-113">변수</span><span class="sxs-lookup"><span data-stu-id="06cbe-113">PARAMETERS</span></span>

### <span data-ttu-id="06cbe-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06cbe-114">-DatabaseName</span></span>
<span data-ttu-id="06cbe-115">이 cmdlet이 가져오는 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06cbe-116">-DefaultProfile</span></span>
<span data-ttu-id="06cbe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06cbe-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06cbe-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="06cbe-118">-ElasticPoolName</span></span>
<span data-ttu-id="06cbe-119">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-119">Specifies the name of an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cbe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06cbe-120">-ResourceGroupName</span></span>
<span data-ttu-id="06cbe-121">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cbe-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="06cbe-122">-ServerName</span></span>
<span data-ttu-id="06cbe-123">탄력적 풀이 포함 된 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-123">Specifies the name of a server that contains an elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06cbe-124">-확인</span><span class="sxs-lookup"><span data-stu-id="06cbe-124">-Confirm</span></span>
<span data-ttu-id="06cbe-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cbe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06cbe-126">-WhatIf</span></span>
<span data-ttu-id="06cbe-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06cbe-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06cbe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06cbe-129">CommonParameters</span></span>
<span data-ttu-id="06cbe-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06cbe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06cbe-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06cbe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06cbe-132">입력</span><span class="sxs-lookup"><span data-stu-id="06cbe-132">INPUTS</span></span>

### <span data-ttu-id="06cbe-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06cbe-133">System.String</span></span>

## <span data-ttu-id="06cbe-134">출력</span><span class="sxs-lookup"><span data-stu-id="06cbe-134">OUTPUTS</span></span>

### <span data-ttu-id="06cbe-135">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="06cbe-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="06cbe-136">상속자</span><span class="sxs-lookup"><span data-stu-id="06cbe-136">NOTES</span></span>

## <span data-ttu-id="06cbe-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06cbe-137">RELATED LINKS</span></span>

[<span data-ttu-id="06cbe-138">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06cbe-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="06cbe-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="06cbe-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="06cbe-140">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06cbe-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="06cbe-141">제거-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06cbe-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="06cbe-142">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06cbe-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)
