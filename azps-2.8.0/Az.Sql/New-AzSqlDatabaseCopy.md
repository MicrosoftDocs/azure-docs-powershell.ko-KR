---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: aa2ba844e364d1c95274573a6b1b38e4550c70f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873619"
---
# <span data-ttu-id="24bcd-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="24bcd-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="24bcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="24bcd-103">현재 시간에 스냅숏을 사용 하는 SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="24bcd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24bcd-104">SYNTAX</span></span>

### <span data-ttu-id="24bcd-105">DtuBasedDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="24bcd-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24bcd-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="24bcd-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24bcd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24bcd-107">DESCRIPTION</span></span>
<span data-ttu-id="24bcd-108">**AzSqlDatabaseCopy** cmdlet은 현재 시간에 데이터의 스냅숏을 사용 하는 Azure SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="24bcd-109">Start-AzSqlDatabaseCopy cmdlet 대신이 cmdlet을 사용 하 여 일회성 데이터베이스 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="24bcd-110">이 cmdlet은 복사본의 **데이터베이스** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="24bcd-111">참고: New-AzSqlDatabaseSecondary cmdlet을 사용 하 여 데이터베이스에 대 한 지리적 복제를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="24bcd-112">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="24bcd-113">예제의</span><span class="sxs-lookup"><span data-stu-id="24bcd-113">EXAMPLES</span></span>

## <span data-ttu-id="24bcd-114">변수</span><span class="sxs-lookup"><span data-stu-id="24bcd-114">PARAMETERS</span></span>

### <span data-ttu-id="24bcd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24bcd-115">-AsJob</span></span>
<span data-ttu-id="24bcd-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="24bcd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24bcd-117">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="24bcd-117">-ComputeGeneration</span></span>
<span data-ttu-id="24bcd-118">새 복사본에 할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="24bcd-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="24bcd-119">-CopyDatabaseName</span></span>
<span data-ttu-id="24bcd-120">SQL 데이터베이스 복사본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="24bcd-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24bcd-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="24bcd-122">복사본을 할당할 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="24bcd-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="24bcd-123">-CopyServerName</span></span>
<span data-ttu-id="24bcd-124">복사본을 호스트 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="24bcd-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24bcd-125">-DatabaseName</span></span>
<span data-ttu-id="24bcd-126">복사할 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="24bcd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bcd-127">-DefaultProfile</span></span>
<span data-ttu-id="24bcd-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24bcd-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24bcd-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="24bcd-129">-ElasticPoolName</span></span>
<span data-ttu-id="24bcd-130">복사본을 할당할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="24bcd-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="24bcd-131">-LicenseType</span></span>
<span data-ttu-id="24bcd-132">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="24bcd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24bcd-133">-ResourceGroupName</span></span>
<span data-ttu-id="24bcd-134">복사할 데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="24bcd-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24bcd-135">-ServerName</span></span>
<span data-ttu-id="24bcd-136">복사할 데이터베이스를 포함 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="24bcd-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="24bcd-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="24bcd-138">복사본에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="24bcd-139">태그</span><span class="sxs-lookup"><span data-stu-id="24bcd-139">-Tags</span></span>
<span data-ttu-id="24bcd-140">Azure SQL 데이터베이스 복사본과 연결할 해시 테이블 형태의 키-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="24bcd-141">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="24bcd-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24bcd-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="24bcd-142">-VCore</span></span>
<span data-ttu-id="24bcd-143">Azure Sql 데이터베이스 복사본의 Vcore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bcd-144">-확인</span><span class="sxs-lookup"><span data-stu-id="24bcd-144">-Confirm</span></span>
<span data-ttu-id="24bcd-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24bcd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24bcd-146">-WhatIf</span></span>
<span data-ttu-id="24bcd-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24bcd-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24bcd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bcd-149">CommonParameters</span></span>
<span data-ttu-id="24bcd-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24bcd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bcd-151">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24bcd-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bcd-152">입력</span><span class="sxs-lookup"><span data-stu-id="24bcd-152">INPUTS</span></span>

### <span data-ttu-id="24bcd-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24bcd-153">System.String</span></span>

## <span data-ttu-id="24bcd-154">출력</span><span class="sxs-lookup"><span data-stu-id="24bcd-154">OUTPUTS</span></span>

### <span data-ttu-id="24bcd-155">AzureSqlDatabaseCopyModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="24bcd-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="24bcd-156">상속자</span><span class="sxs-lookup"><span data-stu-id="24bcd-156">NOTES</span></span>

## <span data-ttu-id="24bcd-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24bcd-157">RELATED LINKS</span></span>

[<span data-ttu-id="24bcd-158">새로운 AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="24bcd-158">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="24bcd-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="24bcd-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)