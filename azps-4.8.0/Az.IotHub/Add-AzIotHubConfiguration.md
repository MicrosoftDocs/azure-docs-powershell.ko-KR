---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211981"
---
# <span data-ttu-id="62690-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="62690-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="62690-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62690-102">SYNOPSIS</span></span>
<span data-ttu-id="62690-103">대상 IoT Hub에 IoT 자동 장치 관리 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="62690-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="62690-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62690-104">SYNTAX</span></span>

### <span data-ttu-id="62690-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="62690-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62690-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62690-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62690-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62690-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62690-108">설명은</span><span class="sxs-lookup"><span data-stu-id="62690-108">DESCRIPTION</span></span>
<span data-ttu-id="62690-109">구성 콘텐츠는 json 이며 장치 또는 모듈 의도에 따라 slighty 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="62690-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="62690-110">장치 구성은 {"deviceContent": {...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="62690-111">모듈 구성은 {"moduleContent": {...}} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="62690-112">구성을 사용 하 여 요청을 평가할 때 사용자가 제공한 메트릭을 정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62690-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="62690-113">사용자 메트릭은 {"쿼리": {...}}의 형식으로 된 json입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="62690-114">또는 {"메트릭스": {"쿼리": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="62690-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="62690-115">참고: 모듈의 대상 조건은 "on devices. 모듈"로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="62690-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="62690-116"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="62690-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="62690-117">예제의</span><span class="sxs-lookup"><span data-stu-id="62690-117">EXAMPLES</span></span>

### <span data-ttu-id="62690-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="62690-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="62690-119">기본 메타 데이터로 장치 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62690-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="62690-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="62690-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="62690-121">장치가 빌드 9에 태그가 지정 되 고 환경이 ' 테스트 ' 인 경우 조건에 적용 되는 우선 순위 3을 사용 하 여 디바이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62690-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="62690-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="62690-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="62690-123">사용자 메트릭을 사용 하 여 디바이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62690-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="62690-124">예제 3</span><span class="sxs-lookup"><span data-stu-id="62690-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="62690-125">레이블을 사용 하 여 디바이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62690-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="62690-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="62690-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="62690-127">콘텐츠를 사용 하 여 디바이스 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62690-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="62690-128">변수</span><span class="sxs-lookup"><span data-stu-id="62690-128">PARAMETERS</span></span>

### <span data-ttu-id="62690-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62690-129">-DefaultProfile</span></span>
<span data-ttu-id="62690-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62690-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="62690-131">-DeviceContent</span></span>
<span data-ttu-id="62690-132">IotHub 장치에 대 한 구성.</span><span class="sxs-lookup"><span data-stu-id="62690-132">Configuration for IotHub devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62690-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62690-133">-InputObject</span></span>
<span data-ttu-id="62690-134">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="62690-134">IotHub object</span></span>

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

### <span data-ttu-id="62690-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62690-135">-IotHubName</span></span>
<span data-ttu-id="62690-136">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="62690-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62690-137">-레이블</span><span class="sxs-lookup"><span data-stu-id="62690-137">-Label</span></span>
<span data-ttu-id="62690-138">대상 구성에 적용 되는 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-138">Map of labels to be applied to target configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62690-139">-미터법</span><span class="sxs-lookup"><span data-stu-id="62690-139">-Metric</span></span>
<span data-ttu-id="62690-140">구성 메트릭 정의에 대 한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-140">Queries collection for configuration metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62690-141">-이름</span><span class="sxs-lookup"><span data-stu-id="62690-141">-Name</span></span>
<span data-ttu-id="62690-142">구성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="62690-143">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="62690-143">-Priority</span></span>
<span data-ttu-id="62690-144">경합 하는 규칙 (최고 wins)에 대 한 장치 구성의 가중치.</span><span class="sxs-lookup"><span data-stu-id="62690-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62690-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62690-145">-ResourceGroupName</span></span>
<span data-ttu-id="62690-146">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62690-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62690-147">-ResourceId</span></span>
<span data-ttu-id="62690-148">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="62690-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62690-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="62690-149">-TargetCondition</span></span>
<span data-ttu-id="62690-150">장치 구성이 적용 되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="62690-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="62690-151">-확인</span><span class="sxs-lookup"><span data-stu-id="62690-151">-Confirm</span></span>
<span data-ttu-id="62690-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62690-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62690-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62690-153">-WhatIf</span></span>
<span data-ttu-id="62690-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62690-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62690-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62690-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62690-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62690-156">CommonParameters</span></span>
<span data-ttu-id="62690-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62690-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62690-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62690-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62690-159">입력</span><span class="sxs-lookup"><span data-stu-id="62690-159">INPUTS</span></span>

### <span data-ttu-id="62690-160">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="62690-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62690-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62690-161">System.String</span></span>

## <span data-ttu-id="62690-162">출력</span><span class="sxs-lookup"><span data-stu-id="62690-162">OUTPUTS</span></span>

### <span data-ttu-id="62690-163">IotHub에 대 한. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="62690-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="62690-164">상속자</span><span class="sxs-lookup"><span data-stu-id="62690-164">NOTES</span></span>

## <span data-ttu-id="62690-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62690-165">RELATED LINKS</span></span>