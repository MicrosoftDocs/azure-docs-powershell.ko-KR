---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: f22730e39a1b53cfea8181163dd770c67dc598a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529355"
---
# <span data-ttu-id="7f0b4-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="7f0b4-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="7f0b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0b4-103">데이터베이스의 지역 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f0b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f0b4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f0b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f0b4-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0b4-106">**AzureRMSqlDatabaseGeoBackup** cmdlet은 지정 된 서버에서 SQL 데이터베이스 또는 사용 가능한 모든 지역 중복 백업의 지정 된 지역 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="7f0b4-107">지역 중복 백업은 별도의 지리적 위치에서 데이터 파일을 사용 하 여 restorable 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="7f0b4-108">지역 정전이 발생 한 경우에 Geo-Restore을 사용 하 여 지역 중복 백업을 복원 하 여 데이터베이스를 새 영역으로 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="7f0b4-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7f0b4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7f0b4-110">EXAMPLES</span></span>

### <span data-ttu-id="7f0b4-111">예제 1: 서버에서 모든 지역 중복 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f0b4-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="7f0b4-112">이 명령은 지정 된 서버에서 사용 가능한 모든 지역 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="7f0b4-113">예제 2: 지정 된 지역 중복 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="7f0b4-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="7f0b4-114">이 명령은 ContosoDatabase 이라는 데이터베이스 지역 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="7f0b4-115">변수</span><span class="sxs-lookup"><span data-stu-id="7f0b4-115">PARAMETERS</span></span>

### <span data-ttu-id="7f0b4-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f0b4-116">-DatabaseName</span></span>
<span data-ttu-id="7f0b4-117">가져올 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-117">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="7f0b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0b4-118">-DefaultProfile</span></span>
<span data-ttu-id="7f0b4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7f0b4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f0b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f0b4-121">SQL 데이터베이스 서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="7f0b4-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f0b4-122">-ServerName</span></span>
<span data-ttu-id="7f0b4-123">복원할 백업을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-123">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="7f0b4-124">-확인</span><span class="sxs-lookup"><span data-stu-id="7f0b4-124">-Confirm</span></span>
<span data-ttu-id="7f0b4-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f0b4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f0b4-126">-WhatIf</span></span>
<span data-ttu-id="7f0b4-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f0b4-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f0b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0b4-129">CommonParameters</span></span>
<span data-ttu-id="7f0b4-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f0b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0b4-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0b4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0b4-132">입력</span><span class="sxs-lookup"><span data-stu-id="7f0b4-132">INPUTS</span></span>

### <span data-ttu-id="7f0b4-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7f0b4-133">System.String</span></span>

## <span data-ttu-id="7f0b4-134">출력</span><span class="sxs-lookup"><span data-stu-id="7f0b4-134">OUTPUTS</span></span>

### <span data-ttu-id="7f0b4-135">AzureSqlDatabaseGeoBackupModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="7f0b4-135">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="7f0b4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="7f0b4-136">NOTES</span></span>

## <span data-ttu-id="7f0b4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f0b4-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f0b4-138">개요: SQL 데이터베이스를 사용 하 여 클라우드 비즈니스 연속성 및 데이터베이스 재해 복구</span><span class="sxs-lookup"><span data-stu-id="7f0b4-138">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="7f0b4-139">작동 중지에서 Azure SQL 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="7f0b4-139">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="7f0b4-140">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7f0b4-140">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="7f0b4-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7f0b4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)