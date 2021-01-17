---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386919"
---
# <span data-ttu-id="f8cdb-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f8cdb-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="f8cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cdb-103">주어진 네임스페이스에 대한 NetworkRuleSet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="f8cdb-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8cdb-104">SYNTAX</span></span>

### <span data-ttu-id="f8cdb-105">NetworkRuleSetPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f8cdb-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cdb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8cdb-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cdb-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8cdb-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8cdb-108">설명</span><span class="sxs-lookup"><span data-stu-id="f8cdb-108">DESCRIPTION</span></span>
<span data-ttu-id="f8cdb-109">주어진 네임스페이스에 대한 NetworkRuleSet을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="f8cdb-110">예제</span><span class="sxs-lookup"><span data-stu-id="f8cdb-110">EXAMPLES</span></span>

### <span data-ttu-id="f8cdb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8cdb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="f8cdb-112">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="f8cdb-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="f8cdb-113">주어진 "Eventhub-Namespace1-1375" 네임스페이스에 대한 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="f8cdb-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f8cdb-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="f8cdb-115">InputObject를 사용하여 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="f8cdb-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="f8cdb-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="f8cdb-117">이름 : defaultAction : 허용 ID : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="f8cdb-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="f8cdb-118">네임스페이스의 ResourceId를 사용하여 NetworkRuleSet을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="f8cdb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8cdb-119">PARAMETERS</span></span>

### <span data-ttu-id="f8cdb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8cdb-120">-AsJob</span></span>
<span data-ttu-id="f8cdb-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f8cdb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8cdb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cdb-122">-DefaultProfile</span></span>
<span data-ttu-id="f8cdb-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8cdb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8cdb-124">-InputObject</span></span>
<span data-ttu-id="f8cdb-125">네임스페이스 개체</span><span class="sxs-lookup"><span data-stu-id="f8cdb-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cdb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f8cdb-126">-Name</span></span>
<span data-ttu-id="f8cdb-127">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="f8cdb-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8cdb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8cdb-128">-PassThru</span></span>
<span data-ttu-id="f8cdb-129">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="f8cdb-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f8cdb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cdb-130">-ResourceGroupName</span></span>
<span data-ttu-id="f8cdb-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f8cdb-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8cdb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8cdb-132">-ResourceId</span></span>
<span data-ttu-id="f8cdb-133">네임스페이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f8cdb-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cdb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8cdb-134">-Confirm</span></span>
<span data-ttu-id="f8cdb-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8cdb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8cdb-136">-WhatIf</span></span>
<span data-ttu-id="f8cdb-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f8cdb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8cdb-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8cdb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cdb-139">CommonParameters</span></span>
<span data-ttu-id="f8cdb-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f8cdb-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f8cdb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cdb-142">입력</span><span class="sxs-lookup"><span data-stu-id="f8cdb-142">INPUTS</span></span>

### <span data-ttu-id="f8cdb-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f8cdb-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="f8cdb-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f8cdb-144">System.String</span></span>

## <span data-ttu-id="f8cdb-145">출력</span><span class="sxs-lookup"><span data-stu-id="f8cdb-145">OUTPUTS</span></span>

### <span data-ttu-id="f8cdb-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8cdb-146">System.Boolean</span></span>

## <span data-ttu-id="f8cdb-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8cdb-147">NOTES</span></span>

## <span data-ttu-id="f8cdb-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8cdb-148">RELATED LINKS</span></span>