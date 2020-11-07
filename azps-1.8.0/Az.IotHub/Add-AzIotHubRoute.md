---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: 7b850f87404a2523c8f91cb60f2f9f3aead97c5b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868154"
---
# <span data-ttu-id="8dfd1-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="8dfd1-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="8dfd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dfd1-102">SYNOPSIS</span></span>
<span data-ttu-id="8dfd1-103">IoT Hub에서 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="8dfd1-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="8dfd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dfd1-104">SYNTAX</span></span>

### <span data-ttu-id="8dfd1-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8dfd1-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfd1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8dfd1-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dfd1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8dfd1-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dfd1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8dfd1-108">DESCRIPTION</span></span>
<span data-ttu-id="8dfd1-109">경로를 만들어 특정 데이터 원본 및 조건을 원하는 끝점에 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="8dfd1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8dfd1-110">EXAMPLES</span></span>

### <span data-ttu-id="8dfd1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dfd1-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="8dfd1-112">새 경로 "R1"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-112">Create a new route "R1".</span></span>

## <span data-ttu-id="8dfd1-113">변수</span><span class="sxs-lookup"><span data-stu-id="8dfd1-113">PARAMETERS</span></span>

### <span data-ttu-id="8dfd1-114">-조건</span><span class="sxs-lookup"><span data-stu-id="8dfd1-114">-Condition</span></span>
<span data-ttu-id="8dfd1-115">라우팅 규칙을 적용 하도록 평가 되는 조건</span><span class="sxs-lookup"><span data-stu-id="8dfd1-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="8dfd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dfd1-116">-DefaultProfile</span></span>
<span data-ttu-id="8dfd1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dfd1-118">-사용</span><span class="sxs-lookup"><span data-stu-id="8dfd1-118">-Enabled</span></span>
<span data-ttu-id="8dfd1-119">경로 사용</span><span class="sxs-lookup"><span data-stu-id="8dfd1-119">Enable route</span></span>

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

### <span data-ttu-id="8dfd1-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-120">-EndpointName</span></span>
<span data-ttu-id="8dfd1-121">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-121">Name of the routing endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dfd1-122">-InputObject</span></span>
<span data-ttu-id="8dfd1-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="8dfd1-123">IotHub Object</span></span>

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

### <span data-ttu-id="8dfd1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8dfd1-124">-Name</span></span>
<span data-ttu-id="8dfd1-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="8dfd1-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8dfd1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-126">-ResourceGroupName</span></span>
<span data-ttu-id="8dfd1-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8dfd1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dfd1-128">-ResourceId</span></span>
<span data-ttu-id="8dfd1-129">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8dfd1-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8dfd1-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8dfd1-130">-RouteName</span></span>
<span data-ttu-id="8dfd1-131">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="8dfd1-131">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd1-132">-원본</span><span class="sxs-lookup"><span data-stu-id="8dfd1-132">-Source</span></span>
<span data-ttu-id="8dfd1-133">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="8dfd1-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dfd1-134">-확인</span><span class="sxs-lookup"><span data-stu-id="8dfd1-134">-Confirm</span></span>
<span data-ttu-id="8dfd1-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dfd1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dfd1-136">-WhatIf</span></span>
<span data-ttu-id="8dfd1-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dfd1-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dfd1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dfd1-139">CommonParameters</span></span>
<span data-ttu-id="8dfd1-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dfd1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dfd1-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dfd1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dfd1-142">입력</span><span class="sxs-lookup"><span data-stu-id="8dfd1-142">INPUTS</span></span>

### <span data-ttu-id="8dfd1-143">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="8dfd1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8dfd1-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8dfd1-144">System.String</span></span>

## <span data-ttu-id="8dfd1-145">출력</span><span class="sxs-lookup"><span data-stu-id="8dfd1-145">OUTPUTS</span></span>

### <span data-ttu-id="8dfd1-146">IotHub. PSRouteMetadata/. \*</span><span class="sxs-lookup"><span data-stu-id="8dfd1-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="8dfd1-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8dfd1-147">NOTES</span></span>

## <span data-ttu-id="8dfd1-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dfd1-148">RELATED LINKS</span></span>