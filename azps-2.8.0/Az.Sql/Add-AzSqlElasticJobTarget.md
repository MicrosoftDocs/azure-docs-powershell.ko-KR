---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: d1788abc6ac0546732fe2476cf2822210a1fa8da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871469"
---
# <span data-ttu-id="da0a6-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="da0a6-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="da0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="da0a6-103">대상 그룹에 대상을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-103">Adds a target to a target group</span></span>

## <span data-ttu-id="da0a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da0a6-104">SYNTAX</span></span>

### <span data-ttu-id="da0a6-105">SqlDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="da0a6-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="da0a6-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da0a6-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="da0a6-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="da0a6-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="da0a6-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="da0a6-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da0a6-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da0a6-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da0a6-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da0a6-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da0a6-114">설명은</span><span class="sxs-lookup"><span data-stu-id="da0a6-114">DESCRIPTION</span></span>
<span data-ttu-id="da0a6-115">Add-AzSqlElasticJobTarget cmdlet이 대상 그룹에 대상 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="da0a6-116">예제의</span><span class="sxs-lookup"><span data-stu-id="da0a6-116">EXAMPLES</span></span>

### <span data-ttu-id="da0a6-117">예제 1-서버 대상 추가</span><span class="sxs-lookup"><span data-stu-id="da0a6-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="da0a6-118">예제 2-데이터베이스 대상 추가</span><span class="sxs-lookup"><span data-stu-id="da0a6-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="da0a6-119">예제 3-탄력적 풀 대상 추가</span><span class="sxs-lookup"><span data-stu-id="da0a6-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="da0a6-120">예제 4-샤 드 맵 대상 추가</span><span class="sxs-lookup"><span data-stu-id="da0a6-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="da0a6-121">대상 그룹에 대상 (서버, 탄력적 풀, 데이터베이스 및 샤 드 맵)을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="da0a6-122">변수</span><span class="sxs-lookup"><span data-stu-id="da0a6-122">PARAMETERS</span></span>

### <span data-ttu-id="da0a6-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="da0a6-123">-AgentName</span></span>
<span data-ttu-id="da0a6-124">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="da0a6-125">-AgentServerName</span></span>
<span data-ttu-id="da0a6-126">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da0a6-127">-DatabaseName</span></span>
<span data-ttu-id="da0a6-128">데이터베이스 대상 이름</span><span class="sxs-lookup"><span data-stu-id="da0a6-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0a6-129">-DefaultProfile</span></span>
<span data-ttu-id="da0a6-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da0a6-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="da0a6-131">-ElasticPoolName</span></span>
<span data-ttu-id="da0a6-132">탄력적 풀 대상 이름</span><span class="sxs-lookup"><span data-stu-id="da0a6-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="da0a6-133">-Exclude</span></span>
<span data-ttu-id="da0a6-134">대상을 제외 합니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="da0a6-135">-ParentObject</span></span>
<span data-ttu-id="da0a6-136">대상 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="da0a6-137">-ParentResourceId</span></span>
<span data-ttu-id="da0a6-138">대상 그룹 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="da0a6-139">-RefreshCredentialName</span></span>
<span data-ttu-id="da0a6-140">자격 증명 이름 새로 고침</span><span class="sxs-lookup"><span data-stu-id="da0a6-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0a6-141">-ResourceGroupName</span></span>
<span data-ttu-id="da0a6-142">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="da0a6-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da0a6-143">-ServerName</span></span>
<span data-ttu-id="da0a6-144">서버 대상 이름</span><span class="sxs-lookup"><span data-stu-id="da0a6-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="da0a6-145">-ShardMapName</span></span>
<span data-ttu-id="da0a6-146">샤 드 맵 대상 이름</span><span class="sxs-lookup"><span data-stu-id="da0a6-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="da0a6-147">-TargetGroupName</span></span>
<span data-ttu-id="da0a6-148">대상 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0a6-149">-확인</span><span class="sxs-lookup"><span data-stu-id="da0a6-149">-Confirm</span></span>
<span data-ttu-id="da0a6-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0a6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0a6-151">-WhatIf</span></span>
<span data-ttu-id="da0a6-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da0a6-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0a6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0a6-154">CommonParameters</span></span>
<span data-ttu-id="da0a6-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da0a6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0a6-156">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da0a6-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0a6-157">입력</span><span class="sxs-lookup"><span data-stu-id="da0a6-157">INPUTS</span></span>

### <span data-ttu-id="da0a6-158">ElasticJobs. AzureSqlElasticJobTargetGroupModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="da0a6-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="da0a6-159">출력</span><span class="sxs-lookup"><span data-stu-id="da0a6-159">OUTPUTS</span></span>

### <span data-ttu-id="da0a6-160">Microsoft. Azure. 관리 대상</span><span class="sxs-lookup"><span data-stu-id="da0a6-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="da0a6-161">상속자</span><span class="sxs-lookup"><span data-stu-id="da0a6-161">NOTES</span></span>

## <span data-ttu-id="da0a6-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da0a6-162">RELATED LINKS</span></span>