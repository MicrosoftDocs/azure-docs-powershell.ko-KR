---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327585"
---
# <span data-ttu-id="78d05-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="78d05-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="78d05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78d05-102">SYNOPSIS</span></span>
<span data-ttu-id="78d05-103">IoT Edge 배포의 변경 가능한 필드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="78d05-104">구문</span><span class="sxs-lookup"><span data-stu-id="78d05-104">SYNTAX</span></span>

### <span data-ttu-id="78d05-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="78d05-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d05-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="78d05-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d05-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="78d05-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d05-108">설명</span><span class="sxs-lookup"><span data-stu-id="78d05-108">DESCRIPTION</span></span>
<span data-ttu-id="78d05-109">IoT Edge 배포의 지정된 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="78d05-110">참고: 구성 콘텐츠는 변경 불가능합니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="78d05-111">업데이트할 수 있는 구성 속성은 'labels', 'metrics', 'priority' 및 'targetCondition'입니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="78d05-112">자세한 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  내용은 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78d05-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="78d05-113">예제</span><span class="sxs-lookup"><span data-stu-id="78d05-113">EXAMPLES</span></span>

### <span data-ttu-id="78d05-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="78d05-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="78d05-115">IoT Edge 배포의 우선 순위를 변경하고 대상 조건을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="78d05-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="78d05-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="78d05-117">IoT Edge 배포의 메트릭 및 레이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="78d05-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78d05-118">PARAMETERS</span></span>

### <span data-ttu-id="78d05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d05-119">-DefaultProfile</span></span>
<span data-ttu-id="78d05-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78d05-121">-Force</span><span class="sxs-lookup"><span data-stu-id="78d05-121">-Force</span></span>
<span data-ttu-id="78d05-122">배포 개체를 마지막으로 검색한 후 업데이트한 경우에도 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="78d05-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78d05-123">-InputObject</span></span>
<span data-ttu-id="78d05-124">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="78d05-124">IotHub object</span></span>

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

### <span data-ttu-id="78d05-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="78d05-125">-IotHubName</span></span>
<span data-ttu-id="78d05-126">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="78d05-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="78d05-127">-Label</span><span class="sxs-lookup"><span data-stu-id="78d05-127">-Label</span></span>
<span data-ttu-id="78d05-128">대상 배포에 적용할 레이블의 맵입니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="78d05-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="78d05-129">-Metric</span></span>
<span data-ttu-id="78d05-130">IoT Edge 배포 메트릭 정의에 대한 쿼리 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="78d05-131">-Name</span><span class="sxs-lookup"><span data-stu-id="78d05-131">-Name</span></span>
<span data-ttu-id="78d05-132">배포에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="78d05-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="78d05-133">-Priority</span></span>
<span data-ttu-id="78d05-134">경쟁 규칙의 경우 배포 가중치(최고 우승).</span><span class="sxs-lookup"><span data-stu-id="78d05-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="78d05-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d05-135">-ResourceGroupName</span></span>
<span data-ttu-id="78d05-136">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="78d05-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="78d05-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78d05-137">-ResourceId</span></span>
<span data-ttu-id="78d05-138">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="78d05-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="78d05-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="78d05-139">-TargetCondition</span></span>
<span data-ttu-id="78d05-140">Edge 배포가 적용되는 대상 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="78d05-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78d05-141">-Confirm</span></span>
<span data-ttu-id="78d05-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d05-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d05-143">-WhatIf</span></span>
<span data-ttu-id="78d05-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="78d05-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d05-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d05-146">CommonParameters</span></span>
<span data-ttu-id="78d05-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78d05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d05-148">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="78d05-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d05-149">입력</span><span class="sxs-lookup"><span data-stu-id="78d05-149">INPUTS</span></span>

### <span data-ttu-id="78d05-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="78d05-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="78d05-151">System.String</span><span class="sxs-lookup"><span data-stu-id="78d05-151">System.String</span></span>

## <span data-ttu-id="78d05-152">출력</span><span class="sxs-lookup"><span data-stu-id="78d05-152">OUTPUTS</span></span>

### <span data-ttu-id="78d05-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="78d05-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="78d05-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78d05-154">NOTES</span></span>

## <span data-ttu-id="78d05-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78d05-155">RELATED LINKS</span></span>