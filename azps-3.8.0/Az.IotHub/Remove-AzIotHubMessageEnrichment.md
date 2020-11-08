---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034885"
---
# <span data-ttu-id="cb071-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cb071-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="cb071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb071-102">SYNOPSIS</span></span>
<span data-ttu-id="cb071-103">IoT hub에서 메시지 보강를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="cb071-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb071-104">SYNTAX</span></span>

### <span data-ttu-id="cb071-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cb071-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb071-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb071-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb071-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb071-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb071-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cb071-108">DESCRIPTION</span></span>
<span data-ttu-id="cb071-109">Azure IoT Hub의 메시지 enrichments에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="cb071-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="cb071-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cb071-110">EXAMPLES</span></span>

### <span data-ttu-id="cb071-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb071-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="cb071-112">"NewKey" 메시지 보강를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="cb071-113">변수</span><span class="sxs-lookup"><span data-stu-id="cb071-113">PARAMETERS</span></span>

### <span data-ttu-id="cb071-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb071-114">-DefaultProfile</span></span>
<span data-ttu-id="cb071-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb071-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb071-116">-InputObject</span></span>
<span data-ttu-id="cb071-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="cb071-117">IotHub object</span></span>

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

### <span data-ttu-id="cb071-118">-키</span><span class="sxs-lookup"><span data-stu-id="cb071-118">-Key</span></span>
<span data-ttu-id="cb071-119">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="cb071-120">-이름</span><span class="sxs-lookup"><span data-stu-id="cb071-120">-Name</span></span>
<span data-ttu-id="cb071-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="cb071-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cb071-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb071-122">-PassThru</span></span>
<span data-ttu-id="cb071-123">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="cb071-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb071-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb071-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb071-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cb071-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb071-127">-ResourceId</span></span>
<span data-ttu-id="cb071-128">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="cb071-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cb071-129">-확인</span><span class="sxs-lookup"><span data-stu-id="cb071-129">-Confirm</span></span>
<span data-ttu-id="cb071-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb071-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb071-131">-WhatIf</span></span>
<span data-ttu-id="cb071-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb071-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb071-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb071-134">CommonParameters</span></span>
<span data-ttu-id="cb071-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb071-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb071-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb071-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb071-137">입력</span><span class="sxs-lookup"><span data-stu-id="cb071-137">INPUTS</span></span>

### <span data-ttu-id="cb071-138">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="cb071-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cb071-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cb071-139">System.String</span></span>

## <span data-ttu-id="cb071-140">출력</span><span class="sxs-lookup"><span data-stu-id="cb071-140">OUTPUTS</span></span>

### <span data-ttu-id="cb071-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cb071-141">System.Boolean</span></span>

## <span data-ttu-id="cb071-142">상속자</span><span class="sxs-lookup"><span data-stu-id="cb071-142">NOTES</span></span>

## <span data-ttu-id="cb071-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb071-143">RELATED LINKS</span></span>