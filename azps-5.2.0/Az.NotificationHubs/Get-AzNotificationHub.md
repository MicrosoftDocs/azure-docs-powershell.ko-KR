---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336309"
---
# <span data-ttu-id="6e268-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6e268-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="6e268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e268-102">SYNOPSIS</span></span>
<span data-ttu-id="6e268-103">알림 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="6e268-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e268-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e268-105">설명</span><span class="sxs-lookup"><span data-stu-id="6e268-105">DESCRIPTION</span></span>
<span data-ttu-id="6e268-106">**Get-AzNotificationHub** cmdlet은 지정된 네임스페이스의 알림 허브에 대한 정보를 받고 지정된 리소스 그룹에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="6e268-107">예를 들어 네임스페이스 ContosoNamespace의 모든 알림 허브에 대한 정보를 받고 ContosoNotificationsGroup 리소스 그룹에 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="6e268-108">또는 *NotificationHub* 매개 변수를 사용하여 반환된 데이터를 특정 알림 허브에 대한 정보로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="6e268-109">알림 허브는 해당 클라이언트에서 사용하는 iOS, Android, Windows Phone 8 및 Windows 스토어와 같은 플랫폼에 관계 없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="6e268-110">이러한 허브는 개별 앱과 거의 동일하며 각 앱에는 일반적으로 자체 알림 허브가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="6e268-111">이 cmdlet은 허브 자체에 대한 정보만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="6e268-112">허브의 권한 부여 규칙, 연결 문자열 및 플랫폼 알림 서비스 자격 증명에 대한 정보를 얻기 위해 Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys 및 Get-AzNotificationHubPNSCredentials와 같은 다른 cmdlet이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="6e268-113">예제</span><span class="sxs-lookup"><span data-stu-id="6e268-113">EXAMPLES</span></span>

### <span data-ttu-id="6e268-114">예제 1: 특정 네임스페이스의 모든 알림 허브에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="6e268-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="6e268-115">이 명령은 리소스 그룹 ContosoNotificationsGroup에 할당된 ContosoNamespace 네임스페이스의 모든 알림 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="6e268-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="6e268-116">Example 2</span></span>

<span data-ttu-id="6e268-117">알림 허브에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="6e268-118">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="6e268-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="6e268-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e268-119">PARAMETERS</span></span>

### <span data-ttu-id="6e268-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e268-120">-DefaultProfile</span></span>
<span data-ttu-id="6e268-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6e268-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e268-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e268-122">-Namespace</span></span>
<span data-ttu-id="6e268-123">알림 허브가 할당된 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="6e268-124">네임스페이스는 알림 허브를 그룹화하고 분류하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6e268-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="6e268-125">-NotificationHub</span></span>
<span data-ttu-id="6e268-126">이 cmdlet이 수신하는 알림 허브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="6e268-127">알림 허브는 해당 클라이언트에서 사용하는 플랫폼에 관계없이 여러 클라이언트에 푸시 알림을 보내는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e268-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e268-128">-ResourceGroup</span></span>
<span data-ttu-id="6e268-129">알림 허브가 할당된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="6e268-130">리소스 그룹은 인벤토리 관리 및 Azure 관리에 도움이 되는 방식으로 네임스페이스, 알림 허브 및 권한 부여 규칙과 같은 항목을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6e268-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e268-131">CommonParameters</span></span>
<span data-ttu-id="6e268-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e268-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e268-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e268-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e268-134">입력</span><span class="sxs-lookup"><span data-stu-id="6e268-134">INPUTS</span></span>

### <span data-ttu-id="6e268-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6e268-135">System.String</span></span>

## <span data-ttu-id="6e268-136">출력</span><span class="sxs-lookup"><span data-stu-id="6e268-136">OUTPUTS</span></span>

### <span data-ttu-id="6e268-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="6e268-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="6e268-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e268-138">NOTES</span></span>

## <span data-ttu-id="6e268-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e268-139">RELATED LINKS</span></span>

[<span data-ttu-id="6e268-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6e268-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="6e268-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="6e268-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="6e268-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="6e268-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="6e268-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6e268-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="6e268-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6e268-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="6e268-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="6e268-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

