---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: f95b016380f640154533f69d3942b8fe12a064d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203844"
---
# <span data-ttu-id="7675e-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7675e-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="7675e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7675e-102">SYNOPSIS</span></span>
<span data-ttu-id="7675e-103">알림 허브에 대 한 권한 부여 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="7675e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7675e-104">SYNTAX</span></span>

### <span data-ttu-id="7675e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7675e-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7675e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7675e-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7675e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7675e-107">DESCRIPTION</span></span>
<span data-ttu-id="7675e-108">**AzNotificationHubAuthorizationRule** cmdlet은 알림 허브에 할당 된 SAS (공유 액세스 서명) 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="7675e-109">권한 부여 규칙은 다양 한 사용 권한 수준에 따라 Uri로 링크를 만들어 알림 허브에 대 한 액세스를 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="7675e-110">사용 권한 수준은 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="7675e-111">듣기</span><span class="sxs-lookup"><span data-stu-id="7675e-111">Listen</span></span>
- <span data-ttu-id="7675e-112">보내기</span><span class="sxs-lookup"><span data-stu-id="7675e-112">Send</span></span>
- <span data-ttu-id="7675e-113">클라이언트 관리는 적절 한 사용 권한 수준에 따라 이러한 Uri 중 하나로 향합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="7675e-114">예를 들어 Listen 권한이 지정 된 클라이언트는 해당 권한의 URI로 리디렉션됩니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="7675e-115">이 cmdlet은 알림 허브에 할당 된 권한 부여 규칙을 수정 하는 두 가지 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="7675e-116">하나를 사용 하는 경우 **Sharedaccessauthorizationruleattributes** 개체의 인스턴스를 만든 다음 규칙을 적용할 속성 값으로 해당 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="7675e-117">.NET Framework를 통해 개체를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="7675e-118">그런 다음 *SASRule* 매개 변수를 사용 하 여 해당 속성 값을 규칙에 복사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="7675e-119">또는 관련 구성 값이 포함 된 JSON (JavaScript 개체 표시법) 파일을 만든 다음 *InputFile* 매개 변수를 통해 해당 값을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="7675e-120">JSON 파일은 {"Name": "ContosoAuthorizationRule"와 같은 구문을 사용 하는 텍스트 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="7675e-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="7675e-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="7675e-122">"권한": \[</span><span class="sxs-lookup"><span data-stu-id="7675e-122">"Rights": \[</span></span>  
        <span data-ttu-id="7675e-123">"듣기",</span><span class="sxs-lookup"><span data-stu-id="7675e-123">"Listen",</span></span>  
        <span data-ttu-id="7675e-124">보내며</span><span class="sxs-lookup"><span data-stu-id="7675e-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="7675e-125">} New-AzNotificationHubAuthorizationRule cmdlet과 함께 사용 하는 경우 앞의 JSON 샘플에서는 사용자가 허브에 대 한 수신 권한을 주고 받을 수 있도록 ContosoAuthorizationRule 이라는 인증 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="7675e-126">예제의</span><span class="sxs-lookup"><span data-stu-id="7675e-126">EXAMPLES</span></span>

### <span data-ttu-id="7675e-127">예제 1: 알림 허브에 할당 된 권한 부여 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="7675e-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="7675e-128">이 명령은 ContosoExternalHub 이라는 알림 허브에 할당 된 권한 부여 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="7675e-129">허브가 있는 네임 스페이스와 허브가 할당 된 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="7675e-130">명령 자체에는 수정 되는 규칙에 대 한 정보가 포함 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="7675e-131">대신이 정보는 입력 파일 C:\Configuration\AuthorizationRules.js에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="7675e-132">변수</span><span class="sxs-lookup"><span data-stu-id="7675e-132">PARAMETERS</span></span>

### <span data-ttu-id="7675e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7675e-133">-DefaultProfile</span></span>
<span data-ttu-id="7675e-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7675e-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7675e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="7675e-135">-Force</span></span>
<span data-ttu-id="7675e-136">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7675e-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7675e-137">-InputFile</span></span>
<span data-ttu-id="7675e-138">새 규칙에 대 한 구성 정보를 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7675e-139">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7675e-139">-Namespace</span></span>
<span data-ttu-id="7675e-140">알림 허브가 할당 된 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="7675e-141">네임 스페이스는 알림 허브를 그룹화 하 고 분류 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="7675e-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="7675e-142">-NotificationHub</span></span>
<span data-ttu-id="7675e-143">이 cmdlet이 권한 부여 규칙을 할당 하는 알림 허브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="7675e-144">알림 허브는 해당 클라이언트에서 사용 하는 것과 관계 없이 여러 클라이언트로 푸시 알림을 보내는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="7675e-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7675e-145">-ResourceGroup</span></span>
<span data-ttu-id="7675e-146">알림 허브가 할당 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="7675e-147">리소스 그룹은 관리 및 Azure 관리를 쉽게 할 수 있는 방식으로 네임 스페이스, 알림 허브, 권한 부여 규칙 등의 항목을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="7675e-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7675e-148">-SASRule</span></span>
<span data-ttu-id="7675e-149">수정 되는 권한 부여 규칙에 대 한 구성 정보를 포함 하는 **Sharedaccessauthorizationruleattributes** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7675e-150">-확인</span><span class="sxs-lookup"><span data-stu-id="7675e-150">-Confirm</span></span>
<span data-ttu-id="7675e-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7675e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7675e-152">-WhatIf</span></span>
<span data-ttu-id="7675e-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7675e-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7675e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7675e-155">CommonParameters</span></span>
<span data-ttu-id="7675e-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7675e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7675e-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7675e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7675e-158">입력</span><span class="sxs-lookup"><span data-stu-id="7675e-158">INPUTS</span></span>

### <span data-ttu-id="7675e-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7675e-159">System.String</span></span>

## <span data-ttu-id="7675e-160">출력</span><span class="sxs-lookup"><span data-stu-id="7675e-160">OUTPUTS</span></span>

### <span data-ttu-id="7675e-161">Microsoft. Azure. 명령. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7675e-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7675e-162">상속자</span><span class="sxs-lookup"><span data-stu-id="7675e-162">NOTES</span></span>

## <span data-ttu-id="7675e-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7675e-163">RELATED LINKS</span></span>

[<span data-ttu-id="7675e-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7675e-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7675e-165">새로운 AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7675e-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="7675e-166">제거-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7675e-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

