---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370574"
---
# <span data-ttu-id="fb3fe-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="fb3fe-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="fb3fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3fe-103">관리되는 SQL 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="fb3fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb3fe-104">SYNTAX</span></span>

### <span data-ttu-id="fb3fe-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb3fe-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3fe-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3fe-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3fe-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3fe-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3fe-108">설명</span><span class="sxs-lookup"><span data-stu-id="fb3fe-108">DESCRIPTION</span></span>
<span data-ttu-id="fb3fe-109">이 Stop-AzSqlInstanceOperation cmdlet은 관리되는 인스턴스에서 제공된 작업 이름을 SQL 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="fb3fe-110">예제</span><span class="sxs-lookup"><span data-stu-id="fb3fe-110">EXAMPLES</span></span>

### <span data-ttu-id="fb3fe-111">예제 1: 특정 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="fb3fe-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="fb3fe-112">이 명령은 관리되는 인스턴스에서 이름이 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9'인 SQL 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="fb3fe-113">예제 2: 작업 리소스 ID 사용</span><span class="sxs-lookup"><span data-stu-id="fb3fe-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="fb3fe-114">이 명령은 리소스 ID $managedInstanceOperation.Id.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="fb3fe-115">예제 3: 작업 개체 사용</span><span class="sxs-lookup"><span data-stu-id="fb3fe-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="fb3fe-116">이 명령은 개체가 있는 작업을 $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="fb3fe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb3fe-117">PARAMETERS</span></span>

### <span data-ttu-id="fb3fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3fe-118">-DefaultProfile</span></span>
<span data-ttu-id="fb3fe-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb3fe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fb3fe-120">-Force</span></span>
<span data-ttu-id="fb3fe-121">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="fb3fe-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fb3fe-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb3fe-122">-InputObject</span></span>
<span data-ttu-id="fb3fe-123">취소할 작업</span><span class="sxs-lookup"><span data-stu-id="fb3fe-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3fe-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="fb3fe-124">-ManagedInstanceName</span></span>
<span data-ttu-id="fb3fe-125">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3fe-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fb3fe-126">-Name</span></span>
<span data-ttu-id="fb3fe-127">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb3fe-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb3fe-130">-ResourceId</span></span>
<span data-ttu-id="fb3fe-131">중지할 작업 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fb3fe-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb3fe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb3fe-132">-Confirm</span></span>
<span data-ttu-id="fb3fe-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3fe-134">-WhatIf</span></span>
<span data-ttu-id="fb3fe-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb3fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3fe-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3fe-137">CommonParameters</span></span>
<span data-ttu-id="fb3fe-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3fe-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb3fe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3fe-140">입력</span><span class="sxs-lookup"><span data-stu-id="fb3fe-140">INPUTS</span></span>

### <span data-ttu-id="fb3fe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fb3fe-141">System.String</span></span>

### <span data-ttu-id="fb3fe-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="fb3fe-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="fb3fe-143">출력</span><span class="sxs-lookup"><span data-stu-id="fb3fe-143">OUTPUTS</span></span>

### <span data-ttu-id="fb3fe-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="fb3fe-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="fb3fe-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb3fe-145">NOTES</span></span>

## <span data-ttu-id="fb3fe-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb3fe-146">RELATED LINKS</span></span>