---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: ac8fc7e3be69704b69fc2dfbfa30ec8df7bf996b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876744"
---
# <span data-ttu-id="a92e4-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a92e4-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a92e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a92e4-103">IoT Hub의 모든 끝점에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a92e4-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="a92e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a92e4-104">SYNTAX</span></span>

### <span data-ttu-id="a92e4-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a92e4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a92e4-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92e4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a92e4-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a92e4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a92e4-108">DESCRIPTION</span></span>
<span data-ttu-id="a92e4-109">끝점에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="a92e4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a92e4-110">EXAMPLES</span></span>

### <span data-ttu-id="a92e4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a92e4-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="a92e4-112">"Myiothub" IoT Hub의 모든 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a92e4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a92e4-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="a92e4-114">"Myiothub" IoT Hub에서 EventHub 유형의 모든 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="a92e4-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="a92e4-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a92e4-116">"Myiothub" IoT Hub에서 EventHub 유형의 모든 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a92e4-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="a92e4-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="a92e4-118">"Myiothub" IoT Hub에서 끝점 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a92e4-119">변수</span><span class="sxs-lookup"><span data-stu-id="a92e4-119">PARAMETERS</span></span>

### <span data-ttu-id="a92e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92e4-120">-DefaultProfile</span></span>
<span data-ttu-id="a92e4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a92e4-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a92e4-122">-EndpointName</span></span>
<span data-ttu-id="a92e4-123">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a92e4-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a92e4-124">-EndpointType</span></span>
<span data-ttu-id="a92e4-125">라우팅 끝점의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-125">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="a92e4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a92e4-126">-InputObject</span></span>
<span data-ttu-id="a92e4-127">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="a92e4-127">IotHub Object</span></span>

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

### <span data-ttu-id="a92e4-128">-이름</span><span class="sxs-lookup"><span data-stu-id="a92e4-128">-Name</span></span>
<span data-ttu-id="a92e4-129">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="a92e4-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a92e4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92e4-130">-ResourceGroupName</span></span>
<span data-ttu-id="a92e4-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a92e4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a92e4-132">-ResourceId</span></span>
<span data-ttu-id="a92e4-133">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="a92e4-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a92e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92e4-134">CommonParameters</span></span>
<span data-ttu-id="a92e4-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92e4-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92e4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92e4-137">입력</span><span class="sxs-lookup"><span data-stu-id="a92e4-137">INPUTS</span></span>

### <span data-ttu-id="a92e4-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="a92e4-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a92e4-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a92e4-139">System.String</span></span>

## <span data-ttu-id="a92e4-140">출력</span><span class="sxs-lookup"><span data-stu-id="a92e4-140">OUTPUTS</span></span>

### <span data-ttu-id="a92e4-141">IotHub. PSRoutingEventHubEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="a92e4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="a92e4-142">System.webserver. List ' 1 [[IotHub. PSRoutingEventHubProperties, Microsoft IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]을 목록으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a92e4-143">IotHub를 통해 PSRoutingServiceBusQueueEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a92e4-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="a92e4-144">IotHub. PSRoutingServiceBusQueueEndpointProperties 속성 []</span><span class="sxs-lookup"><span data-stu-id="a92e4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="a92e4-145">IotHub. Psroutingservice<c13> Stopicendpoint.</span><span class="sxs-lookup"><span data-stu-id="a92e4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="a92e4-146">IotHub.-Psroutingservice<c13> Stopicendpointproperties []</span><span class="sxs-lookup"><span data-stu-id="a92e4-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="a92e4-147">IotHub. PSRoutingStorageContainerEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="a92e4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="a92e4-148">IotHub를 PSRoutingStorageContainerProperties []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a92e4-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="a92e4-149">IotHub. PSRoutingCustomEndpoint [] ()</span><span class="sxs-lookup"><span data-stu-id="a92e4-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="a92e4-150">상속자</span><span class="sxs-lookup"><span data-stu-id="a92e4-150">NOTES</span></span>

## <span data-ttu-id="a92e4-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a92e4-151">RELATED LINKS</span></span>