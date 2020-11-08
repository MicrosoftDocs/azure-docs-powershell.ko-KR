---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056374"
---
# <span data-ttu-id="dd57b-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="dd57b-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="dd57b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd57b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd57b-103">장치 등록 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-103">Gets the device registration state.</span></span>

## <span data-ttu-id="dd57b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd57b-104">SYNTAX</span></span>

### <span data-ttu-id="dd57b-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dd57b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd57b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd57b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd57b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dd57b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd57b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dd57b-108">DESCRIPTION</span></span>
<span data-ttu-id="dd57b-109">Azure IoT Hub Device 프로비저닝 서비스에서 enrollmentGroup 아래에 디바이스 등록 상태 또는 장치 등록 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="dd57b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dd57b-110">EXAMPLES</span></span>

### <span data-ttu-id="dd57b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd57b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="dd57b-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 등록 상태 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="dd57b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dd57b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="dd57b-114">이 enrollmentGroup의 모든 장치에 대 한 등록 상태를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="dd57b-115">변수</span><span class="sxs-lookup"><span data-stu-id="dd57b-115">PARAMETERS</span></span>

### <span data-ttu-id="dd57b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd57b-116">-DefaultProfile</span></span>
<span data-ttu-id="dd57b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd57b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="dd57b-118">-DpsName</span></span>
<span data-ttu-id="dd57b-119">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="dd57b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dd57b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="dd57b-120">-DpsObject</span></span>
<span data-ttu-id="dd57b-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="dd57b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="dd57b-122">-등록 Id</span><span class="sxs-lookup"><span data-stu-id="dd57b-122">-EnrollmentId</span></span>
<span data-ttu-id="dd57b-123">등록 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="dd57b-124">-쿼리</span><span class="sxs-lookup"><span data-stu-id="dd57b-124">-Query</span></span>
<span data-ttu-id="dd57b-125">Sql 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-125">Sql query.</span></span>

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

### <span data-ttu-id="dd57b-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="dd57b-126">-RegistrationId</span></span>
<span data-ttu-id="dd57b-127">디바이스 등록의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-127">ID of device registration.</span></span>

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

### <span data-ttu-id="dd57b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd57b-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd57b-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dd57b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd57b-130">-ResourceId</span></span>
<span data-ttu-id="dd57b-131">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="dd57b-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dd57b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd57b-132">CommonParameters</span></span>
<span data-ttu-id="dd57b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd57b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd57b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd57b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd57b-135">입력</span><span class="sxs-lookup"><span data-stu-id="dd57b-135">INPUTS</span></span>

### <span data-ttu-id="dd57b-136">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="dd57b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="dd57b-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd57b-137">System.String</span></span>

## <span data-ttu-id="dd57b-138">출력</span><span class="sxs-lookup"><span data-stu-id="dd57b-138">OUTPUTS</span></span>

### <span data-ttu-id="dd57b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="dd57b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="dd57b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="dd57b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="dd57b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="dd57b-141">NOTES</span></span>

## <span data-ttu-id="dd57b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd57b-142">RELATED LINKS</span></span>