---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 7a5ecbb21af23b31b321ef1568c2eb953a548cf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874035"
---
# <span data-ttu-id="0c110-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0c110-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="0c110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c110-102">SYNOPSIS</span></span>
<span data-ttu-id="0c110-103">SQL 데이터 웨어하우스 데이터베이스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="0c110-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c110-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c110-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0c110-105">DESCRIPTION</span></span>
<span data-ttu-id="0c110-106">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="0c110-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0c110-107">EXAMPLES</span></span>

### <span data-ttu-id="0c110-108">예제 1: Azure SQL Data Warehouse 데이터베이스 일시 중단</span><span class="sxs-lookup"><span data-stu-id="0c110-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0c110-109">이 명령은 활성 Azure SQL 데이터 웨어하우스 데이터베이스를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="0c110-110">변수</span><span class="sxs-lookup"><span data-stu-id="0c110-110">PARAMETERS</span></span>

### <span data-ttu-id="0c110-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c110-111">-AsJob</span></span>
<span data-ttu-id="0c110-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0c110-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c110-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0c110-113">-DatabaseName</span></span>
<span data-ttu-id="0c110-114">이 cmdlet이 일시 중단 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="0c110-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c110-115">-DefaultProfile</span></span>
<span data-ttu-id="0c110-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c110-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c110-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c110-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c110-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0c110-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0c110-119">-ServerName</span></span>
<span data-ttu-id="0c110-120">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="0c110-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0c110-121">-Confirm</span></span>
<span data-ttu-id="0c110-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c110-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c110-123">-WhatIf</span></span>
<span data-ttu-id="0c110-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c110-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c110-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c110-126">CommonParameters</span></span>
<span data-ttu-id="0c110-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c110-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c110-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c110-129">입력</span><span class="sxs-lookup"><span data-stu-id="0c110-129">INPUTS</span></span>

### <span data-ttu-id="0c110-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c110-130">System.String</span></span>

## <span data-ttu-id="0c110-131">출력</span><span class="sxs-lookup"><span data-stu-id="0c110-131">OUTPUTS</span></span>

### <span data-ttu-id="0c110-132">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="0c110-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="0c110-133">상속자</span><span class="sxs-lookup"><span data-stu-id="0c110-133">NOTES</span></span>
* <span data-ttu-id="0c110-134">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="0c110-135">이 작업은 Azure SQL Database Basic, Standard 및 Premium edition에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c110-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="0c110-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c110-136">RELATED LINKS</span></span>

[<span data-ttu-id="0c110-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0c110-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0c110-138">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0c110-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="0c110-139">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0c110-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="0c110-140">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0c110-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0c110-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0c110-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="0c110-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="0c110-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

