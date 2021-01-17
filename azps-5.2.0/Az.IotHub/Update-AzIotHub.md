---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: fce61fd015271c9f6b5a3752fae33eaa80d6447c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361733"
---
# <span data-ttu-id="d9b84-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="d9b84-101">Update-AzIotHub</span></span>

## <span data-ttu-id="d9b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b84-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b84-103">Azure IoT Hub를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="d9b84-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9b84-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b84-105">설명</span><span class="sxs-lookup"><span data-stu-id="d9b84-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b84-106">IotHub의 태그 속성을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="d9b84-107">예제</span><span class="sxs-lookup"><span data-stu-id="d9b84-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b84-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9b84-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="d9b84-109">IoT Hub의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="d9b84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9b84-110">PARAMETERS</span></span>

### <span data-ttu-id="d9b84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b84-111">-DefaultProfile</span></span>
<span data-ttu-id="d9b84-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9b84-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d9b84-113">-Name</span></span>
<span data-ttu-id="d9b84-114">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="d9b84-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b84-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="d9b84-115">-Reset</span></span>
<span data-ttu-id="d9b84-116">IoTHub 태그 다시 설정</span><span class="sxs-lookup"><span data-stu-id="d9b84-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="d9b84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b84-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9b84-118">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d9b84-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b84-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9b84-119">-Tag</span></span>
<span data-ttu-id="d9b84-120">IoTHub 태그 컬렉션</span><span class="sxs-lookup"><span data-stu-id="d9b84-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b84-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9b84-121">-Confirm</span></span>
<span data-ttu-id="d9b84-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b84-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b84-123">-WhatIf</span></span>
<span data-ttu-id="d9b84-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9b84-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9b84-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b84-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b84-126">CommonParameters</span></span>
<span data-ttu-id="d9b84-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9b84-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b84-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d9b84-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b84-129">입력</span><span class="sxs-lookup"><span data-stu-id="d9b84-129">INPUTS</span></span>

### <span data-ttu-id="d9b84-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d9b84-130">System.String</span></span>

## <span data-ttu-id="d9b84-131">출력</span><span class="sxs-lookup"><span data-stu-id="d9b84-131">OUTPUTS</span></span>

### <span data-ttu-id="d9b84-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9b84-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="d9b84-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9b84-133">NOTES</span></span>

## <span data-ttu-id="d9b84-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9b84-134">RELATED LINKS</span></span>