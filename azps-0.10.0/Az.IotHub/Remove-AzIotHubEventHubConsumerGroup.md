---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875865"
---
# <span data-ttu-id="694ca-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="694ca-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="694ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="694ca-102">SYNOPSIS</span></span>
<span data-ttu-id="694ca-103">Eventhub consumergroup를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="694ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="694ca-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="694ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="694ca-105">DESCRIPTION</span></span>
<span data-ttu-id="694ca-106">Eventhub consumergroup를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="694ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="694ca-107">EXAMPLES</span></span>

### <span data-ttu-id="694ca-108">예제 1 원격 분석 eventhub에서 eventhub consumergroup 제거</span><span class="sxs-lookup"><span data-stu-id="694ca-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="694ca-109">"Myiothub" IotHub에서 이름이 myconsumergroup 인 consumergroup을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="694ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="694ca-110">PARAMETERS</span></span>

### <span data-ttu-id="694ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694ca-111">-DefaultProfile</span></span>
<span data-ttu-id="694ca-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="694ca-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="694ca-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="694ca-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="694ca-114">EventHub ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="694ca-115">-이름</span><span class="sxs-lookup"><span data-stu-id="694ca-115">-Name</span></span>
<span data-ttu-id="694ca-116">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-116">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="694ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="694ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="694ca-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="694ca-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="694ca-119">-확인</span><span class="sxs-lookup"><span data-stu-id="694ca-119">-Confirm</span></span>
<span data-ttu-id="694ca-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694ca-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694ca-121">-WhatIf</span></span>
<span data-ttu-id="694ca-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="694ca-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694ca-124">CommonParameters</span></span>
<span data-ttu-id="694ca-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="694ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694ca-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694ca-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694ca-127">입력</span><span class="sxs-lookup"><span data-stu-id="694ca-127">INPUTS</span></span>

### <span data-ttu-id="694ca-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="694ca-128">System.String</span></span>

## <span data-ttu-id="694ca-129">출력</span><span class="sxs-lookup"><span data-stu-id="694ca-129">OUTPUTS</span></span>

### <span data-ttu-id="694ca-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="694ca-130">System.String</span></span>

## <span data-ttu-id="694ca-131">상속자</span><span class="sxs-lookup"><span data-stu-id="694ca-131">NOTES</span></span>

## <span data-ttu-id="694ca-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="694ca-132">RELATED LINKS</span></span>