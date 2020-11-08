---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212734"
---
# <span data-ttu-id="6a9cc-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a9cc-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="6a9cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9cc-103">IoT Hub의 모든 끝점에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6a9cc-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="6a9cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a9cc-104">SYNTAX</span></span>

### <span data-ttu-id="6a9cc-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a9cc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9cc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6a9cc-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9cc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6a9cc-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9cc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6a9cc-108">DESCRIPTION</span></span>
<span data-ttu-id="6a9cc-109">끝점에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="6a9cc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6a9cc-110">EXAMPLES</span></span>

### <span data-ttu-id="6a9cc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a9cc-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="6a9cc-112">"Myiothub" IoT Hub의 모든 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="6a9cc-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6a9cc-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="6a9cc-114">"Myiothub" IoT Hub에서 EventHub 유형의 모든 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="6a9cc-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6a9cc-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="6a9cc-116">"Myiothub" IoT Hub에서 EventHub 유형의 모든 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="6a9cc-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="6a9cc-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="6a9cc-118">"Myiothub" IoT Hub에서 끝점 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="6a9cc-119">변수</span><span class="sxs-lookup"><span data-stu-id="6a9cc-119">PARAMETERS</span></span>

### <span data-ttu-id="6a9cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9cc-120">-DefaultProfile</span></span>
<span data-ttu-id="6a9cc-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9cc-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6a9cc-122">-EndpointName</span></span>
<span data-ttu-id="6a9cc-123">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="6a9cc-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="6a9cc-124">-EndpointType</span></span>
<span data-ttu-id="6a9cc-125">라우팅 끝점의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9cc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a9cc-126">-InputObject</span></span>
<span data-ttu-id="6a9cc-127">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="6a9cc-127">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9cc-128">-이름</span><span class="sxs-lookup"><span data-stu-id="6a9cc-128">-Name</span></span>
<span data-ttu-id="6a9cc-129">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="6a9cc-129">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9cc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9cc-130">-ResourceGroupName</span></span>
<span data-ttu-id="6a9cc-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9cc-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a9cc-132">-ResourceId</span></span>
<span data-ttu-id="6a9cc-133">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="6a9cc-133">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9cc-134">CommonParameters</span></span>
<span data-ttu-id="6a9cc-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9cc-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9cc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9cc-137">입력</span><span class="sxs-lookup"><span data-stu-id="6a9cc-137">INPUTS</span></span>

### <span data-ttu-id="6a9cc-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="6a9cc-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6a9cc-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6a9cc-139">System.String</span></span>

## <span data-ttu-id="6a9cc-140">출력</span><span class="sxs-lookup"><span data-stu-id="6a9cc-140">OUTPUTS</span></span>

### <span data-ttu-id="6a9cc-141">IotHub. PSRoutingEventHubEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="6a9cc-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="6a9cc-142">System.webserver. List ' 1 [[IotHub. PSRoutingEventHubProperties, Microsoft IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]을 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6a9cc-143">IotHub를 통해 PSRoutingServiceBusQueueEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="6a9cc-144">IotHub. PSRoutingServiceBusQueueEndpointProperties 속성 []</span><span class="sxs-lookup"><span data-stu-id="6a9cc-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="6a9cc-145">IotHub. Psroutingservice Stopicendpoint.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="6a9cc-146">IotHub.-Psroutingservice Stopicendpointproperties []</span><span class="sxs-lookup"><span data-stu-id="6a9cc-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="6a9cc-147">IotHub. PSRoutingStorageContainerEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="6a9cc-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="6a9cc-148">IotHub를 PSRoutingStorageContainerProperties []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a9cc-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="6a9cc-149">IotHub. PSRoutingCustomEndpoint [] ()</span><span class="sxs-lookup"><span data-stu-id="6a9cc-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="6a9cc-150">상속자</span><span class="sxs-lookup"><span data-stu-id="6a9cc-150">NOTES</span></span>

## <span data-ttu-id="6a9cc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a9cc-151">RELATED LINKS</span></span>