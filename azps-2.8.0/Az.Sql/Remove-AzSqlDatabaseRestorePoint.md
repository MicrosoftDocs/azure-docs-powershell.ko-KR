---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 0351e720d2f9a93a8c3a4a220c6a4d8844ebfecd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873861"
---
# <span data-ttu-id="9e561-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="9e561-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="9e561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e561-102">SYNOPSIS</span></span>
<span data-ttu-id="9e561-103">SQL 데이터베이스에서 지정 된 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="9e561-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e561-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e561-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e561-105">DESCRIPTION</span></span>
<span data-ttu-id="9e561-106">**AzSqlDatabaseRestorePoint** Cmdlet은 Azure SQL 데이터베이스에서 지정 된 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="9e561-107">이 cmdlet은 Azure SQL Database의 SQL Server Datawarehouse 서비스에서 현재 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="9e561-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9e561-108">EXAMPLES</span></span>

### <span data-ttu-id="9e561-109">예제 1: 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="9e561-110">이 명령은 Azure SQL Database에서 제공 된 생성 날짜에 대 한 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="9e561-111">변수</span><span class="sxs-lookup"><span data-stu-id="9e561-111">PARAMETERS</span></span>

### <span data-ttu-id="9e561-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9e561-112">-DatabaseName</span></span>
<span data-ttu-id="9e561-113">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="9e561-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e561-114">-DefaultProfile</span></span>
<span data-ttu-id="9e561-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e561-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e561-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e561-116">-PassThru</span></span>
<span data-ttu-id="9e561-117">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="9e561-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9e561-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e561-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e561-119">SQL 데이터베이스를 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="9e561-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="9e561-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="9e561-121">복원 시점 만든 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e561-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e561-122">-ServerName</span></span>
<span data-ttu-id="9e561-123">데이터베이스를 호스트 하는 AzureSQL 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="9e561-124">-확인</span><span class="sxs-lookup"><span data-stu-id="9e561-124">-Confirm</span></span>
<span data-ttu-id="9e561-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e561-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e561-126">-WhatIf</span></span>
<span data-ttu-id="9e561-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e561-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e561-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e561-129">CommonParameters</span></span>
<span data-ttu-id="9e561-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e561-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e561-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e561-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e561-132">입력</span><span class="sxs-lookup"><span data-stu-id="9e561-132">INPUTS</span></span>

### <span data-ttu-id="9e561-133">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="9e561-133">System.DateTime</span></span>

### <span data-ttu-id="9e561-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9e561-134">System.String</span></span>

## <span data-ttu-id="9e561-135">출력</span><span class="sxs-lookup"><span data-stu-id="9e561-135">OUTPUTS</span></span>

### <span data-ttu-id="9e561-136">AzureSqlDatabaseRestorePointModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="9e561-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="9e561-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9e561-137">NOTES</span></span>

## <span data-ttu-id="9e561-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e561-138">RELATED LINKS</span></span>