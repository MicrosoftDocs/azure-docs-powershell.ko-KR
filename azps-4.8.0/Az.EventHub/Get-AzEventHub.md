---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213590"
---
# <span data-ttu-id="1d233-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="1d233-101">Get-AzEventHub</span></span>

## <span data-ttu-id="1d233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d233-102">SYNOPSIS</span></span>
<span data-ttu-id="1d233-103">단일 이벤트 허브의 세부 정보를 가져오거나 이벤트 허브 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="1d233-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d233-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d233-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d233-105">DESCRIPTION</span></span>
<span data-ttu-id="1d233-106">Get-AzEventHub cmdlet은 이벤트 허브의 세부 정보 또는 현재 네임 스페이스에 있는 모든 이벤트 허브의 목록 중 하나를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="1d233-107">이벤트 허브 이름을 제공 하는 경우 단일 이벤트 허브에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="1d233-108">이벤트 허브 이름을 제공 하지 않으면 지정 된 네임 스페이스에 있는 모든 이벤트 허브 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="1d233-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1d233-109">EXAMPLES</span></span>

### <span data-ttu-id="1d233-110">예제 1: 지정 된 EventHub</span><span class="sxs-lookup"><span data-stu-id="1d233-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="1d233-111">이벤트 허브 MyEventHubName의 세부 정보를 반환 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="1d233-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="1d233-112">예제 2: 지정 된 네임 스페이스의 EventHub 목록</span><span class="sxs-lookup"><span data-stu-id="1d233-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="1d233-113">네임 스페이스 MyNamespaceName의 이벤트 허브 목록을 반환 \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="1d233-114">변수</span><span class="sxs-lookup"><span data-stu-id="1d233-114">PARAMETERS</span></span>

### <span data-ttu-id="1d233-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d233-115">-DefaultProfile</span></span>
<span data-ttu-id="1d233-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d233-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1d233-117">-MaxCount</span></span>
<span data-ttu-id="1d233-118">반환할 최대 EventHubs 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="1d233-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1d233-119">-Name</span></span>
<span data-ttu-id="1d233-120">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="1d233-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d233-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1d233-121">-Namespace</span></span>
<span data-ttu-id="1d233-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="1d233-122">Namespace Name</span></span>

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

### <span data-ttu-id="1d233-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d233-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d233-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1d233-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1d233-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d233-125">CommonParameters</span></span>
<span data-ttu-id="1d233-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d233-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d233-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d233-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d233-128">입력</span><span class="sxs-lookup"><span data-stu-id="1d233-128">INPUTS</span></span>

### <span data-ttu-id="1d233-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1d233-129">System.String</span></span>

## <span data-ttu-id="1d233-130">출력</span><span class="sxs-lookup"><span data-stu-id="1d233-130">OUTPUTS</span></span>

### <span data-ttu-id="1d233-131">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="1d233-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="1d233-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1d233-132">NOTES</span></span>

## <span data-ttu-id="1d233-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d233-133">RELATED LINKS</span></span>