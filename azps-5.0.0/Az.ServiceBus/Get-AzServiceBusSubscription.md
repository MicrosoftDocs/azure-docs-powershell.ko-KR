---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215686"
---
# <span data-ttu-id="c4618-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="c4618-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="c4618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4618-102">SYNOPSIS</span></span>
<span data-ttu-id="c4618-103">지정 된 항목에 대 한 구독 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="c4618-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4618-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4618-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c4618-105">DESCRIPTION</span></span>
<span data-ttu-id="c4618-106">**AzServiceBusSubscription** cmdlet은 지정 된 Service Bus 항목에 대 한 구독 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="c4618-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c4618-107">EXAMPLES</span></span>

### <span data-ttu-id="c4618-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4618-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="c4618-109">지정 된 Service Bus 항목에 대 한 구독 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="c4618-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="c4618-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="c4618-111">지정 된 Service Bus 항목에 대 한 구독 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="c4618-112">기본적으로 100 구독이 반환 됩니다. 구독 수는-MaxCount 매개 변수를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="c4618-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="c4618-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="c4618-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="c4618-114">지정 된 Service Bus 항목에 대 한 첫 번째 150 구독의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="c4618-115">변수</span><span class="sxs-lookup"><span data-stu-id="c4618-115">PARAMETERS</span></span>

### <span data-ttu-id="c4618-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4618-116">-DefaultProfile</span></span>
<span data-ttu-id="c4618-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4618-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c4618-118">-MaxCount</span></span>
<span data-ttu-id="c4618-119">반환할 최대 구독 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="c4618-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c4618-120">-Name</span></span>
<span data-ttu-id="c4618-121">구독 이름</span><span class="sxs-lookup"><span data-stu-id="c4618-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4618-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4618-122">-Namespace</span></span>
<span data-ttu-id="c4618-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="c4618-123">Namespace Name</span></span>

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

### <span data-ttu-id="c4618-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4618-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4618-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-125">The name of the resource group</span></span>

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

### <span data-ttu-id="c4618-126">-주제</span><span class="sxs-lookup"><span data-stu-id="c4618-126">-Topic</span></span>
<span data-ttu-id="c4618-127">주제 이름</span><span class="sxs-lookup"><span data-stu-id="c4618-127">Topic Name</span></span>

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

### <span data-ttu-id="c4618-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4618-128">CommonParameters</span></span>
<span data-ttu-id="c4618-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4618-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4618-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4618-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4618-131">입력</span><span class="sxs-lookup"><span data-stu-id="c4618-131">INPUTS</span></span>

### <span data-ttu-id="c4618-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c4618-132">System.String</span></span>

## <span data-ttu-id="c4618-133">출력</span><span class="sxs-lookup"><span data-stu-id="c4618-133">OUTPUTS</span></span>

### <span data-ttu-id="c4618-134">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="c4618-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="c4618-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c4618-135">NOTES</span></span>

## <span data-ttu-id="c4618-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4618-136">RELATED LINKS</span></span>