---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlDatabase.md
ms.openlocfilehash: c4bca877138f07c5bd3b0b5303ab09c39eb700a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327151"
---
# <span data-ttu-id="a9445-101">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9445-101">Restore-AzSqlDatabase</span></span>

## <span data-ttu-id="a9445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9445-102">SYNOPSIS</span></span>
<span data-ttu-id="a9445-103">데이터베이스를 SQL 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-103">Restores a SQL database.</span></span>

## <span data-ttu-id="a9445-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9445-104">SYNTAX</span></span>

### <span data-ttu-id="a9445-105">FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-105">FromPointInTimeBackup</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9445-106">FromPointInTimeBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a9445-106">FromPointInTimeBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String>
 -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9445-107">FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-107">FromDeletedDatabaseBackup</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <String>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob] [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9445-108">FromDeletedDatabaseBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a9445-108">FromDeletedDatabaseBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> -Edition <String> [-AsJob]
 -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>] [-BackupStorageRedundancy <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9445-109">FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-109">FromGeoBackup</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9445-110">FromGeoBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a9445-110">FromGeoBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String> -TargetDatabaseName <String>
 -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9445-111">FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-111">FromLongTermRetentionBackup</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <String>] [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9445-112">FromLongTermRetentionBackupWithVcore</span><span class="sxs-lookup"><span data-stu-id="a9445-112">FromLongTermRetentionBackupWithVcore</span></span>
```
Restore-AzSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> -Edition <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9445-113">설명</span><span class="sxs-lookup"><span data-stu-id="a9445-113">DESCRIPTION</span></span>
<span data-ttu-id="a9445-114">**Restore-AzSqlDatabase** cmdlet은 지역 중복 백업, 삭제된 데이터베이스의 백업, 장기 보존 백업 또는 라이브 데이터베이스의 지정 시간에서 SQL 데이터베이스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-114">The **Restore-AzSqlDatabase** cmdlet restores a SQL database from a geo-redundant backup, a backup of a deleted database, a long term retention backup, or a point in time in a live database.</span></span>
<span data-ttu-id="a9445-115">복원된 데이터베이스는 새 데이터베이스로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-115">The restored database is created as a new database.</span></span>
<span data-ttu-id="a9445-116">*ElasticPoolName* 매개 SQL 기존 탄력적 풀로 설정하여 탄력적 데이터베이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-116">You can create an elastic SQL database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="a9445-117">예제</span><span class="sxs-lookup"><span data-stu-id="a9445-117">EXAMPLES</span></span>

### <span data-ttu-id="a9445-118">예제 1: 시점에서 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="a9445-118">Example 1: Restore a database from a point in time</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

<span data-ttu-id="a9445-119">첫 번째 명령은 Database01이라는 SQL 데이터베이스를 인용한 다음, $Database 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-119">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="a9445-120">두 번째 명령은 지정된 $Database 지정 시간 백업에서 RestoreDatabase라는 데이터베이스로 데이터베이스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-120">The second command restores the database in $Database from the specified point-in-time backup to the database named RestoredDatabase.</span></span>

### <span data-ttu-id="a9445-121">예제 2: 시점에서 탄력적 풀로 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="a9445-121">Example 2: Restore a database from a point in time to an elastic pool</span></span>
```
PS C:\>$Database = Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a9445-122">첫 번째 명령은 Database01이라는 SQL 데이터베이스를 인용한 다음, $Database 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-122">The first command gets the SQL database named Database01, and then stores it in the $Database variable.</span></span>
<span data-ttu-id="a9445-123">두 번째 명령은 지정한 지정 시간 $Database elasticpool01 탄력적 풀의 RestoreDatabase라는 SQL 데이터베이스로 데이터베이스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-123">The second command restores the database in $Database from the specified point-in-time backup to the SQL database named RestoredDatabase in the elastic pool named elasticpool01.</span></span>

### <span data-ttu-id="a9445-124">예제 3: 삭제된 데이터베이스 복원</span><span class="sxs-lookup"><span data-stu-id="a9445-124">Example 3: Restore a deleted database</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

<span data-ttu-id="a9445-125">첫 번째 명령은 [Get-AzSqlDeletedDatabaseBackup을](./Get-AzSqlDeletedDatabaseBackup.md)사용하여 복원하려는 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-125">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="a9445-126">두 번째 명령은 [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet을 사용하여 삭제된 데이터베이스 백업에서 복원을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-126">The second command starts the restore from the deleted database backup by using the [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md) cmdlet.</span></span> <span data-ttu-id="a9445-127">-PointInTime 매개 변수를 지정하지 않으면 데이터베이스가 지우기 시간으로 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-127">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="a9445-128">예제 4: 삭제된 데이터베이스를 탄력적 풀로 복원</span><span class="sxs-lookup"><span data-stu-id="a9445-128">Example 4: Restore a deleted database into an elastic pool</span></span>
```
PS C:\>$DeletedDatabase = Get-AzSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

<span data-ttu-id="a9445-129">첫 번째 명령은 [Get-AzSqlDeletedDatabaseBackup을](./Get-AzSqlDeletedDatabaseBackup.md)사용하여 복원하려는 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-129">The first command gets the deleted database backup that you want to restore by using [Get-AzSqlDeletedDatabaseBackup](./Get-AzSqlDeletedDatabaseBackup.md).</span></span>
<span data-ttu-id="a9445-130">두 번째 명령은 [Restore-AzSqlDatabase를](./Restore-AzSqlDatabase.md)사용하여 삭제된 데이터베이스 백업에서 복원을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-130">The second command starts the restore from the deleted database backup by using [Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md).</span></span> <span data-ttu-id="a9445-131">-PointInTime 매개 변수를 지정하지 않으면 데이터베이스가 지우기 시간으로 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-131">If the -PointInTime parameter is not specified, the database will be restored to the deletion time.</span></span>

### <span data-ttu-id="a9445-132">예제 5: Geo-Restore 연결</span><span class="sxs-lookup"><span data-stu-id="a9445-132">Example 5: Geo-Restore a database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

<span data-ttu-id="a9445-133">첫 번째 명령은 Database01이라는 데이터베이스에 대한 지역 중복 백업을 수행한 다음, 데이터베이스 변수에 $GeoBackup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-133">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="a9445-134">두 번째 명령은 RestoreDatabase라는 $GeoBackup 데이터베이스로 SQL 백업을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-134">The second command restores the backup in $GeoBackup to the SQL database named RestoredDatabase.</span></span>

## <span data-ttu-id="a9445-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9445-135">PARAMETERS</span></span>

### <span data-ttu-id="a9445-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9445-136">-AsJob</span></span>
<span data-ttu-id="a9445-137">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a9445-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9445-138">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a9445-138">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a9445-139">SQL 데이터베이스에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-139">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="a9445-140">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-140">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-141">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a9445-141">-ComputeGeneration</span></span>
<span data-ttu-id="a9445-142">복원된 데이터베이스에 할당할 계산 생성</span><span class="sxs-lookup"><span data-stu-id="a9445-142">The compute generation to assign to the restored database</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9445-143">-DefaultProfile</span></span>
<span data-ttu-id="a9445-144">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a9445-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9445-145">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a9445-145">-DeletionDate</span></span>
<span data-ttu-id="a9445-146">삭제 날짜를 **DateTime 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="a9445-146">Specifies the deletion date as a **DateTime** object.</span></span>
<span data-ttu-id="a9445-147">**DateTime 개체를** 얻습니다. Get-Date cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-147">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-148">-Edition</span><span class="sxs-lookup"><span data-stu-id="a9445-148">-Edition</span></span>
<span data-ttu-id="a9445-149">SQL 데이터베이스의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-149">Specifies the edition of the SQL database.</span></span>
<span data-ttu-id="a9445-150">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a9445-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9445-151">없음</span><span class="sxs-lookup"><span data-stu-id="a9445-151">None</span></span>
- <span data-ttu-id="a9445-152">기본</span><span class="sxs-lookup"><span data-stu-id="a9445-152">Basic</span></span>
- <span data-ttu-id="a9445-153">표준</span><span class="sxs-lookup"><span data-stu-id="a9445-153">Standard</span></span>
- <span data-ttu-id="a9445-154">프리미엄</span><span class="sxs-lookup"><span data-stu-id="a9445-154">Premium</span></span>
- <span data-ttu-id="a9445-155">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="a9445-155">DataWarehouse</span></span>
- <span data-ttu-id="a9445-156">무료</span><span class="sxs-lookup"><span data-stu-id="a9445-156">Free</span></span>
- <span data-ttu-id="a9445-157">Stretch</span><span class="sxs-lookup"><span data-stu-id="a9445-157">Stretch</span></span>
- <span data-ttu-id="a9445-158">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="a9445-158">GeneralPurpose</span></span>
- <span data-ttu-id="a9445-159">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="a9445-159">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-160">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a9445-160">-ElasticPoolName</span></span>
<span data-ttu-id="a9445-161">데이터베이스를 넣을 탄력적 풀의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-161">Specifies the name of the elastic pool in which to put the SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-162">-FromDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-162">-FromDeletedDatabaseBackup</span></span>
<span data-ttu-id="a9445-163">이 cmdlet이 삭제된 데이터베이스의 백업에서 데이터베이스를 SQL 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-163">Indicates that this cmdlet restores a database from a backup of a deleted SQL database.</span></span>
<span data-ttu-id="a9445-164">Get-AzSqlDeletedDatabaseBackup cmdlet을 사용하여 삭제된 데이터베이스의 백업을 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-164">You can use the Get-AzSqlDeletedDatabaseBackup cmdlet to get the backup of a deleted SQL database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-165">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-165">-FromGeoBackup</span></span>
<span data-ttu-id="a9445-166">이 cmdlet은 지역 중복 백업에서 SQL 데이터베이스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-166">Indicates that this cmdlet restores a SQL database from a geo-redundant backup.</span></span>
<span data-ttu-id="a9445-167">지역 중복 백업을 Get-AzSqlDatabaseGeoBackup cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-167">You can use the Get-AzSqlDatabaseGeoBackup cmdlet to get a geo-redundant backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup, FromGeoBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-168">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-168">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="a9445-169">이 cmdlet은 장기 보존 백업에서 SQL 데이터베이스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-169">Indicates that this cmdlet restores a SQL database from a long term retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup, FromLongTermRetentionBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-170">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-170">-FromPointInTimeBackup</span></span>
<span data-ttu-id="a9445-171">이 cmdlet이 지정 시간 백업에서 SQL 데이터베이스를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-171">Indicates that this cmdlet restores a SQL database from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-172">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a9445-172">-LicenseType</span></span>
<span data-ttu-id="a9445-173">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-173">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="a9445-174">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="a9445-174">-PointInTime</span></span>
<span data-ttu-id="a9445-175">데이터베이스를 복원하려는 특정 시점을 **DateTime** 개체로 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-175">Specifies the point in time, as a **DateTime** object, that you want to restore your SQL database to.</span></span>
<span data-ttu-id="a9445-176">**DateTime 개체를** 얻습니다. **Get-Date** cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-176">To get a **DateTime** object, use **Get-Date** cmdlet.</span></span>
<span data-ttu-id="a9445-177">*FromPointInTimeBackup* 매개 변수와 함께 이 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-177">Use this parameter together with the *FromPointInTimeBackup* parameter.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup, FromPointInTimeBackupWithVcore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup, FromDeletedDatabaseBackupWithVcore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9445-178">-ResourceGroupName</span></span>
<span data-ttu-id="a9445-179">이 cmdlet이 리소스 데이터베이스를 할당할 리소스 그룹의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-179">Specifies the name of the resource group to which this cmdlet assigns the SQL database.</span></span>

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

### <span data-ttu-id="a9445-180">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9445-180">-ResourceId</span></span>
<span data-ttu-id="a9445-181">복원할 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-181">Specifies the ID of the resource to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9445-182">-ServerName</span></span>
<span data-ttu-id="a9445-183">데이터베이스 서버의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-183">Specifies the name of the SQL database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-184">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a9445-184">-ServiceObjectiveName</span></span>
<span data-ttu-id="a9445-185">서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-185">Specifies the name of the service objective.</span></span>

```yaml
Type: System.String
Parameter Sets: FromPointInTimeBackup, FromDeletedDatabaseBackup, FromGeoBackup, FromLongTermRetentionBackup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-186">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9445-186">-TargetDatabaseName</span></span>
<span data-ttu-id="a9445-187">복원할 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-187">Specifies the name of the database to restore to.</span></span>

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

### <span data-ttu-id="a9445-188">-VCore</span><span class="sxs-lookup"><span data-stu-id="a9445-188">-VCore</span></span>
<span data-ttu-id="a9445-189">복원된 Azure Sql Database의 Vcore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-189">The Vcore numbers of the restored Azure Sql Database.</span></span>

```yaml
Type: System.Int32
Parameter Sets: FromPointInTimeBackupWithVcore, FromDeletedDatabaseBackupWithVcore, FromGeoBackupWithVcore, FromLongTermRetentionBackupWithVcore
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9445-190">-Confirm</span></span>
<span data-ttu-id="a9445-191">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-191">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9445-192">-WhatIf</span></span>
<span data-ttu-id="a9445-193">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a9445-193">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9445-194">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-194">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9445-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9445-195">CommonParameters</span></span>
<span data-ttu-id="a9445-196">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9445-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9445-197">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9445-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9445-198">입력</span><span class="sxs-lookup"><span data-stu-id="a9445-198">INPUTS</span></span>

### <span data-ttu-id="a9445-199">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="a9445-199">System.DateTime</span></span>

### <span data-ttu-id="a9445-200">System.String</span><span class="sxs-lookup"><span data-stu-id="a9445-200">System.String</span></span>

## <span data-ttu-id="a9445-201">출력</span><span class="sxs-lookup"><span data-stu-id="a9445-201">OUTPUTS</span></span>

### <span data-ttu-id="a9445-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a9445-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a9445-203">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9445-203">NOTES</span></span>

## <span data-ttu-id="a9445-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9445-204">RELATED LINKS</span></span>

[<span data-ttu-id="a9445-205">Azure SQL 데이터베이스를 정전으로부터 복구</span><span class="sxs-lookup"><span data-stu-id="a9445-205">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="a9445-206">사용자 오류에서 Azure SQL 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="a9445-206">Recover an Azure SQL Database from a user error</span></span>](http://go.microsoft.com/fwlink/?LinkId=746944)

[<span data-ttu-id="a9445-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9445-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a9445-208">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-208">Get-AzSqlDatabaseGeoBackup</span></span>](./Get-AzSqlDatabaseGeoBackup.md)

[<span data-ttu-id="a9445-209">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a9445-209">Get-AzSqlDeletedDatabaseBackup</span></span>](./Get-AzSqlDeletedDatabaseBackup.md)

[<span data-ttu-id="a9445-210">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a9445-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
