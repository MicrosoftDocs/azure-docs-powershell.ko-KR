---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386653"
---
# <span data-ttu-id="d7724-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d7724-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="d7724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7724-102">SYNOPSIS</span></span>
<span data-ttu-id="d7724-103">IoT Hub에서 메시지 보강을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="d7724-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7724-104">SYNTAX</span></span>

### <span data-ttu-id="d7724-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7724-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7724-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d7724-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7724-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d7724-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7724-108">설명</span><span class="sxs-lookup"><span data-stu-id="d7724-108">DESCRIPTION</span></span>
<span data-ttu-id="d7724-109">Azure IoT Hub의 메시지 보강에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="d7724-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="d7724-110">예제</span><span class="sxs-lookup"><span data-stu-id="d7724-110">EXAMPLES</span></span>

### <span data-ttu-id="d7724-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7724-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="d7724-112">"newKey" 메시지 보강을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="d7724-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7724-113">PARAMETERS</span></span>

### <span data-ttu-id="d7724-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7724-114">-DefaultProfile</span></span>
<span data-ttu-id="d7724-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7724-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7724-116">-InputObject</span></span>
<span data-ttu-id="d7724-117">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="d7724-117">IotHub object</span></span>

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

### <span data-ttu-id="d7724-118">-Key</span><span class="sxs-lookup"><span data-stu-id="d7724-118">-Key</span></span>
<span data-ttu-id="d7724-119">보강의 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-119">The enrichment's key.</span></span>

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

### <span data-ttu-id="d7724-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d7724-120">-Name</span></span>
<span data-ttu-id="d7724-121">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d7724-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d7724-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7724-122">-PassThru</span></span>
<span data-ttu-id="d7724-123">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="d7724-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7724-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7724-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7724-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d7724-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d7724-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7724-127">-ResourceId</span></span>
<span data-ttu-id="d7724-128">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d7724-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d7724-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7724-129">-Confirm</span></span>
<span data-ttu-id="d7724-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7724-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7724-131">-WhatIf</span></span>
<span data-ttu-id="d7724-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d7724-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7724-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7724-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7724-134">CommonParameters</span></span>
<span data-ttu-id="d7724-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7724-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7724-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d7724-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7724-137">입력</span><span class="sxs-lookup"><span data-stu-id="d7724-137">INPUTS</span></span>

### <span data-ttu-id="d7724-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d7724-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d7724-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d7724-139">System.String</span></span>

## <span data-ttu-id="d7724-140">출력</span><span class="sxs-lookup"><span data-stu-id="d7724-140">OUTPUTS</span></span>

### <span data-ttu-id="d7724-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7724-141">System.Boolean</span></span>

## <span data-ttu-id="d7724-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7724-142">NOTES</span></span>

## <span data-ttu-id="d7724-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7724-143">RELATED LINKS</span></span>