---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 66c127e701432604654cacb556d71588d9786dbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526820"
---
# <span data-ttu-id="055ba-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="055ba-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="055ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="055ba-102">SYNOPSIS</span></span>
<span data-ttu-id="055ba-103">기존 활동 로그 알림을 새로 만들거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="055ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="055ba-104">SYNTAX</span></span>

### <span data-ttu-id="055ba-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="055ba-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="055ba-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="055ba-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="055ba-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="055ba-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="055ba-108">설명은</span><span class="sxs-lookup"><span data-stu-id="055ba-108">DESCRIPTION</span></span>
<span data-ttu-id="055ba-109">**AzureRmActivityLogAlert** cmdlet은 새 작업을 만들거나 기존 활동 로그 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="055ba-110">태그, 조건, 작업의 경우 개체를 미리 생성 하 고 쉼표로 구분 된이 호출에 매개 변수로 전달 해야 합니다 (아래 예제 참조).</span><span class="sxs-lookup"><span data-stu-id="055ba-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="055ba-111">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 만들거나 수정 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="055ba-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

<span data-ttu-id="055ba-112">**참고** :이 cmdlet 및 관련 항목은 사용 되지 않는 **추가 기능** (2017 11 월)을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="055ba-113">예제의</span><span class="sxs-lookup"><span data-stu-id="055ba-113">EXAMPLES</span></span>

### <span data-ttu-id="055ba-114">예제 1: 활동 로그 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="055ba-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="055ba-115">처음 4 개의 명령은 리프 조건과 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="055ba-116">마지막 명령은 조건과 작업 그룹을 사용 하 여 활동 로그 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="055ba-117">예제 2: 활동 로그 알림 만들기 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="055ba-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="055ba-118">처음 4 개의 명령은 리프 조건과 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="055ba-119">마지막 명령은 조건과 작업 그룹을 사용 하 여 활동 로그 알림을 만들지만 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="055ba-120">예제 3: 파이프 또는 InputObject 매개 변수의 값을 사용 하 여 활동 로그 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="055ba-121">첫 번째 명령은 nop과 비슷하지만 경고 규칙을 검색 하 고, 설명을 변경 하 고, 사용 하지 않도록 설정한 다음 InputObject 매개 변수를 사용 하 여 해당 변경 내용을 유지 하는 것과 동일한 값으로 경고를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="055ba-122">예제 4: 파이프의 ResourceId 값을 사용 하 여 활동 로그 알림 설정</span><span class="sxs-lookup"><span data-stu-id="055ba-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="055ba-123">지정 된 로그 알림 규칙이 있으면이 명령을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="055ba-124">변수</span><span class="sxs-lookup"><span data-stu-id="055ba-124">PARAMETERS</span></span>

### <span data-ttu-id="055ba-125">-작업</span><span class="sxs-lookup"><span data-stu-id="055ba-125">-Action</span></span>
<span data-ttu-id="055ba-126">활동 로그 알림에 대 한 작업 그룹의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="055ba-127">-조건</span><span class="sxs-lookup"><span data-stu-id="055ba-127">-Condition</span></span>
<span data-ttu-id="055ba-128">활동 로그 알림에 대 한 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-128">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="055ba-129">**참고** : 조건 목록에 "Category"와 같은 필드에 적어도 1이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="055ba-130">이 조건이 없는 경우 백 엔드는 400 (BadRequest)로 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="055ba-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055ba-131">-DefaultProfile</span></span>
<span data-ttu-id="055ba-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="055ba-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-133">-설명</span><span class="sxs-lookup"><span data-stu-id="055ba-133">-Description</span></span>
<span data-ttu-id="055ba-134">알림 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-134">The description of the alert resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="055ba-135">-DisableAlert</span></span>
<span data-ttu-id="055ba-136">사용 하지 않도록 설정 된 활동 로그 알림을 사용자가 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="055ba-137">지정 하지 않으면 경고가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="055ba-138">-InputObject</span></span>
<span data-ttu-id="055ba-139">필요한 이름을 추출 하는 호출의 InputObject tags 속성 및 리소스 그룹 이름 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-140">-위치</span><span class="sxs-lookup"><span data-stu-id="055ba-140">-Location</span></span>
<span data-ttu-id="055ba-141">활동 로그 경고가 존재 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-142">-이름</span><span class="sxs-lookup"><span data-stu-id="055ba-142">-Name</span></span>
<span data-ttu-id="055ba-143">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-143">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055ba-144">-ResourceGroupName</span></span>
<span data-ttu-id="055ba-145">알림 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="055ba-146">-ResourceId</span></span>
<span data-ttu-id="055ba-147">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-148">-범위</span><span class="sxs-lookup"><span data-stu-id="055ba-148">-Scope</span></span>
<span data-ttu-id="055ba-149">활동 로그 알림의 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="055ba-150">태그</span><span class="sxs-lookup"><span data-stu-id="055ba-150">-Tag</span></span>
<span data-ttu-id="055ba-151">활동 로그 알림 리소스의 tags 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="055ba-152">-확인</span><span class="sxs-lookup"><span data-stu-id="055ba-152">-Confirm</span></span>
<span data-ttu-id="055ba-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="055ba-154">-WhatIf</span></span>
<span data-ttu-id="055ba-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="055ba-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ba-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055ba-157">CommonParameters</span></span>
<span data-ttu-id="055ba-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055ba-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="055ba-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055ba-160">입력</span><span class="sxs-lookup"><span data-stu-id="055ba-160">INPUTS</span></span>

### <span data-ttu-id="055ba-161">않아야</span><span class="sxs-lookup"><span data-stu-id="055ba-161">None</span></span>
<span data-ttu-id="055ba-162">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="055ba-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="055ba-163">출력</span><span class="sxs-lookup"><span data-stu-id="055ba-163">OUTPUTS</span></span>

### <span data-ttu-id="055ba-164">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="055ba-164">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="055ba-165">상속자</span><span class="sxs-lookup"><span data-stu-id="055ba-165">NOTES</span></span>

## <span data-ttu-id="055ba-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="055ba-166">RELATED LINKS</span></span>

[<span data-ttu-id="055ba-167">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="055ba-167">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="055ba-168">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="055ba-168">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="055ba-169">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="055ba-169">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="055ba-170">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="055ba-170">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="055ba-171">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="055ba-171">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="055ba-172">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="055ba-172">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)