---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: f162bf5f22ab435dd0d340bfd96db1ae616ccc96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217733"
---
# <span data-ttu-id="91542-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="91542-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="91542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91542-102">SYNOPSIS</span></span>
<span data-ttu-id="91542-103">IoT Hub의 끝점 삭제</span><span class="sxs-lookup"><span data-stu-id="91542-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="91542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91542-104">SYNTAX</span></span>

### <span data-ttu-id="91542-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="91542-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91542-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91542-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91542-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91542-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91542-108">설명은</span><span class="sxs-lookup"><span data-stu-id="91542-108">DESCRIPTION</span></span>
<span data-ttu-id="91542-109">끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="91542-109">Delete an endpoint.</span></span> <span data-ttu-id="91542-110">이 끝점을 사용 하는 모든 경로를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91542-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="91542-111">예제의</span><span class="sxs-lookup"><span data-stu-id="91542-111">EXAMPLES</span></span>

### <span data-ttu-id="91542-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="91542-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="91542-113">"Myiothub" IoT Hub에서 "E2" 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="91542-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="91542-114">변수</span><span class="sxs-lookup"><span data-stu-id="91542-114">PARAMETERS</span></span>

### <span data-ttu-id="91542-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91542-115">-DefaultProfile</span></span>
<span data-ttu-id="91542-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91542-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91542-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="91542-117">-EndpointName</span></span>
<span data-ttu-id="91542-118">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91542-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="91542-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="91542-119">-EndpointType</span></span>
<span data-ttu-id="91542-120">라우팅 끝점의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="91542-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="91542-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91542-121">-InputObject</span></span>
<span data-ttu-id="91542-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="91542-122">IotHub Object</span></span>

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

### <span data-ttu-id="91542-123">-이름</span><span class="sxs-lookup"><span data-stu-id="91542-123">-Name</span></span>
<span data-ttu-id="91542-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="91542-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="91542-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91542-125">-PassThru</span></span>
<span data-ttu-id="91542-126">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91542-126">Allows to return the boolean object.</span></span> <span data-ttu-id="91542-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91542-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91542-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91542-128">-ResourceGroupName</span></span>
<span data-ttu-id="91542-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91542-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91542-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91542-130">-ResourceId</span></span>
<span data-ttu-id="91542-131">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="91542-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="91542-132">-확인</span><span class="sxs-lookup"><span data-stu-id="91542-132">-Confirm</span></span>
<span data-ttu-id="91542-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91542-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91542-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91542-134">-WhatIf</span></span>
<span data-ttu-id="91542-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91542-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91542-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91542-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91542-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91542-137">CommonParameters</span></span>
<span data-ttu-id="91542-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91542-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91542-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91542-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91542-140">입력</span><span class="sxs-lookup"><span data-stu-id="91542-140">INPUTS</span></span>

### <span data-ttu-id="91542-141">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="91542-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="91542-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91542-142">System.String</span></span>

## <span data-ttu-id="91542-143">출력</span><span class="sxs-lookup"><span data-stu-id="91542-143">OUTPUTS</span></span>

### <span data-ttu-id="91542-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="91542-144">System.Boolean</span></span>

## <span data-ttu-id="91542-145">상속자</span><span class="sxs-lookup"><span data-stu-id="91542-145">NOTES</span></span>

## <span data-ttu-id="91542-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91542-146">RELATED LINKS</span></span>