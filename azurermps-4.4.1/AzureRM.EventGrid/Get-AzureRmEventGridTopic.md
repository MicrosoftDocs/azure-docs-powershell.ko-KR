---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534100"
---
# <span data-ttu-id="a4cb9-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a4cb9-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="a4cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cb9-103">이벤트 그리드 항목의 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 그리드 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4cb9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4cb9-104">SYNTAX</span></span>

### <span data-ttu-id="a4cb9-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4cb9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4cb9-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4cb9-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4cb9-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4cb9-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4cb9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a4cb9-108">DESCRIPTION</span></span>
<span data-ttu-id="a4cb9-109">Get-AzureRmEventGridTopic cmdlet은 지정 된 이벤트 그리드 주제에 대 한 세부 정보 또는 현재 Azure 구독에 있는 모든 이벤트 그리드 항목의 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="a4cb9-110">주제 이름을 제공 하는 경우 단일 이벤트 그리드 주제에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="a4cb9-111">주제 이름을 제공 하지 않으면 항목 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="a4cb9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a4cb9-112">EXAMPLES</span></span>

### <span data-ttu-id="a4cb9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4cb9-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="a4cb9-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1에 대 한 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="a4cb9-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a4cb9-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="a4cb9-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="a4cb9-116">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1에 대 한 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="a4cb9-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a4cb9-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="a4cb9-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="a4cb9-118">자원 그룹 MyResourceGroupName 모든 이벤트 눈금 항목을 나열 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a4cb9-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="a4cb9-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="a4cb9-120">구독의 모든 이벤트 그리드 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="a4cb9-121">변수</span><span class="sxs-lookup"><span data-stu-id="a4cb9-121">PARAMETERS</span></span>

### <span data-ttu-id="a4cb9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a4cb9-122">-Name</span></span>
<span data-ttu-id="a4cb9-123">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-123">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4cb9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cb9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4cb9-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4cb9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cb9-126">-ResourceId</span></span>
<span data-ttu-id="a4cb9-127">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-127">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4cb9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cb9-128">-DefaultProfile</span></span>
<span data-ttu-id="a4cb9-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4cb9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cb9-130">CommonParameters</span></span>
<span data-ttu-id="a4cb9-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cb9-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4cb9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cb9-133">입력</span><span class="sxs-lookup"><span data-stu-id="a4cb9-133">INPUTS</span></span>

### <span data-ttu-id="a4cb9-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a4cb9-134">System.String</span></span>
<span data-ttu-id="a4cb9-135">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a4cb9-136">출력</span><span class="sxs-lookup"><span data-stu-id="a4cb9-136">OUTPUTS</span></span>

### <span data-ttu-id="a4cb9-137">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="a4cb9-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="a4cb9-138">System.webserver. List ' 1 [[Microsoft Azure.] EventGrid. 모델. t e m l a m a m a m/1.0.0.0, Instance 그리드, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a4cb9-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a4cb9-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a4cb9-139">NOTES</span></span>

## <span data-ttu-id="a4cb9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4cb9-140">RELATED LINKS</span></span>
