---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494878"
---
# <span data-ttu-id="248a6-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="248a6-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="248a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="248a6-102">SYNOPSIS</span></span>
<span data-ttu-id="248a6-103">주어진 토픽 구독에서 기존 규칙의 정의를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="248a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="248a6-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="248a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="248a6-105">DESCRIPTION</span></span>
<span data-ttu-id="248a6-106">**Get-AzServiceBusRule** cmdlet은 지정된 토픽 구독에서 지정된 규칙에 대한 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="248a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="248a6-107">EXAMPLES</span></span>

### <span data-ttu-id="248a6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="248a6-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="248a6-109">지정된 구독에 대해 지정된 규칙 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="248a6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="248a6-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="248a6-111">지정된 구독에 대한 규칙 설명 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="248a6-112">기본적으로 100개 규칙이 반환됩니다. 100개가 넘는 규칙이 반환되는 경우 -MaxCount 매개 변수를 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="248a6-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="248a6-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="248a6-114">지정된 구독에 대한 처음 150개 규칙 설명 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="248a6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="248a6-115">PARAMETERS</span></span>

### <span data-ttu-id="248a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248a6-116">-DefaultProfile</span></span>
<span data-ttu-id="248a6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="248a6-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="248a6-118">-MaxCount</span></span>
<span data-ttu-id="248a6-119">반환할 규칙의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="248a6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="248a6-120">-Name</span></span>
<span data-ttu-id="248a6-121">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="248a6-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="248a6-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="248a6-122">-Namespace</span></span>
<span data-ttu-id="248a6-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="248a6-123">Namespace Name</span></span>

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

### <span data-ttu-id="248a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="248a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="248a6-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="248a6-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="248a6-126">-Subscription</span><span class="sxs-lookup"><span data-stu-id="248a6-126">-Subscription</span></span>
<span data-ttu-id="248a6-127">구독 이름</span><span class="sxs-lookup"><span data-stu-id="248a6-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="248a6-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="248a6-128">-Topic</span></span>
<span data-ttu-id="248a6-129">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="248a6-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="248a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248a6-130">CommonParameters</span></span>
<span data-ttu-id="248a6-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="248a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248a6-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="248a6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248a6-133">입력</span><span class="sxs-lookup"><span data-stu-id="248a6-133">INPUTS</span></span>

### <span data-ttu-id="248a6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="248a6-134">System.String</span></span>

## <span data-ttu-id="248a6-135">출력</span><span class="sxs-lookup"><span data-stu-id="248a6-135">OUTPUTS</span></span>

### <span data-ttu-id="248a6-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="248a6-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="248a6-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="248a6-137">NOTES</span></span>

## <span data-ttu-id="248a6-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="248a6-138">RELATED LINKS</span></span>