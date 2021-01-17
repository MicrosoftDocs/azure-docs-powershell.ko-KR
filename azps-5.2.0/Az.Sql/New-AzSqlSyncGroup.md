---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361509"
---
# <span data-ttu-id="37e83-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="37e83-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="37e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37e83-102">SYNOPSIS</span></span>
<span data-ttu-id="37e83-103">Azure SQL 데이터베이스 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="37e83-104">구문</span><span class="sxs-lookup"><span data-stu-id="37e83-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e83-105">설명</span><span class="sxs-lookup"><span data-stu-id="37e83-105">DESCRIPTION</span></span>
<span data-ttu-id="37e83-106">**New-AzSqlSyncGroup** cmdlet은 Azure SQL 데이터베이스 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="37e83-107">예제</span><span class="sxs-lookup"><span data-stu-id="37e83-107">EXAMPLES</span></span>

### <span data-ttu-id="37e83-108">예제 1: Azure SQL 데이터베이스용 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="37e83-109">이 명령은 Azure SQL 데이터베이스용 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="37e83-110">"schema.json"은 로컬 디스크의 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="37e83-111">json 형식의 Schema 페이로드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="37e83-112">schema json의 예: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="37e83-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="37e83-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37e83-113">PARAMETERS</span></span>

### <span data-ttu-id="37e83-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="37e83-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="37e83-115">동기화 그룹의 허브와 멤버 데이터베이스 간의 충돌을 해결하는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e83-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="37e83-116">-DatabaseCredential</span></span>
<span data-ttu-id="37e83-117">허브 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e83-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37e83-118">-DatabaseName</span></span>
<span data-ttu-id="37e83-119">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="37e83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e83-120">-DefaultProfile</span></span>
<span data-ttu-id="37e83-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="37e83-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37e83-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="37e83-122">-IntervalInSeconds</span></span>
<span data-ttu-id="37e83-123">데이터 동기화를 수행한 빈도(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="37e83-124">기본값은 -1입니다. 즉, 자동 동기화가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e83-125">-Name</span><span class="sxs-lookup"><span data-stu-id="37e83-125">-Name</span></span>
<span data-ttu-id="37e83-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e83-127">-ResourceGroupName</span></span>
<span data-ttu-id="37e83-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="37e83-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="37e83-129">-SchemaFile</span></span>
<span data-ttu-id="37e83-130">schema 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="37e83-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37e83-131">-ServerName</span></span>
<span data-ttu-id="37e83-132">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="37e83-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="37e83-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="37e83-133">-SyncDatabaseName</span></span>
<span data-ttu-id="37e83-134">동기화 관련 메타데이터를 저장하는 데 사용되는 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="37e83-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e83-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="37e83-136">동기화 메타데이터 데이터베이스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="37e83-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="37e83-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="37e83-138">동기화 메타데이터 데이터베이스가 호스트되는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="37e83-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="37e83-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="37e83-140">이 동기화 그룹의 허브에 연결할 때 개인 링크 연결을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="37e83-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

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

### <span data-ttu-id="37e83-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37e83-141">-Confirm</span></span>
<span data-ttu-id="37e83-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e83-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e83-143">-WhatIf</span></span>
<span data-ttu-id="37e83-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37e83-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e83-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e83-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e83-146">CommonParameters</span></span>
<span data-ttu-id="37e83-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37e83-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e83-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37e83-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e83-149">입력</span><span class="sxs-lookup"><span data-stu-id="37e83-149">INPUTS</span></span>

### <span data-ttu-id="37e83-150">System.String</span><span class="sxs-lookup"><span data-stu-id="37e83-150">System.String</span></span>

## <span data-ttu-id="37e83-151">출력</span><span class="sxs-lookup"><span data-stu-id="37e83-151">OUTPUTS</span></span>

### <span data-ttu-id="37e83-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="37e83-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="37e83-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37e83-153">NOTES</span></span>

## <span data-ttu-id="37e83-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37e83-154">RELATED LINKS</span></span>

[<span data-ttu-id="37e83-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="37e83-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="37e83-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="37e83-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="37e83-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="37e83-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)
