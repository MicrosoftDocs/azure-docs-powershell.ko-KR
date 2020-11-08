---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034763"
---
# <span data-ttu-id="e2799-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2799-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e2799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2799-102">SYNOPSIS</span></span>
<span data-ttu-id="e2799-103">지정 된 리소스 그룹에서 Service Bus 네임 스페이스 또는 큐 또는 주제의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="e2799-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2799-104">SYNTAX</span></span>

### <span data-ttu-id="e2799-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2799-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2799-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="e2799-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2799-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2799-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2799-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e2799-108">DESCRIPTION</span></span>
<span data-ttu-id="e2799-109">**AzServiceBusAuthorizationRule** cmdlet은 지정 된 리소스 그룹에 대 한 Service Bus 네임 스페이스 또는 큐 또는 항목의 권한 부여 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="e2799-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e2799-110">EXAMPLES</span></span>

### <span data-ttu-id="e2799-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2799-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="e2799-112">`SBAuthoRule1`지정 된 리소스 그룹에서 네임 스페이스의 권한 부여 규칙을 제거 `SB-Example1` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="e2799-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e2799-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="e2799-114">`SBAuthoRule1`지정 된 리소스 그룹에서 큐의 권한 부여 규칙을 제거 `SBQueue` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="e2799-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e2799-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="e2799-116">지정 된 리소스 그룹의 주제에 대 한 권한 부여 규칙을 제거 `SBAuthoRule1` `SBTopic` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="e2799-117">변수</span><span class="sxs-lookup"><span data-stu-id="e2799-117">PARAMETERS</span></span>

### <span data-ttu-id="e2799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2799-118">-DefaultProfile</span></span>
<span data-ttu-id="e2799-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2799-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e2799-120">-Force</span></span>
<span data-ttu-id="e2799-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e2799-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2799-122">-InputObject</span></span>
<span data-ttu-id="e2799-123">ServiceBus AuthorizationRule 개체</span><span class="sxs-lookup"><span data-stu-id="e2799-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2799-124">-이름</span><span class="sxs-lookup"><span data-stu-id="e2799-124">-Name</span></span>
<span data-ttu-id="e2799-125">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="e2799-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2799-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2799-126">-Namespace</span></span>
<span data-ttu-id="e2799-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="e2799-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2799-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2799-128">-PassThru</span></span>
<span data-ttu-id="e2799-129">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2799-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e2799-131">-큐</span><span class="sxs-lookup"><span data-stu-id="e2799-131">-Queue</span></span>
<span data-ttu-id="e2799-132">큐 이름</span><span class="sxs-lookup"><span data-stu-id="e2799-132">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2799-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2799-133">-ResourceGroupName</span></span>
<span data-ttu-id="e2799-134">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e2799-134">Resource Group Name</span></span>

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

### <span data-ttu-id="e2799-135">-주제</span><span class="sxs-lookup"><span data-stu-id="e2799-135">-Topic</span></span>
<span data-ttu-id="e2799-136">주제 이름</span><span class="sxs-lookup"><span data-stu-id="e2799-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2799-137">-확인</span><span class="sxs-lookup"><span data-stu-id="e2799-137">-Confirm</span></span>
<span data-ttu-id="e2799-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2799-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2799-139">-WhatIf</span></span>
<span data-ttu-id="e2799-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2799-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2799-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2799-142">CommonParameters</span></span>
<span data-ttu-id="e2799-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2799-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2799-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2799-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2799-145">입력</span><span class="sxs-lookup"><span data-stu-id="e2799-145">INPUTS</span></span>

### <span data-ttu-id="e2799-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2799-146">System.String</span></span>

### <span data-ttu-id="e2799-147">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e2799-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e2799-148">출력</span><span class="sxs-lookup"><span data-stu-id="e2799-148">OUTPUTS</span></span>

### <span data-ttu-id="e2799-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e2799-149">System.Boolean</span></span>

## <span data-ttu-id="e2799-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e2799-150">NOTES</span></span>

## <span data-ttu-id="e2799-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2799-151">RELATED LINKS</span></span>