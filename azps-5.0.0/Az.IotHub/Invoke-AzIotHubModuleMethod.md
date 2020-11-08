---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226978"
---
# <span data-ttu-id="31bb3-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="31bb3-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="31bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="31bb3-103">Edge 모듈 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="31bb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31bb3-104">SYNTAX</span></span>

### <span data-ttu-id="31bb3-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="31bb3-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31bb3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31bb3-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bb3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31bb3-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31bb3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="31bb3-108">DESCRIPTION</span></span>
<span data-ttu-id="31bb3-109">Edge 모듈 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-109">Invoke an Edge module method.</span></span> <span data-ttu-id="31bb3-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31bb3-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="31bb3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="31bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="31bb3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="31bb3-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="31bb3-113">Edge 모듈 메서드를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="31bb3-114">변수</span><span class="sxs-lookup"><span data-stu-id="31bb3-114">PARAMETERS</span></span>

### <span data-ttu-id="31bb3-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="31bb3-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="31bb3-116">연결을 설정할 때까지 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="31bb3-117">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-117">Default is 10.</span></span>

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

### <span data-ttu-id="31bb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bb3-118">-DefaultProfile</span></span>
<span data-ttu-id="31bb3-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31bb3-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="31bb3-120">-DeviceId</span></span>
<span data-ttu-id="31bb3-121">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-121">Target Device Id.</span></span>

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

### <span data-ttu-id="31bb3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bb3-122">-InputObject</span></span>
<span data-ttu-id="31bb3-123">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="31bb3-123">IotHub object</span></span>

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

### <span data-ttu-id="31bb3-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="31bb3-124">-IotHubName</span></span>
<span data-ttu-id="31bb3-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="31bb3-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="31bb3-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="31bb3-126">-ModuleId</span></span>
<span data-ttu-id="31bb3-127">대상 디바이스의 모듈 id입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bb3-128">-이름</span><span class="sxs-lookup"><span data-stu-id="31bb3-128">-Name</span></span>
<span data-ttu-id="31bb3-129">이 장치 모듈에서 호출할 메서드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="31bb3-130">-페이로드</span><span class="sxs-lookup"><span data-stu-id="31bb3-130">-Payload</span></span>
<span data-ttu-id="31bb3-131">이 장치 모듈에서 호출할 메서드의 페이로드입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="31bb3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bb3-132">-ResourceGroupName</span></span>
<span data-ttu-id="31bb3-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="31bb3-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31bb3-134">-ResourceId</span></span>
<span data-ttu-id="31bb3-135">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="31bb3-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="31bb3-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="31bb3-136">-ResponseTimeOut</span></span>
<span data-ttu-id="31bb3-137">Direct 메서드에서 결과를 받을 때까지 대기 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="31bb3-138">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-138">Default is 10.</span></span>

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

### <span data-ttu-id="31bb3-139">-확인</span><span class="sxs-lookup"><span data-stu-id="31bb3-139">-Confirm</span></span>
<span data-ttu-id="31bb3-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31bb3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bb3-141">-WhatIf</span></span>
<span data-ttu-id="31bb3-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31bb3-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31bb3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bb3-144">CommonParameters</span></span>
<span data-ttu-id="31bb3-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31bb3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bb3-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31bb3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bb3-147">입력</span><span class="sxs-lookup"><span data-stu-id="31bb3-147">INPUTS</span></span>

### <span data-ttu-id="31bb3-148">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="31bb3-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="31bb3-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="31bb3-149">System.String</span></span>

## <span data-ttu-id="31bb3-150">출력</span><span class="sxs-lookup"><span data-stu-id="31bb3-150">OUTPUTS</span></span>

### <span data-ttu-id="31bb3-151">IotHub. PSCloudToDeviceMethodResult/. \*</span><span class="sxs-lookup"><span data-stu-id="31bb3-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="31bb3-152">상속자</span><span class="sxs-lookup"><span data-stu-id="31bb3-152">NOTES</span></span>

## <span data-ttu-id="31bb3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31bb3-153">RELATED LINKS</span></span>