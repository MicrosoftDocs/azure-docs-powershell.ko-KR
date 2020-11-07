---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: 3db29e4ab0f2ab4afc9a3c29ef8ea0335ed5d528
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873936"
---
# <span data-ttu-id="9e547-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="9e547-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="9e547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e547-102">SYNOPSIS</span></span>
<span data-ttu-id="9e547-103">Azure SQL 관리 인스턴스 데이터베이스 중복 백업에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="9e547-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e547-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e547-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e547-105">DESCRIPTION</span></span>
<span data-ttu-id="9e547-106">**AzSqlInstanceDatabaseGeoBackup** Cmdlet은 Azure Sql Database 관리 인스턴스에서 하나 이상의 azure sql database 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="9e547-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e547-107">EXAMPLES</span></span>

### <span data-ttu-id="9e547-108">예제 1: 인스턴스에 모든 데이터베이스 중복 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e547-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="9e547-109">이 명령은 managedInstance1 이라는 인스턴스의 모든 데이터베이스 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="9e547-110">예제 2: 관리 되는 인스턴스에서 이름으로 데이터베이스 중복 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e547-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="9e547-111">이 명령은 managedInstance1 라는 인스턴스에서 managedDatabase1 라는 데이터베이스 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="9e547-112">예제 3: 필터링을 사용 하 여 인스턴스에 대 한 모든 데이터베이스 중복 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="9e547-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="9e547-113">이 명령은 "managedDatabase"로 시작 하는 managedInstance1 라는 인스턴스에 대 한 모든 데이터베이스 중복 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="9e547-114">변수</span><span class="sxs-lookup"><span data-stu-id="9e547-114">PARAMETERS</span></span>

### <span data-ttu-id="9e547-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e547-115">-DefaultProfile</span></span>
<span data-ttu-id="9e547-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e547-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9e547-117">-InstanceName</span></span>
<span data-ttu-id="9e547-118">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-118">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e547-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9e547-119">-Name</span></span>
<span data-ttu-id="9e547-120">검색할 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9e547-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e547-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e547-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e547-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e547-123">CommonParameters</span></span>
<span data-ttu-id="9e547-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e547-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e547-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e547-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e547-126">입력</span><span class="sxs-lookup"><span data-stu-id="9e547-126">INPUTS</span></span>

### <span data-ttu-id="9e547-127">않아야</span><span class="sxs-lookup"><span data-stu-id="9e547-127">None</span></span>

## <span data-ttu-id="9e547-128">출력</span><span class="sxs-lookup"><span data-stu-id="9e547-128">OUTPUTS</span></span>

### <span data-ttu-id="9e547-129">AzureSqlRecoverableManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="9e547-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="9e547-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9e547-130">NOTES</span></span>

## <span data-ttu-id="9e547-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e547-131">RELATED LINKS</span></span>