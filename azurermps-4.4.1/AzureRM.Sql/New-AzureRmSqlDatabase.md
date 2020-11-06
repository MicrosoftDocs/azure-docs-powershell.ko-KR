---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527220"
---
# <span data-ttu-id="9bd98-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9bd98-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="9bd98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bd98-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd98-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bd98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9bd98-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9bd98-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd98-106">**AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="9bd98-107">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="9bd98-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9bd98-108">EXAMPLES</span></span>

### <span data-ttu-id="9bd98-109">예제 1: 지정 된 서버에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="9bd98-109">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="9bd98-110">이 명령은 서버 Server01에 Database01 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="9bd98-111">예제 2: 지정 된 서버에서 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="9bd98-111">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="9bd98-112">이 명령은 서버 Server01의 ElasticPool01 이라는 탄력적 풀에 Database01 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="9bd98-113">변수</span><span class="sxs-lookup"><span data-stu-id="9bd98-113">PARAMETERS</span></span>

### <span data-ttu-id="9bd98-114">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="9bd98-114">-CatalogCollation</span></span>
<span data-ttu-id="9bd98-115">SQL 데이터베이스 카탈로그 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="9bd98-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="9bd98-116">-CollationName</span></span>
<span data-ttu-id="9bd98-117">SQL 데이터베이스 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="9bd98-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bd98-118">-DatabaseName</span></span>
<span data-ttu-id="9bd98-119">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-119">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-120">-에디션</span><span class="sxs-lookup"><span data-stu-id="9bd98-120">-Edition</span></span>
<span data-ttu-id="9bd98-121">데이터베이스에 할당할 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="9bd98-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9bd98-123">기본값</span><span class="sxs-lookup"><span data-stu-id="9bd98-123">Default</span></span>
- <span data-ttu-id="9bd98-124">않아야</span><span class="sxs-lookup"><span data-stu-id="9bd98-124">None</span></span>
- <span data-ttu-id="9bd98-125">Premium</span><span class="sxs-lookup"><span data-stu-id="9bd98-125">Premium</span></span>
- <span data-ttu-id="9bd98-126">기본적</span><span class="sxs-lookup"><span data-stu-id="9bd98-126">Basic</span></span>
- <span data-ttu-id="9bd98-127">표준이</span><span class="sxs-lookup"><span data-stu-id="9bd98-127">Standard</span></span>
- <span data-ttu-id="9bd98-128">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="9bd98-128">DataWarehouse</span></span>
- <span data-ttu-id="9bd98-129">비우거나</span><span class="sxs-lookup"><span data-stu-id="9bd98-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-130">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9bd98-130">-ElasticPoolName</span></span>
<span data-ttu-id="9bd98-131">데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="9bd98-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="9bd98-132">-MaxSizeBytes</span></span>
<span data-ttu-id="9bd98-133">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-133">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="9bd98-134">-ReadScale</span></span>
<span data-ttu-id="9bd98-135">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="9bd98-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9bd98-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="9bd98-137">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="9bd98-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd98-138">-ResourceGroupName</span></span>
<span data-ttu-id="9bd98-139">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="9bd98-140">-SampleName</span><span class="sxs-lookup"><span data-stu-id="9bd98-140">-SampleName</span></span>
<span data-ttu-id="9bd98-141">이 데이터베이스를 만들 때 적용할 샘플 스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-141">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9bd98-142">-ServerName</span></span>
<span data-ttu-id="9bd98-143">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9bd98-144">태그</span><span class="sxs-lookup"><span data-stu-id="9bd98-144">-Tags</span></span>
<span data-ttu-id="9bd98-145">이 cmdlet가 새 데이터베이스와 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="9bd98-146">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="9bd98-146">For example:</span></span>

<span data-ttu-id="9bd98-147">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9bd98-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-148">-확인</span><span class="sxs-lookup"><span data-stu-id="9bd98-148">-Confirm</span></span>
<span data-ttu-id="9bd98-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd98-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd98-150">-WhatIf</span></span>
<span data-ttu-id="9bd98-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd98-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd98-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd98-153">-DefaultProfile</span></span>
<span data-ttu-id="9bd98-154">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd98-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd98-155">CommonParameters</span></span>
<span data-ttu-id="9bd98-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bd98-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd98-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd98-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd98-158">입력</span><span class="sxs-lookup"><span data-stu-id="9bd98-158">INPUTS</span></span>

## <span data-ttu-id="9bd98-159">출력</span><span class="sxs-lookup"><span data-stu-id="9bd98-159">OUTPUTS</span></span>

### <span data-ttu-id="9bd98-160">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="9bd98-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9bd98-161">상속자</span><span class="sxs-lookup"><span data-stu-id="9bd98-161">NOTES</span></span>

## <span data-ttu-id="9bd98-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bd98-162">RELATED LINKS</span></span>

[<span data-ttu-id="9bd98-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9bd98-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="9bd98-164">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9bd98-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="9bd98-165">새로운 AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="9bd98-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="9bd98-166">제거-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9bd98-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="9bd98-167">이력서-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9bd98-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="9bd98-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9bd98-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="9bd98-169">일시 중단-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9bd98-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="9bd98-170">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9bd98-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)