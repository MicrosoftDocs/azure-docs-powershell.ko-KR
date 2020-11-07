---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: ce7bf498dc005f6cae8bfff28f0e470cacff71ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873728"
---
# <span data-ttu-id="ce266-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce266-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="ce266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce266-102">SYNOPSIS</span></span>
<span data-ttu-id="ce266-103">데이터베이스 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="ce266-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce266-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce266-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce266-105">DESCRIPTION</span></span>
<span data-ttu-id="ce266-106">**AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="ce266-107">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="ce266-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ce266-108">EXAMPLES</span></span>

### <span data-ttu-id="ce266-109">예제 1: 장기 보존 정책의 현재 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="ce266-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="ce266-110">이 명령은 database01에 대 한 장기 보존 정책의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="ce266-111">변수</span><span class="sxs-lookup"><span data-stu-id="ce266-111">PARAMETERS</span></span>

### <span data-ttu-id="ce266-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce266-112">-DatabaseName</span></span>
<span data-ttu-id="ce266-113">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="ce266-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce266-114">-DefaultProfile</span></span>
<span data-ttu-id="ce266-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce266-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce266-116">-ResourceGroupName</span></span>
<span data-ttu-id="ce266-117">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce266-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce266-118">-ServerName</span></span>
<span data-ttu-id="ce266-119">데이터베이스가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="ce266-120">-확인</span><span class="sxs-lookup"><span data-stu-id="ce266-120">-Confirm</span></span>
<span data-ttu-id="ce266-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce266-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce266-122">-WhatIf</span></span>
<span data-ttu-id="ce266-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce266-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce266-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce266-125">CommonParameters</span></span>
<span data-ttu-id="ce266-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce266-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce266-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce266-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce266-128">입력</span><span class="sxs-lookup"><span data-stu-id="ce266-128">INPUTS</span></span>

### <span data-ttu-id="ce266-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce266-129">System.String</span></span>

## <span data-ttu-id="ce266-130">출력</span><span class="sxs-lookup"><span data-stu-id="ce266-130">OUTPUTS</span></span>

### <span data-ttu-id="ce266-131">AzureSqlDatabaseBackupLongTermRetentionPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="ce266-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="ce266-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ce266-132">NOTES</span></span>

## <span data-ttu-id="ce266-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce266-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce266-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ce266-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ce266-135">제거-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ce266-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ce266-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce266-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ce266-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ce266-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)