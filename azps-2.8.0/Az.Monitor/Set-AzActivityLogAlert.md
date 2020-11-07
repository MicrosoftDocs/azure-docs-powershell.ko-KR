---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: a6894765d4da1e0582adc4f22fe0a0e572f000d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870973"
---
# <span data-ttu-id="90e53-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90e53-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="90e53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e53-102">SYNOPSIS</span></span>
<span data-ttu-id="90e53-103">기존 활동 로그 알림을 새로 만들거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="90e53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90e53-104">SYNTAX</span></span>

### <span data-ttu-id="90e53-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90e53-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e53-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90e53-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e53-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="90e53-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90e53-108">설명은</span><span class="sxs-lookup"><span data-stu-id="90e53-108">DESCRIPTION</span></span>
<span data-ttu-id="90e53-109">**AzActivityLogAlert** cmdlet은 새 작업을 만들거나 기존 활동 로그 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="90e53-110">태그, 조건, 작업의 경우 개체를 미리 생성 하 고 쉼표로 구분 된이 호출에 매개 변수로 전달 해야 합니다 (아래 예제 참조).</span><span class="sxs-lookup"><span data-stu-id="90e53-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="90e53-111">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 만들거나 수정 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="90e53-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="90e53-112">**참고** :이 cmdlet 및 관련 항목은 사용 되지 않는 **추가 기능** (2017 11 월)을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="90e53-113">예제의</span><span class="sxs-lookup"><span data-stu-id="90e53-113">EXAMPLES</span></span>

### <span data-ttu-id="90e53-114">예제 1: 활동 로그 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="90e53-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="90e53-115">처음 4 개의 명령은 리프 조건과 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="90e53-116">마지막 명령은 조건과 작업 그룹을 사용 하 여 활동 로그 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="90e53-117">예제 2: 활동 로그 알림 만들기 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="90e53-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="90e53-118">처음 4 개의 명령은 리프 조건과 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="90e53-119">마지막 명령은 조건과 작업 그룹을 사용 하 여 활동 로그 알림을 만들지만 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="90e53-120">예제 3: 파이프 또는 InputObject 매개 변수의 값을 사용 하 여 활동 로그 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="90e53-121">첫 번째 명령은 nop과 비슷하지만 경고 규칙을 검색 하 고, 설명을 변경 하 고, 사용 하지 않도록 설정한 다음 InputObject 매개 변수를 사용 하 여 해당 변경 내용을 유지 하는 것과 동일한 값으로 경고를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="90e53-122">예제 4: 파이프의 ResourceId 값을 사용 하 여 활동 로그 알림 설정</span><span class="sxs-lookup"><span data-stu-id="90e53-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="90e53-123">지정 된 로그 알림 규칙이 있으면이 명령을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="90e53-124">변수</span><span class="sxs-lookup"><span data-stu-id="90e53-124">PARAMETERS</span></span>

### <span data-ttu-id="90e53-125">-작업</span><span class="sxs-lookup"><span data-stu-id="90e53-125">-Action</span></span>
<span data-ttu-id="90e53-126">활동 로그 알림에 대 한 작업 그룹의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-127">-조건</span><span class="sxs-lookup"><span data-stu-id="90e53-127">-Condition</span></span>
<span data-ttu-id="90e53-128">활동 로그 알림에 대 한 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="90e53-129">**참고** : 조건 목록에 "Category"와 같은 필드에 적어도 1이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="90e53-130">이 조건이 없는 경우 백 엔드는 400 (BadRequest)로 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e53-131">-DefaultProfile</span></span>
<span data-ttu-id="90e53-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90e53-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90e53-133">-설명</span><span class="sxs-lookup"><span data-stu-id="90e53-133">-Description</span></span>
<span data-ttu-id="90e53-134">알림 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="90e53-135">-DisableAlert</span></span>
<span data-ttu-id="90e53-136">사용 하지 않도록 설정 된 활동 로그 알림을 사용자가 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="90e53-137">지정 하지 않으면 경고가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90e53-138">-InputObject</span></span>
<span data-ttu-id="90e53-139">필요한 이름을 추출 하는 호출의 InputObject tags 속성 및 리소스 그룹 이름 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-140">-위치</span><span class="sxs-lookup"><span data-stu-id="90e53-140">-Location</span></span>
<span data-ttu-id="90e53-141">활동 로그 경고가 존재 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-142">-이름</span><span class="sxs-lookup"><span data-stu-id="90e53-142">-Name</span></span>
<span data-ttu-id="90e53-143">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e53-144">-ResourceGroupName</span></span>
<span data-ttu-id="90e53-145">알림 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90e53-146">-ResourceId</span></span>
<span data-ttu-id="90e53-147">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-148">-범위</span><span class="sxs-lookup"><span data-stu-id="90e53-148">-Scope</span></span>
<span data-ttu-id="90e53-149">활동 로그 알림의 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-150">태그</span><span class="sxs-lookup"><span data-stu-id="90e53-150">-Tag</span></span>
<span data-ttu-id="90e53-151">활동 로그 알림 리소스의 tags 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e53-152">-확인</span><span class="sxs-lookup"><span data-stu-id="90e53-152">-Confirm</span></span>
<span data-ttu-id="90e53-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e53-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e53-154">-WhatIf</span></span>
<span data-ttu-id="90e53-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90e53-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e53-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e53-157">CommonParameters</span></span>
<span data-ttu-id="90e53-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e53-159">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90e53-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e53-160">입력</span><span class="sxs-lookup"><span data-stu-id="90e53-160">INPUTS</span></span>

### <span data-ttu-id="90e53-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="90e53-161">System.String</span></span>

### <span data-ttu-id="90e53-162">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90e53-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="90e53-163">System.webserver. List ' 1 [[ActivityLogAlertLeafCondition, Microsoft azure.. t e l. i = 1.0.0.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="90e53-164">System.webserver. List ' 1 [[Microsoft. t e ...]. ActivityLogAlertActionGroup, Microsoft Azure. PowerShell, Culture = 중립, PublicKeyToken = null]]이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90e53-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="90e53-165">System.webserver. Dictionary ' 2 [[4.0.0.0], CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e], [System.webserver,, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="90e53-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="90e53-166">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="90e53-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="90e53-167">출력</span><span class="sxs-lookup"><span data-stu-id="90e53-167">OUTPUTS</span></span>

### <span data-ttu-id="90e53-168">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="90e53-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="90e53-169">상속자</span><span class="sxs-lookup"><span data-stu-id="90e53-169">NOTES</span></span>

## <span data-ttu-id="90e53-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90e53-170">RELATED LINKS</span></span>

[<span data-ttu-id="90e53-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90e53-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="90e53-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90e53-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="90e53-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90e53-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="90e53-174">제거-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="90e53-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="90e53-175">새로운 AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="90e53-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="90e53-176">새로운 AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="90e53-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)