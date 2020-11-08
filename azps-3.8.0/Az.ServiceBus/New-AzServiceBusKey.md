---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: b4e008dcb80cf1b67e7987fe89d86c89f247476c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043723"
---
# <span data-ttu-id="52cf7-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="52cf7-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="52cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="52cf7-103">Service Bus 네임 스페이스 또는 큐 또는 항목에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="52cf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52cf7-104">SYNTAX</span></span>

### <span data-ttu-id="52cf7-105">NamespaceAuthorizationRuleSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="52cf7-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52cf7-106">QueueAuthorizationRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="52cf7-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52cf7-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="52cf7-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52cf7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="52cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="52cf7-109">**AzServiceBusKey** cmdlet은 지정 된 네임 스페이스 또는 큐 또는 항목 및 권한 부여 규칙에 대 한 새 기본 또는 보조 연결 문자열을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="52cf7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="52cf7-110">EXAMPLES</span></span>

### <span data-ttu-id="52cf7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="52cf7-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="52cf7-112">네임 스페이스에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="52cf7-113">예제 1.1</span><span class="sxs-lookup"><span data-stu-id="52cf7-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="52cf7-114">네임 스페이스에 대해 제공 된 키 값으로 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="52cf7-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="52cf7-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="52cf7-116">큐에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="52cf7-117">예제 2.2</span><span class="sxs-lookup"><span data-stu-id="52cf7-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="52cf7-118">큐에 대해 제공 된 키 값을 사용 하 여 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="52cf7-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="52cf7-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="52cf7-120">주제에 대 한 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="52cf7-121">예제 3.1</span><span class="sxs-lookup"><span data-stu-id="52cf7-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="52cf7-122">항목에 대해 제공 된 키 값을 사용 하 여 기본 또는 보조 연결 문자열을 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="52cf7-123">변수</span><span class="sxs-lookup"><span data-stu-id="52cf7-123">PARAMETERS</span></span>

### <span data-ttu-id="52cf7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52cf7-124">-DefaultProfile</span></span>
<span data-ttu-id="52cf7-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52cf7-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="52cf7-126">-KeyValue</span></span>
<span data-ttu-id="52cf7-127">SAS 토큰에 서명 하 고 유효성을 검사 하기 위한 base64 인코딩된 256 비트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52cf7-128">-이름</span><span class="sxs-lookup"><span data-stu-id="52cf7-128">-Name</span></span>
<span data-ttu-id="52cf7-129">AuthorizationRule 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="52cf7-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="52cf7-130">-Namespace</span></span>
<span data-ttu-id="52cf7-131">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="52cf7-131">Namespace Name</span></span>

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

### <span data-ttu-id="52cf7-132">-큐</span><span class="sxs-lookup"><span data-stu-id="52cf7-132">-Queue</span></span>
<span data-ttu-id="52cf7-133">큐 이름</span><span class="sxs-lookup"><span data-stu-id="52cf7-133">Queue Name</span></span>

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

### <span data-ttu-id="52cf7-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="52cf7-134">-RegenerateKey</span></span>
<span data-ttu-id="52cf7-135">' PrimaryKey '/' SecondaryKey ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52cf7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52cf7-136">-ResourceGroupName</span></span>
<span data-ttu-id="52cf7-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="52cf7-137">Resource Group Name</span></span>

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

### <span data-ttu-id="52cf7-138">-주제</span><span class="sxs-lookup"><span data-stu-id="52cf7-138">-Topic</span></span>
<span data-ttu-id="52cf7-139">주제 이름</span><span class="sxs-lookup"><span data-stu-id="52cf7-139">Topic Name</span></span>

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

### <span data-ttu-id="52cf7-140">-확인</span><span class="sxs-lookup"><span data-stu-id="52cf7-140">-Confirm</span></span>
<span data-ttu-id="52cf7-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52cf7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cf7-142">-WhatIf</span></span>
<span data-ttu-id="52cf7-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52cf7-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52cf7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cf7-145">CommonParameters</span></span>
<span data-ttu-id="52cf7-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52cf7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cf7-147">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52cf7-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cf7-148">입력</span><span class="sxs-lookup"><span data-stu-id="52cf7-148">INPUTS</span></span>

### <span data-ttu-id="52cf7-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52cf7-149">System.String</span></span>

## <span data-ttu-id="52cf7-150">출력</span><span class="sxs-lookup"><span data-stu-id="52cf7-150">OUTPUTS</span></span>

### <span data-ttu-id="52cf7-151">ServiceBus. PSListKeysAttributes/.</span><span class="sxs-lookup"><span data-stu-id="52cf7-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="52cf7-152">상속자</span><span class="sxs-lookup"><span data-stu-id="52cf7-152">NOTES</span></span>

## <span data-ttu-id="52cf7-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52cf7-153">RELATED LINKS</span></span>