---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 72d5fb7f5af5fb8e6501bfedee55ebe791765715
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867254"
---
# <span data-ttu-id="4ce96-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4ce96-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="4ce96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce96-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce96-103">활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="4ce96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ce96-104">SYNTAX</span></span>

### <span data-ttu-id="4ce96-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ce96-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce96-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ce96-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce96-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce96-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce96-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4ce96-108">DESCRIPTION</span></span>
<span data-ttu-id="4ce96-109">**AzActivityLogAlert** cmdlet은 활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="4ce96-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 패치 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="4ce96-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="4ce96-111">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4ce96-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4ce96-112">EXAMPLES</span></span>

### <span data-ttu-id="4ce96-113">예제 1: 활동 로그 알림 제거</span><span class="sxs-lookup"><span data-stu-id="4ce96-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="4ce96-114">이름 및 리소스 그룹 이름을 입력으로 사용 하 여 활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="4ce96-115">예제 2: PSActivityLogAlertResource를 입력으로 사용 하 여 활동 로그 알림 제거</span><span class="sxs-lookup"><span data-stu-id="4ce96-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="4ce96-116">PSActivityLogAlertResource를 입력으로 사용 하 여 활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="4ce96-117">예제 3: ResourceId 매개 변수를 사용 하 여 ActivityLogAlert 제거</span><span class="sxs-lookup"><span data-stu-id="4ce96-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="4ce96-118">이 명령은 파이프의 ResourceId 매개 변수를 사용 하 여 ActivityLogAlert를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="4ce96-119">변수</span><span class="sxs-lookup"><span data-stu-id="4ce96-119">PARAMETERS</span></span>

### <span data-ttu-id="4ce96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce96-120">-DefaultProfile</span></span>
<span data-ttu-id="4ce96-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ce96-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ce96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ce96-122">-InputObject</span></span>
<span data-ttu-id="4ce96-123">필요한 이름을 추출 하는 호출의 InputObject tags 속성 및 리소스 그룹 이름 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-124">-이름</span><span class="sxs-lookup"><span data-stu-id="4ce96-124">-Name</span></span>
<span data-ttu-id="4ce96-125">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce96-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ce96-127">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce96-128">-ResourceId</span></span>
<span data-ttu-id="4ce96-129">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce96-130">-확인</span><span class="sxs-lookup"><span data-stu-id="4ce96-130">-Confirm</span></span>
<span data-ttu-id="4ce96-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce96-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce96-132">-WhatIf</span></span>
<span data-ttu-id="4ce96-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ce96-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce96-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce96-135">CommonParameters</span></span>
<span data-ttu-id="4ce96-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce96-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce96-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce96-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce96-138">입력</span><span class="sxs-lookup"><span data-stu-id="4ce96-138">INPUTS</span></span>

### <span data-ttu-id="4ce96-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ce96-139">System.String</span></span>

### <span data-ttu-id="4ce96-140">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="4ce96-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="4ce96-141">출력</span><span class="sxs-lookup"><span data-stu-id="4ce96-141">OUTPUTS</span></span>

### <span data-ttu-id="4ce96-142">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4ce96-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4ce96-143">상속자</span><span class="sxs-lookup"><span data-stu-id="4ce96-143">NOTES</span></span>

## <span data-ttu-id="4ce96-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ce96-144">RELATED LINKS</span></span>

[<span data-ttu-id="4ce96-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4ce96-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="4ce96-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4ce96-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="4ce96-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4ce96-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="4ce96-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4ce96-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="4ce96-149">새로운 AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="4ce96-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="4ce96-150">새로운 AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4ce96-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)
