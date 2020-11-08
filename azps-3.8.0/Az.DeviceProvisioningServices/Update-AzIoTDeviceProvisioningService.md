---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 411d4594c94fe1eb031f60d6abbff35f5060d4e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041902"
---
# <span data-ttu-id="0e73f-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0e73f-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0e73f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e73f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e73f-103">Azure IoT Hub 디바이스 프로비저닝 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0e73f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e73f-104">SYNTAX</span></span>

### <span data-ttu-id="0e73f-105">ResourceUpdateSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e73f-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e73f-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0e73f-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e73f-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0e73f-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e73f-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0e73f-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e73f-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0e73f-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e73f-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0e73f-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e73f-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0e73f-111">DESCRIPTION</span></span>
<span data-ttu-id="0e73f-112">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e73f-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0e73f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0e73f-113">EXAMPLES</span></span>

### <span data-ttu-id="0e73f-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e73f-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="0e73f-115">Azure IoT Hub device 프로비저닝 서비스 "myiotdps"의 "GeoLatency"에 할당 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0e73f-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="0e73f-116">Example 2</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="0e73f-117">@tagsAzure IoT Hub device 프로비저닝 서비스 "myiotdps"의 태그에 ""를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0e73f-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="0e73f-118">Example 3</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag @tags -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="0e73f-119">@tags파이프라인을 사용 하 여 태그를 삭제 하 고 "myiotdps" 서비스의 태그에 새 ""를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="0e73f-120">변수</span><span class="sxs-lookup"><span data-stu-id="0e73f-120">PARAMETERS</span></span>

### <span data-ttu-id="0e73f-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0e73f-121">-AllocationPolicy</span></span>
<span data-ttu-id="0e73f-122">IoT Device 프로 비전 서비스 할당 정책</span><span class="sxs-lookup"><span data-stu-id="0e73f-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e73f-123">-DefaultProfile</span></span>
<span data-ttu-id="0e73f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e73f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e73f-125">-InputObject</span></span>
<span data-ttu-id="0e73f-126">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="0e73f-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-127">-이름</span><span class="sxs-lookup"><span data-stu-id="0e73f-127">-Name</span></span>
<span data-ttu-id="0e73f-128">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="0e73f-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="0e73f-129">-Reset</span></span>
<span data-ttu-id="0e73f-130">IoT Device 프로비저닝 서비스 태그 다시 설정</span><span class="sxs-lookup"><span data-stu-id="0e73f-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e73f-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e73f-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e73f-133">-ResourceId</span></span>
<span data-ttu-id="0e73f-134">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="0e73f-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-135">태그</span><span class="sxs-lookup"><span data-stu-id="0e73f-135">-Tag</span></span>
<span data-ttu-id="0e73f-136">IoT Device 프로 비전 서비스 태그 모음</span><span class="sxs-lookup"><span data-stu-id="0e73f-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e73f-137">-확인</span><span class="sxs-lookup"><span data-stu-id="0e73f-137">-Confirm</span></span>
<span data-ttu-id="0e73f-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e73f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e73f-139">-WhatIf</span></span>
<span data-ttu-id="0e73f-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e73f-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e73f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e73f-142">CommonParameters</span></span>
<span data-ttu-id="0e73f-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e73f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e73f-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e73f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e73f-145">입력</span><span class="sxs-lookup"><span data-stu-id="0e73f-145">INPUTS</span></span>

### <span data-ttu-id="0e73f-146">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="0e73f-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0e73f-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e73f-147">System.String</span></span>

## <span data-ttu-id="0e73f-148">출력</span><span class="sxs-lookup"><span data-stu-id="0e73f-148">OUTPUTS</span></span>

### <span data-ttu-id="0e73f-149">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="0e73f-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="0e73f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="0e73f-150">NOTES</span></span>

## <span data-ttu-id="0e73f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e73f-151">RELATED LINKS</span></span>