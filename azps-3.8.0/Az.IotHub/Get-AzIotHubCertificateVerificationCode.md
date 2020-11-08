---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033914"
---
# <span data-ttu-id="7cefb-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="7cefb-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="7cefb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cefb-102">SYNOPSIS</span></span>
<span data-ttu-id="7cefb-103">Azure IoT Hub 인증서에 대 한 확인 코드를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="7cefb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7cefb-104">SYNTAX</span></span>

### <span data-ttu-id="7cefb-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7cefb-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cefb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7cefb-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cefb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7cefb-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cefb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7cefb-108">DESCRIPTION</span></span>
<span data-ttu-id="7cefb-109">이 확인 코드는 인증서에 대 한 소유 단계 증명을 완료 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="7cefb-110">이 확인 코드를 루트 인증서 개인 키를 사용 하 여 서명 된 새 인증서의 CN으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="7cefb-111">Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="7cefb-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="7cefb-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7cefb-112">EXAMPLES</span></span>

### <span data-ttu-id="7cefb-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7cefb-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="7cefb-114">MyCertificate에 대 한 확인 코드를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="7cefb-115">변수</span><span class="sxs-lookup"><span data-stu-id="7cefb-115">PARAMETERS</span></span>

### <span data-ttu-id="7cefb-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7cefb-116">-CertificateName</span></span>
<span data-ttu-id="7cefb-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="7cefb-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cefb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cefb-118">-DefaultProfile</span></span>
<span data-ttu-id="7cefb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cefb-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="7cefb-120">-Etag</span></span>
<span data-ttu-id="7cefb-121">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="7cefb-121">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cefb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cefb-122">-InputObject</span></span>
<span data-ttu-id="7cefb-123">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="7cefb-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cefb-124">-이름</span><span class="sxs-lookup"><span data-stu-id="7cefb-124">-Name</span></span>
<span data-ttu-id="7cefb-125">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="7cefb-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cefb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cefb-126">-ResourceGroupName</span></span>
<span data-ttu-id="7cefb-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cefb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cefb-128">-ResourceId</span></span>
<span data-ttu-id="7cefb-129">인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7cefb-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="7cefb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cefb-130">CommonParameters</span></span>
<span data-ttu-id="7cefb-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7cefb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cefb-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cefb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cefb-133">입력</span><span class="sxs-lookup"><span data-stu-id="7cefb-133">INPUTS</span></span>

### <span data-ttu-id="7cefb-134">IotHub. PSCertificateDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="7cefb-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="7cefb-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7cefb-135">System.String</span></span>

## <span data-ttu-id="7cefb-136">출력</span><span class="sxs-lookup"><span data-stu-id="7cefb-136">OUTPUTS</span></span>

### <span data-ttu-id="7cefb-137">IotHub. PSCertificateWithNonceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="7cefb-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="7cefb-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7cefb-138">NOTES</span></span>

## <span data-ttu-id="7cefb-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cefb-139">RELATED LINKS</span></span>