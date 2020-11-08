---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217749"
---
# <span data-ttu-id="7c9f3-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7c9f3-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="7c9f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9f3-103">장치 트윈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-103">Gets a device twin.</span></span>

## <span data-ttu-id="7c9f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c9f3-104">SYNTAX</span></span>

### <span data-ttu-id="7c9f3-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c9f3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c9f3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c9f3-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c9f3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c9f3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c9f3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c9f3-108">DESCRIPTION</span></span>
<span data-ttu-id="7c9f3-109">장치 트윈을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-109">Gets a device twin.</span></span> <span data-ttu-id="7c9f3-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="7c9f3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7c9f3-111">EXAMPLES</span></span>

### <span data-ttu-id="7c9f3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c9f3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="7c9f3-113">장치 트윈 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-113">Returns the device twin object.</span></span>

## <span data-ttu-id="7c9f3-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c9f3-114">PARAMETERS</span></span>

### <span data-ttu-id="7c9f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9f3-115">-DefaultProfile</span></span>
<span data-ttu-id="7c9f3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c9f3-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7c9f3-117">-DeviceId</span></span>
<span data-ttu-id="7c9f3-118">대상 장치 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-118">Target Device Id.</span></span>

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

### <span data-ttu-id="7c9f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c9f3-119">-InputObject</span></span>
<span data-ttu-id="7c9f3-120">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="7c9f3-120">IotHub object</span></span>

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

### <span data-ttu-id="7c9f3-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7c9f3-121">-IotHubName</span></span>
<span data-ttu-id="7c9f3-122">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="7c9f3-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7c9f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c9f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c9f3-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c9f3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c9f3-125">-ResourceId</span></span>
<span data-ttu-id="7c9f3-126">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7c9f3-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7c9f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9f3-127">CommonParameters</span></span>
<span data-ttu-id="7c9f3-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c9f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9f3-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c9f3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9f3-130">입력</span><span class="sxs-lookup"><span data-stu-id="7c9f3-130">INPUTS</span></span>

### <span data-ttu-id="7c9f3-131">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="7c9f3-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7c9f3-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c9f3-132">System.String</span></span>

## <span data-ttu-id="7c9f3-133">출력</span><span class="sxs-lookup"><span data-stu-id="7c9f3-133">OUTPUTS</span></span>

### <span data-ttu-id="7c9f3-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7c9f3-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="7c9f3-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7c9f3-135">NOTES</span></span>

## <span data-ttu-id="7c9f3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c9f3-136">RELATED LINKS</span></span>