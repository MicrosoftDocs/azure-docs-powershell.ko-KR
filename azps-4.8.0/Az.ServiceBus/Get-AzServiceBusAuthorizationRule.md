---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e0f6c8c2b07c0d9ab788504bb8eae3eb4615a7e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048740"
---
# <span data-ttu-id="d0bc4-101">Get-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d0bc4-101">Get-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="d0bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bc4-103">지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (GeoDR 구성)에 대해 지정 된 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span> 

## <span data-ttu-id="d0bc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0bc4-104">SYNTAX</span></span>

### <span data-ttu-id="d0bc4-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0bc4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bc4-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="d0bc4-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bc4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0bc4-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0bc4-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0bc4-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0bc4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d0bc4-109">DESCRIPTION</span></span>
<span data-ttu-id="d0bc4-110">**AzServiceBusAuthorizationRule** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목 또는 별칭 (Geodr 구성)에서 지정한 권한 부여 규칙에 대 한 설명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-110">The **Get-AzServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="d0bc4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d0bc4-111">EXAMPLES</span></span>

### <span data-ttu-id="d0bc4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0bc4-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="d0bc4-113">지정 된 네임 스페이스에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-113">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="d0bc4-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0bc4-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="d0bc4-115">지정 된 큐에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-115">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="d0bc4-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="d0bc4-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="d0bc4-117">지정 된 항목에 대 한 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-117">Returns the specified authorization rule description for a specified topic.</span></span>

### <span data-ttu-id="d0bc4-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="d0bc4-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="d0bc4-119">지정한 네임 스페이스 및 별칭에 대해 지정 된 권한 부여 규칙 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-119">Returns the specified authorization rule description for a specified namespace and alias.</span></span>

## <span data-ttu-id="d0bc4-120">변수</span><span class="sxs-lookup"><span data-stu-id="d0bc4-120">PARAMETERS</span></span>

### <span data-ttu-id="d0bc4-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="d0bc4-121">-AliasName</span></span>
<span data-ttu-id="d0bc4-122">GeoDR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-122">GeoDR Configuration Name</span></span>

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

### <span data-ttu-id="d0bc4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bc4-123">-DefaultProfile</span></span>
<span data-ttu-id="d0bc4-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0bc4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-125">-Name</span></span>
<span data-ttu-id="d0bc4-126">AuthorizationRule 이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0bc4-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d0bc4-127">-Namespace</span></span>
<span data-ttu-id="d0bc4-128">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-128">Namespace Name</span></span>

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

### <span data-ttu-id="d0bc4-129">-큐</span><span class="sxs-lookup"><span data-stu-id="d0bc4-129">-Queue</span></span>
<span data-ttu-id="d0bc4-130">큐 이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-130">Queue Name</span></span>

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

### <span data-ttu-id="d0bc4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0bc4-131">-ResourceGroupName</span></span>
<span data-ttu-id="d0bc4-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-132">Resource Group Name</span></span>

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

### <span data-ttu-id="d0bc4-133">-주제</span><span class="sxs-lookup"><span data-stu-id="d0bc4-133">-Topic</span></span>
<span data-ttu-id="d0bc4-134">주제 이름</span><span class="sxs-lookup"><span data-stu-id="d0bc4-134">Topic Name</span></span>

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

### <span data-ttu-id="d0bc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bc4-135">CommonParameters</span></span>
<span data-ttu-id="d0bc4-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bc4-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0bc4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bc4-138">입력</span><span class="sxs-lookup"><span data-stu-id="d0bc4-138">INPUTS</span></span>

### <span data-ttu-id="d0bc4-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0bc4-139">System.String</span></span>

## <span data-ttu-id="d0bc4-140">출력</span><span class="sxs-lookup"><span data-stu-id="d0bc4-140">OUTPUTS</span></span>

### <span data-ttu-id="d0bc4-141">ServiceBus. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="d0bc4-141">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="d0bc4-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d0bc4-142">NOTES</span></span>

## <span data-ttu-id="d0bc4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0bc4-143">RELATED LINKS</span></span>