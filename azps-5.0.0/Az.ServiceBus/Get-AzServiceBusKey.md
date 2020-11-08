---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215876"
---
# <span data-ttu-id="0cac7-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="0cac7-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="0cac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cac7-102">SYNOPSIS</span></span>
<span data-ttu-id="0cac7-103">지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (GeoDR 구성)에 대 한 기본 및 보조 연결 문자열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="0cac7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0cac7-104">SYNTAX</span></span>

### <span data-ttu-id="0cac7-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0cac7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cac7-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="0cac7-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cac7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cac7-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cac7-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="0cac7-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cac7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0cac7-109">DESCRIPTION</span></span>
<span data-ttu-id="0cac7-110">**AzServiceBusKey** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (Geodr 구성)에 대 한 기본 및 보조 연결 문자열을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="0cac7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0cac7-111">EXAMPLES</span></span>

### <span data-ttu-id="0cac7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0cac7-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="0cac7-113">지정 된 네임 스페이스에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="0cac7-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="0cac7-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="0cac7-115">지정 된 큐에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="0cac7-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="0cac7-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="0cac7-117">지정 된 항목에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="0cac7-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="0cac7-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="0cac7-119">지정 된 네임 스페이스 및 별칭에 대 한 기본 및 보조 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="0cac7-120">변수</span><span class="sxs-lookup"><span data-stu-id="0cac7-120">PARAMETERS</span></span>

### <span data-ttu-id="0cac7-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="0cac7-121">-AliasName</span></span>
<span data-ttu-id="0cac7-122">별칭 이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-122">Alias Name</span></span>

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

### <span data-ttu-id="0cac7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cac7-123">-DefaultProfile</span></span>
<span data-ttu-id="0cac7-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cac7-125">-이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-125">-Name</span></span>
<span data-ttu-id="0cac7-126">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="0cac7-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0cac7-127">-Namespace</span></span>
<span data-ttu-id="0cac7-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-128">Namespace Name</span></span>

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

### <span data-ttu-id="0cac7-129">-큐</span><span class="sxs-lookup"><span data-stu-id="0cac7-129">-Queue</span></span>
<span data-ttu-id="0cac7-130">큐 이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-130">Queue Name</span></span>

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

### <span data-ttu-id="0cac7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cac7-131">-ResourceGroupName</span></span>
<span data-ttu-id="0cac7-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-132">Resource Group Name</span></span>

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

### <span data-ttu-id="0cac7-133">-주제</span><span class="sxs-lookup"><span data-stu-id="0cac7-133">-Topic</span></span>
<span data-ttu-id="0cac7-134">주제 이름</span><span class="sxs-lookup"><span data-stu-id="0cac7-134">Topic Name</span></span>

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

### <span data-ttu-id="0cac7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cac7-135">CommonParameters</span></span>
<span data-ttu-id="0cac7-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cac7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cac7-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cac7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cac7-138">입력</span><span class="sxs-lookup"><span data-stu-id="0cac7-138">INPUTS</span></span>

### <span data-ttu-id="0cac7-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0cac7-139">System.String</span></span>

## <span data-ttu-id="0cac7-140">출력</span><span class="sxs-lookup"><span data-stu-id="0cac7-140">OUTPUTS</span></span>

### <span data-ttu-id="0cac7-141">ServiceBus. PSListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="0cac7-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="0cac7-142">상속자</span><span class="sxs-lookup"><span data-stu-id="0cac7-142">NOTES</span></span>

## <span data-ttu-id="0cac7-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cac7-143">RELATED LINKS</span></span>