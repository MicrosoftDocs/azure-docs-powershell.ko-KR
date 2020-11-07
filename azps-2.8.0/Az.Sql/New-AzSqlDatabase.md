---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 3655204204dc35ea62473a1002a84d53ce0c327d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873893"
---
# <span data-ttu-id="fc239-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="fc239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc239-102">SYNOPSIS</span></span>
<span data-ttu-id="fc239-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="fc239-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc239-104">SYNTAX</span></span>

### <span data-ttu-id="fc239-105">DtuBasedDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc239-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc239-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc239-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc239-107">DESCRIPTION</span></span>
<span data-ttu-id="fc239-108">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="fc239-109">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="fc239-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fc239-110">EXAMPLES</span></span>

### <span data-ttu-id="fc239-111">예제 1: 지정 된 서버에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="fc239-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
LicenseType                   :
Tags                          :
```

<span data-ttu-id="fc239-112">이 명령은 서버 Server01에 Database01 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="fc239-113">예제 2: 지정 된 서버에서 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="fc239-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
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
LicenseType                   :
Tags                          :
```

<span data-ttu-id="fc239-114">이 명령은 서버 Server01의 ElasticPool01 이라는 탄력적 풀에 Database02 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="fc239-115">예제 3: 지정 된 서버에서 Vcore 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="fc239-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="fc239-116">이 명령은 서버 Server01에 Database03 이라는 Vcore 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="fc239-117">예제 4: 지정 된 서버에서 서버를 실행 하지 않은 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="fc239-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="fc239-118">이 명령은 서버 Server01에서 Database04 이라는 데이터베이스를 만들 때 생성 되지 않은 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="fc239-119">변수</span><span class="sxs-lookup"><span data-stu-id="fc239-119">PARAMETERS</span></span>

### <span data-ttu-id="fc239-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc239-120">-AsJob</span></span>
<span data-ttu-id="fc239-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fc239-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc239-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="fc239-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="fc239-123">데이터베이스에 대 한 자동 일시 정지 지연 시간 (서버를 사용할 수 없음),-1에서 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="fc239-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="fc239-124">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="fc239-124">-CatalogCollation</span></span>
<span data-ttu-id="fc239-125">SQL 데이터베이스 카탈로그 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-125">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="fc239-126">-CollationName</span><span class="sxs-lookup"><span data-stu-id="fc239-126">-CollationName</span></span>
<span data-ttu-id="fc239-127">SQL 데이터베이스 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-127">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="fc239-128">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="fc239-128">-ComputeGeneration</span></span>
<span data-ttu-id="fc239-129">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-129">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="fc239-130">-ComputeModel</span></span>
<span data-ttu-id="fc239-131">Azure Sql 데이터베이스의 계산 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-131">The compute model for Azure Sql database.</span></span> <span data-ttu-id="fc239-132">서버에서 또는 프로 비전 됨</span><span class="sxs-lookup"><span data-stu-id="fc239-132">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc239-133">-DatabaseName</span></span>
<span data-ttu-id="fc239-134">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="fc239-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc239-135">-DefaultProfile</span></span>
<span data-ttu-id="fc239-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc239-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc239-137">-에디션</span><span class="sxs-lookup"><span data-stu-id="fc239-137">-Edition</span></span>
<span data-ttu-id="fc239-138">데이터베이스에 할당할 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-138">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="fc239-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc239-140">않아야</span><span class="sxs-lookup"><span data-stu-id="fc239-140">None</span></span>
- <span data-ttu-id="fc239-141">기본적</span><span class="sxs-lookup"><span data-stu-id="fc239-141">Basic</span></span>
- <span data-ttu-id="fc239-142">표준이</span><span class="sxs-lookup"><span data-stu-id="fc239-142">Standard</span></span>
- <span data-ttu-id="fc239-143">Premium</span><span class="sxs-lookup"><span data-stu-id="fc239-143">Premium</span></span>
- <span data-ttu-id="fc239-144">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="fc239-144">DataWarehouse</span></span>
- <span data-ttu-id="fc239-145">비우거나</span><span class="sxs-lookup"><span data-stu-id="fc239-145">Free</span></span>
- <span data-ttu-id="fc239-146">늘이고</span><span class="sxs-lookup"><span data-stu-id="fc239-146">Stretch</span></span>
- <span data-ttu-id="fc239-147">일반 목적</span><span class="sxs-lookup"><span data-stu-id="fc239-147">GeneralPurpose</span></span>
- <span data-ttu-id="fc239-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="fc239-148">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fc239-149">-ElasticPoolName</span></span>
<span data-ttu-id="fc239-150">데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-150">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fc239-151">-LicenseType</span></span>
<span data-ttu-id="fc239-152">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="fc239-153">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-153">Possible values are:</span></span>
- <span data-ttu-id="fc239-154">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="fc239-155">기존 SQL Server 라이선스 소유자에 게 데이터베이스 가격이 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="fc239-156">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="fc239-157">데이터베이스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="fc239-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="fc239-158">-MaxSizeBytes</span></span>
<span data-ttu-id="fc239-159">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-159">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="fc239-160">-가을 용량</span><span class="sxs-lookup"><span data-stu-id="fc239-160">-MinimumCapacity</span></span>
<span data-ttu-id="fc239-161">데이터베이스가 일시 중지 되지 않은 경우 항상 할당 되는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="fc239-162">서버를 사용할 경우 Azure Sql 데이터베이스에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-163">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="fc239-163">-ReadScale</span></span>
<span data-ttu-id="fc239-164">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="fc239-164">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="fc239-165">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fc239-165">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="fc239-166">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-166">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc239-167">-ResourceGroupName</span></span>
<span data-ttu-id="fc239-168">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-168">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fc239-169">-SampleName</span><span class="sxs-lookup"><span data-stu-id="fc239-169">-SampleName</span></span>
<span data-ttu-id="fc239-170">이 데이터베이스를 만들 때 적용할 샘플 스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-170">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="fc239-171">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc239-171">-ServerName</span></span>
<span data-ttu-id="fc239-172">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-172">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="fc239-173">태그</span><span class="sxs-lookup"><span data-stu-id="fc239-173">-Tags</span></span>
<span data-ttu-id="fc239-174">이 cmdlet가 새 데이터베이스와 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-174">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="fc239-175">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fc239-175">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fc239-176">-VCore</span><span class="sxs-lookup"><span data-stu-id="fc239-176">-VCore</span></span>
<span data-ttu-id="fc239-177">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="fc239-177">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc239-178">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="fc239-178">-ZoneRedundant</span></span>
<span data-ttu-id="fc239-179">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="fc239-179">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="fc239-180">-확인</span><span class="sxs-lookup"><span data-stu-id="fc239-180">-Confirm</span></span>
<span data-ttu-id="fc239-181">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc239-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc239-182">-WhatIf</span></span>
<span data-ttu-id="fc239-183">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc239-184">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc239-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc239-185">CommonParameters</span></span>
<span data-ttu-id="fc239-186">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc239-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc239-187">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc239-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc239-188">입력</span><span class="sxs-lookup"><span data-stu-id="fc239-188">INPUTS</span></span>

### <span data-ttu-id="fc239-189">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc239-189">System.String</span></span>

## <span data-ttu-id="fc239-190">출력</span><span class="sxs-lookup"><span data-stu-id="fc239-190">OUTPUTS</span></span>

### <span data-ttu-id="fc239-191">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="fc239-191">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fc239-192">상속자</span><span class="sxs-lookup"><span data-stu-id="fc239-192">NOTES</span></span>

## <span data-ttu-id="fc239-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc239-193">RELATED LINKS</span></span>

[<span data-ttu-id="fc239-194">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-194">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="fc239-195">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fc239-195">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="fc239-196">새로운 AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="fc239-196">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="fc239-197">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-197">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="fc239-198">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-198">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="fc239-199">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-199">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="fc239-200">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc239-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="fc239-201">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="fc239-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
