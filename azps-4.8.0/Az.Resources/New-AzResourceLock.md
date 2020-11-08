---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204429"
---
# <span data-ttu-id="be54e-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="be54e-101">New-AzResourceLock</span></span>

## <span data-ttu-id="be54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be54e-102">SYNOPSIS</span></span>
<span data-ttu-id="be54e-103">리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-103">Creates a resource lock.</span></span>

## <span data-ttu-id="be54e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be54e-104">SYNTAX</span></span>

### <span data-ttu-id="be54e-105">BySpecifiedScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="be54e-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be54e-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be54e-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be54e-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="be54e-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be54e-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="be54e-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be54e-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="be54e-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be54e-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="be54e-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be54e-111">설명은</span><span class="sxs-lookup"><span data-stu-id="be54e-111">DESCRIPTION</span></span>
<span data-ttu-id="be54e-112">**AzResourceLock** cmdlet은 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="be54e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="be54e-113">EXAMPLES</span></span>

### <span data-ttu-id="be54e-114">예제 1: 웹 사이트에서 자원 잠금 만들기</span><span class="sxs-lookup"><span data-stu-id="be54e-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="be54e-115">이 명령은 웹 사이트에 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="be54e-116">예제 2: 데이터베이스에 리소스 잠금 만들기</span><span class="sxs-lookup"><span data-stu-id="be54e-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="be54e-117">이 명령은 Azure 데이터베이스에서 리소스 잠금을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="be54e-118">변수</span><span class="sxs-lookup"><span data-stu-id="be54e-118">PARAMETERS</span></span>

### <span data-ttu-id="be54e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be54e-119">-ApiVersion</span></span>
<span data-ttu-id="be54e-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="be54e-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="be54e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be54e-122">-DefaultProfile</span></span>
<span data-ttu-id="be54e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="be54e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be54e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="be54e-124">-Force</span></span>
<span data-ttu-id="be54e-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be54e-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="be54e-126">-LockId</span></span>
<span data-ttu-id="be54e-127">잠금의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-127">Specifies the ID of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="be54e-128">-LockLevel</span></span>
<span data-ttu-id="be54e-129">잠금의 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="be54e-130">현재 유효한 값은 CanNotDelete, ReadOnly입니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="be54e-131">-LockName</span></span>
<span data-ttu-id="be54e-132">잠금의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-132">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-133">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="be54e-133">-LockNotes</span></span>
<span data-ttu-id="be54e-134">잠금에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-134">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="be54e-135">-Pre</span></span>
<span data-ttu-id="be54e-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be54e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be54e-137">-ResourceGroupName</span></span>
<span data-ttu-id="be54e-138">잠금이 적용 되거나 잠금이 적용 되는 리소스 그룹을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-139">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="be54e-139">-ResourceName</span></span>
<span data-ttu-id="be54e-140">잠금이 적용 되는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="be54e-141">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="be54e-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="be54e-142">-ResourceType</span></span>
<span data-ttu-id="be54e-143">잠금이 적용 되는 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-143">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-144">-범위</span><span class="sxs-lookup"><span data-stu-id="be54e-144">-Scope</span></span>
<span data-ttu-id="be54e-145">잠금이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="be54e-146">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 id `/resourceGroups/` 리소스 그룹 이름 `/providers/Microsoft.Sql/servers/` 서버 이름 `/databases/` 데이터베이스 이름 리소스 그룹을 지정 하려면 다음 형식을 사용 합니다. `/subscriptions/` 구독 ID `/resourceGroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="be54e-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54e-147">-확인</span><span class="sxs-lookup"><span data-stu-id="be54e-147">-Confirm</span></span>
<span data-ttu-id="be54e-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be54e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be54e-149">-WhatIf</span></span>
<span data-ttu-id="be54e-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be54e-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be54e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be54e-152">CommonParameters</span></span>
<span data-ttu-id="be54e-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be54e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be54e-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be54e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be54e-155">입력</span><span class="sxs-lookup"><span data-stu-id="be54e-155">INPUTS</span></span>

### <span data-ttu-id="be54e-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be54e-156">System.String</span></span>

### <span data-ttu-id="be54e-157">Microsoft. Azure.. m a. 잠금. LockLevel</span><span class="sxs-lookup"><span data-stu-id="be54e-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="be54e-158">출력</span><span class="sxs-lookup"><span data-stu-id="be54e-158">OUTPUTS</span></span>

### <span data-ttu-id="be54e-159">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="be54e-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="be54e-160">상속자</span><span class="sxs-lookup"><span data-stu-id="be54e-160">NOTES</span></span>

## <span data-ttu-id="be54e-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be54e-161">RELATED LINKS</span></span>

[<span data-ttu-id="be54e-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="be54e-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="be54e-163">제거-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="be54e-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="be54e-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="be54e-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)

