---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: ad0103e2a4d529a4f306749a1d55ca0b6eadc013
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873862"
---
# <span data-ttu-id="cd6e8-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd6e8-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="cd6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6e8-103">Azure SQL 데이터베이스의 감사 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="cd6e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd6e8-104">SYNTAX</span></span>

### <span data-ttu-id="cd6e8-105">DatabaseParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd6e8-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd6e8-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd6e8-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd6e8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cd6e8-107">DESCRIPTION</span></span>
<span data-ttu-id="cd6e8-108">**AzSqlDatabaseAudit** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="cd6e8-109">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="cd6e8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cd6e8-110">EXAMPLES</span></span>

### <span data-ttu-id="cd6e8-111">예제 1: Azure SQL 데이터베이스의 감사 설정 제거</span><span class="sxs-lookup"><span data-stu-id="cd6e8-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="cd6e8-112">예제 2: Azure SQL 데이터베이스의 감사 설정, 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="cd6e8-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="cd6e8-113">변수</span><span class="sxs-lookup"><span data-stu-id="cd6e8-113">PARAMETERS</span></span>

### <span data-ttu-id="cd6e8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd6e8-114">-DatabaseName</span></span>
<span data-ttu-id="cd6e8-115">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e8-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cd6e8-116">-DatabaseObject</span></span>
<span data-ttu-id="cd6e8-117">감사 정책을 관리 하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6e8-118">-DefaultProfile</span></span>
<span data-ttu-id="cd6e8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd6e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd6e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="cd6e8-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e8-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd6e8-122">-ServerName</span></span>
<span data-ttu-id="cd6e8-123">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd6e8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="cd6e8-124">-Confirm</span></span>
<span data-ttu-id="cd6e8-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd6e8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd6e8-126">-WhatIf</span></span>
<span data-ttu-id="cd6e8-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd6e8-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd6e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6e8-129">CommonParameters</span></span>
<span data-ttu-id="cd6e8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6e8-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6e8-132">입력</span><span class="sxs-lookup"><span data-stu-id="cd6e8-132">INPUTS</span></span>

### <span data-ttu-id="cd6e8-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cd6e8-133">System.String</span></span>

### <span data-ttu-id="cd6e8-134">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="cd6e8-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cd6e8-135">출력</span><span class="sxs-lookup"><span data-stu-id="cd6e8-135">OUTPUTS</span></span>

### <span data-ttu-id="cd6e8-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cd6e8-136">System.Boolean</span></span>

## <span data-ttu-id="cd6e8-137">상속자</span><span class="sxs-lookup"><span data-stu-id="cd6e8-137">NOTES</span></span>

## <span data-ttu-id="cd6e8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd6e8-138">RELATED LINKS</span></span>