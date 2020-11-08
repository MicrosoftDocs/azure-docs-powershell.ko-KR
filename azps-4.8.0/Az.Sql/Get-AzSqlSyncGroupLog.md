---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgrouplog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroupLog.md
ms.openlocfilehash: f8e73860d87d9389f2099a29039d90e0ac0534d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213227"
---
# <span data-ttu-id="28406-101">Get-AzSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="28406-101">Get-AzSqlSyncGroupLog</span></span>

## <span data-ttu-id="28406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28406-102">SYNOPSIS</span></span>
<span data-ttu-id="28406-103">Azure SQL 데이터베이스 동기화 그룹의 로그를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28406-103">Returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="28406-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28406-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroupLog [-SyncGroupName] <String> -StartTime <DateTime> [-EndTime <DateTime>]
 [-LogLevel <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28406-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28406-105">DESCRIPTION</span></span>
<span data-ttu-id="28406-106">**AzSqlSyncGroupLog** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹의 로그를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28406-106">The **Get-AzSqlSyncGroupLog** cmdlet returns the logs of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="28406-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28406-107">EXAMPLES</span></span>

### <span data-ttu-id="28406-108">예제 1: Azure SQL 동기화 그룹의 로그 가져오기</span><span class="sxs-lookup"><span data-stu-id="28406-108">Example 1: Get the logs of an Azure SQL Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroupLog -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -StartTime "9/16/2016 11:31:12" -EndTime "9/16/2016 12:31:00" -LogLevel "All"
TimeStamp            LogLevel Details                                   Source
---------            -------- -------                                   ------
6/13/2017 9:14:26 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
6/13/2017 7:11:59 AM Success  Schema information obtained successfully. fangltest2.database.windows.net/fangltest
```

<span data-ttu-id="28406-109">이 명령은 Azure SQL 동기화 그룹의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28406-109">This command gets the logs of an Azure SQL Sync Group.</span></span>

## <span data-ttu-id="28406-110">변수</span><span class="sxs-lookup"><span data-stu-id="28406-110">PARAMETERS</span></span>

### <span data-ttu-id="28406-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28406-111">-DatabaseName</span></span>
<span data-ttu-id="28406-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="28406-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28406-113">-DefaultProfile</span></span>
<span data-ttu-id="28406-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="28406-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28406-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="28406-115">-EndTime</span></span>
<span data-ttu-id="28406-116">쿼리할 로그의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-116">The end time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28406-117">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="28406-117">-LogLevel</span></span>
<span data-ttu-id="28406-118">쿼리할 로그의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-118">The type of the logs to query.</span></span>
<span data-ttu-id="28406-119">유효한 값은 ' Error ', ' Warning ', ' Success ' 및 ' All '입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-119">Valid values are: 'Error', 'Warning', 'Success' and 'All'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Success, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28406-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28406-120">-ResourceGroupName</span></span>
<span data-ttu-id="28406-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="28406-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28406-122">-ServerName</span></span>
<span data-ttu-id="28406-123">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="28406-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="28406-124">-StartTime</span></span>
<span data-ttu-id="28406-125">쿼리할 로그의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-125">The start time of the logs to query.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28406-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="28406-126">-SyncGroupName</span></span>
<span data-ttu-id="28406-127">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28406-127">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28406-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28406-128">CommonParameters</span></span>
<span data-ttu-id="28406-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28406-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28406-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28406-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28406-131">입력</span><span class="sxs-lookup"><span data-stu-id="28406-131">INPUTS</span></span>

### <span data-ttu-id="28406-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28406-132">System.String</span></span>

## <span data-ttu-id="28406-133">출력</span><span class="sxs-lookup"><span data-stu-id="28406-133">OUTPUTS</span></span>

### <span data-ttu-id="28406-134">AzureSqlSyncGroupLogModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="28406-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupLogModel</span></span>

## <span data-ttu-id="28406-135">상속자</span><span class="sxs-lookup"><span data-stu-id="28406-135">NOTES</span></span>

## <span data-ttu-id="28406-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28406-136">RELATED LINKS</span></span>