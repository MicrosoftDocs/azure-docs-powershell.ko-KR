---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524435"
---
# <span data-ttu-id="32c2a-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="32c2a-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="32c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="32c2a-103">Azure IoT Hub Device 프로비저닝 서비스에 포함 된 모든 인증서 또는 특정 인증서를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c2a-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32c2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32c2a-104">SYNTAX</span></span>

### <span data-ttu-id="32c2a-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="32c2a-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32c2a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="32c2a-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32c2a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="32c2a-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32c2a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="32c2a-108">DESCRIPTION</span></span>
<span data-ttu-id="32c2a-109">Azure IoT Hub Device 프로비저닝 서비스의 CA 인증서에 대 한 자세한 설명은을 참조 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 하세요.</span><span class="sxs-lookup"><span data-stu-id="32c2a-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="32c2a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="32c2a-110">EXAMPLES</span></span>

### <span data-ttu-id="32c2a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="32c2a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="32c2a-112">Azure IoT Hub 디바이스 프로비저닝 서비스의 "mycertificate"에 대 한 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c2a-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="32c2a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="32c2a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="32c2a-114">파이프라인을 사용 하 여 "myiotdps"의 모든 인증서를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c2a-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="32c2a-115">변수</span><span class="sxs-lookup"><span data-stu-id="32c2a-115">PARAMETERS</span></span>

### <span data-ttu-id="32c2a-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="32c2a-116">-CertificateName</span></span>
<span data-ttu-id="32c2a-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="32c2a-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="32c2a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c2a-118">-DefaultProfile</span></span>
<span data-ttu-id="32c2a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32c2a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32c2a-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="32c2a-120">-DpsObject</span></span>
<span data-ttu-id="32c2a-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="32c2a-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="32c2a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="32c2a-122">-Name</span></span>
<span data-ttu-id="32c2a-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="32c2a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="32c2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32c2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="32c2a-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32c2a-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="32c2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32c2a-126">-ResourceId</span></span>
<span data-ttu-id="32c2a-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="32c2a-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="32c2a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c2a-128">CommonParameters</span></span>
<span data-ttu-id="32c2a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c2a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c2a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32c2a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c2a-131">입력</span><span class="sxs-lookup"><span data-stu-id="32c2a-131">INPUTS</span></span>

### <span data-ttu-id="32c2a-132">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="32c2a-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="32c2a-133">매개 변수: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32c2a-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="32c2a-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32c2a-134">System.String</span></span>

## <span data-ttu-id="32c2a-135">출력</span><span class="sxs-lookup"><span data-stu-id="32c2a-135">OUTPUTS</span></span>

### <span data-ttu-id="32c2a-136">DeviceProvisioningServices. PSCertificateResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="32c2a-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="32c2a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="32c2a-137">NOTES</span></span>

## <span data-ttu-id="32c2a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32c2a-138">RELATED LINKS</span></span>