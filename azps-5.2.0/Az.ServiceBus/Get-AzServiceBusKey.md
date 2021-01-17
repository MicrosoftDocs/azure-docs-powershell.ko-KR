---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338877"
---
# <span data-ttu-id="22cd7-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="22cd7-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="22cd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="22cd7-103">주어진 네임스페이스 또는 큐 또는 토픽 또는 별칭(GeoDR 구성)에 대한 기본 및 보조 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="22cd7-104">구문</span><span class="sxs-lookup"><span data-stu-id="22cd7-104">SYNTAX</span></span>

### <span data-ttu-id="22cd7-105">NamespaceAuthorizationRuleSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="22cd7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cd7-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="22cd7-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cd7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="22cd7-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cd7-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="22cd7-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cd7-109">설명</span><span class="sxs-lookup"><span data-stu-id="22cd7-109">DESCRIPTION</span></span>
<span data-ttu-id="22cd7-110">**Get-AzServiceBusKey** cmdlet은 주어진 네임스페이스 또는 큐 또는 토픽 또는 별칭(GeoDR 구성)에 대한 기본 및 보조 연결 문자열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="22cd7-111">예제</span><span class="sxs-lookup"><span data-stu-id="22cd7-111">EXAMPLES</span></span>

### <span data-ttu-id="22cd7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="22cd7-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="22cd7-113">지정된 네임스페이스에 대한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="22cd7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="22cd7-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="22cd7-115">지정된 큐에 대한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="22cd7-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="22cd7-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="22cd7-117">지정된 토픽에 대한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="22cd7-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="22cd7-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="22cd7-119">지정된 네임스페이스 및 별칭에 대한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="22cd7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cd7-120">PARAMETERS</span></span>

### <span data-ttu-id="22cd7-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="22cd7-121">-AliasName</span></span>
<span data-ttu-id="22cd7-122">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="22cd7-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22cd7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cd7-123">-DefaultProfile</span></span>
<span data-ttu-id="22cd7-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cd7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="22cd7-125">-Name</span></span>
<span data-ttu-id="22cd7-126">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="22cd7-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="22cd7-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="22cd7-127">-Namespace</span></span>
<span data-ttu-id="22cd7-128">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="22cd7-128">Namespace Name</span></span>

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

### <span data-ttu-id="22cd7-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="22cd7-129">-Queue</span></span>
<span data-ttu-id="22cd7-130">큐 이름</span><span class="sxs-lookup"><span data-stu-id="22cd7-130">Queue Name</span></span>

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

### <span data-ttu-id="22cd7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cd7-131">-ResourceGroupName</span></span>
<span data-ttu-id="22cd7-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="22cd7-132">Resource Group Name</span></span>

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

### <span data-ttu-id="22cd7-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="22cd7-133">-Topic</span></span>
<span data-ttu-id="22cd7-134">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="22cd7-134">Topic Name</span></span>

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

### <span data-ttu-id="22cd7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cd7-135">CommonParameters</span></span>
<span data-ttu-id="22cd7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22cd7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cd7-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="22cd7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cd7-138">입력</span><span class="sxs-lookup"><span data-stu-id="22cd7-138">INPUTS</span></span>

### <span data-ttu-id="22cd7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="22cd7-139">System.String</span></span>

## <span data-ttu-id="22cd7-140">출력</span><span class="sxs-lookup"><span data-stu-id="22cd7-140">OUTPUTS</span></span>

### <span data-ttu-id="22cd7-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="22cd7-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="22cd7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22cd7-142">NOTES</span></span>

## <span data-ttu-id="22cd7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22cd7-143">RELATED LINKS</span></span>