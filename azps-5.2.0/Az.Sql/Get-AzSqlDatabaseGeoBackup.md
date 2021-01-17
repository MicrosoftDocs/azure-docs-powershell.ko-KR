---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323175"
---
# <span data-ttu-id="06450-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="06450-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="06450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06450-102">SYNOPSIS</span></span>
<span data-ttu-id="06450-103">데이터베이스의 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="06450-104">구문</span><span class="sxs-lookup"><span data-stu-id="06450-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06450-105">설명</span><span class="sxs-lookup"><span data-stu-id="06450-105">DESCRIPTION</span></span>
<span data-ttu-id="06450-106">**Get-AzSqlDatabaseGeoBackup** cmdlet은 지정된 서버에서 SQL 데이터베이스 또는 사용 가능한 모든 지역 중복 백업의 지정된 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="06450-107">지역 중복 백업은 별도의 지리적 위치에서 데이터 파일을 사용하여 복원 가능한 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="06450-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="06450-108">데이터베이스를 Geo-Restore 지역 정전이 발생하면 지역 중복 백업을 복원하여 데이터베이스를 새 지역으로 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="06450-109">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="06450-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="06450-110">예제</span><span class="sxs-lookup"><span data-stu-id="06450-110">EXAMPLES</span></span>

### <span data-ttu-id="06450-111">예제 1: 서버에서 모든 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="06450-112">이 명령은 지정된 서버에서 사용 가능한 모든 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="06450-113">예제 2: 지정된 지역 중복 백업을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06450-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="06450-114">이 명령은 ContosoDatabase라는 데이터베이스 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="06450-115">예제 3: 필터링을 사용하여 서버에서 모든 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="06450-116">이 명령은 "Contoso"로 시작하는 지정된 서버에서 사용 가능한 모든 지역 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="06450-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06450-117">PARAMETERS</span></span>

### <span data-ttu-id="06450-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="06450-118">-DatabaseName</span></span>
<span data-ttu-id="06450-119">얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06450-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06450-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06450-120">-DefaultProfile</span></span>
<span data-ttu-id="06450-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06450-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06450-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06450-122">-ResourceGroupName</span></span>
<span data-ttu-id="06450-123">데이터베이스 서버가 할당된 리소스 SQL 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06450-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="06450-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="06450-124">-ServerName</span></span>
<span data-ttu-id="06450-125">복원할 백업을 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="06450-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="06450-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06450-126">-Confirm</span></span>
<span data-ttu-id="06450-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06450-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06450-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06450-128">-WhatIf</span></span>
<span data-ttu-id="06450-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06450-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06450-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06450-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06450-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06450-131">CommonParameters</span></span>
<span data-ttu-id="06450-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06450-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06450-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06450-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06450-134">입력</span><span class="sxs-lookup"><span data-stu-id="06450-134">INPUTS</span></span>

### <span data-ttu-id="06450-135">System.String</span><span class="sxs-lookup"><span data-stu-id="06450-135">System.String</span></span>

## <span data-ttu-id="06450-136">출력</span><span class="sxs-lookup"><span data-stu-id="06450-136">OUTPUTS</span></span>

### <span data-ttu-id="06450-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="06450-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="06450-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06450-138">NOTES</span></span>

## <span data-ttu-id="06450-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06450-139">RELATED LINKS</span></span>

[<span data-ttu-id="06450-140">개요: SQL Database를 통해 클라우드 비즈니스 연속성 및 데이터베이스 재해 복구</span><span class="sxs-lookup"><span data-stu-id="06450-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="06450-141">Azure SQL 데이터베이스를 정전으로부터 복구</span><span class="sxs-lookup"><span data-stu-id="06450-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="06450-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="06450-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="06450-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="06450-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)