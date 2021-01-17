---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376958"
---
# <span data-ttu-id="fd7e2-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="fd7e2-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="fd7e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e2-103">디바이스 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="fd7e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd7e2-104">SYNTAX</span></span>

### <span data-ttu-id="fd7e2-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd7e2-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd7e2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd7e2-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd7e2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd7e2-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7e2-108">설명</span><span class="sxs-lookup"><span data-stu-id="fd7e2-108">DESCRIPTION</span></span>
<span data-ttu-id="fd7e2-109">Azure IoT Hub Device Provisioning Service에서 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fd7e2-110">예제</span><span class="sxs-lookup"><span data-stu-id="fd7e2-110">EXAMPLES</span></span>

### <span data-ttu-id="fd7e2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fd7e2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="fd7e2-112">지정된 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="fd7e2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fd7e2-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="fd7e2-114">모든 등록 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="fd7e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd7e2-115">PARAMETERS</span></span>

### <span data-ttu-id="fd7e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e2-116">-DefaultProfile</span></span>
<span data-ttu-id="fd7e2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd7e2-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="fd7e2-118">-DpsName</span></span>
<span data-ttu-id="fd7e2-119">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="fd7e2-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fd7e2-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fd7e2-120">-DpsObject</span></span>
<span data-ttu-id="fd7e2-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="fd7e2-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fd7e2-122">-Name</span></span>
<span data-ttu-id="fd7e2-123">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="fd7e2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd7e2-124">-PassThru</span></span>
<span data-ttu-id="fd7e2-125">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="fd7e2-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd7e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd7e2-128">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fd7e2-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd7e2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7e2-129">-ResourceId</span></span>
<span data-ttu-id="fd7e2-130">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fd7e2-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fd7e2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd7e2-131">-Confirm</span></span>
<span data-ttu-id="fd7e2-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7e2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7e2-133">-WhatIf</span></span>
<span data-ttu-id="fd7e2-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fd7e2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd7e2-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e2-136">CommonParameters</span></span>
<span data-ttu-id="fd7e2-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e2-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fd7e2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e2-139">입력</span><span class="sxs-lookup"><span data-stu-id="fd7e2-139">INPUTS</span></span>

### <span data-ttu-id="fd7e2-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fd7e2-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fd7e2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fd7e2-141">System.String</span></span>

## <span data-ttu-id="fd7e2-142">출력</span><span class="sxs-lookup"><span data-stu-id="fd7e2-142">OUTPUTS</span></span>

### <span data-ttu-id="fd7e2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd7e2-143">System.Boolean</span></span>

## <span data-ttu-id="fd7e2-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd7e2-144">NOTES</span></span>

## <span data-ttu-id="fd7e2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd7e2-145">RELATED LINKS</span></span>