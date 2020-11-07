---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868129"
---
# <span data-ttu-id="78c05-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="78c05-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="78c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c05-102">SYNOPSIS</span></span>
<span data-ttu-id="78c05-103">모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="78c05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78c05-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c05-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78c05-105">DESCRIPTION</span></span>
<span data-ttu-id="78c05-106">IotHub에서 사용 하는 다른 EventHubs에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="78c05-107">예제의</span><span class="sxs-lookup"><span data-stu-id="78c05-107">EXAMPLES</span></span>

### <span data-ttu-id="78c05-108">예제 1 원격 분석 eventhub에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="78c05-109">Myiothub iothub에 대 한 원격 분석 eventhub의 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="78c05-110">예제 2 operationsmonitoring eventhub에 대 한 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="78c05-111">Myiothub iothub에 대 한 operationsMonitoringEvents eventhub의 모든 eventhub consumergroups를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="78c05-112">변수</span><span class="sxs-lookup"><span data-stu-id="78c05-112">PARAMETERS</span></span>

### <span data-ttu-id="78c05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c05-113">-DefaultProfile</span></span>
<span data-ttu-id="78c05-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78c05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78c05-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="78c05-115">-EventHubEndpointName</span></span>
<span data-ttu-id="78c05-116">이벤트 허브 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="78c05-117">사용할 수 있는 값 이벤트, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="78c05-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c05-118">-이름</span><span class="sxs-lookup"><span data-stu-id="78c05-118">-Name</span></span>
<span data-ttu-id="78c05-119">IotHub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="78c05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c05-120">-ResourceGroupName</span></span>
<span data-ttu-id="78c05-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="78c05-121">Resource Group Name</span></span>

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

### <span data-ttu-id="78c05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c05-122">CommonParameters</span></span>
<span data-ttu-id="78c05-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78c05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c05-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c05-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c05-125">입력</span><span class="sxs-lookup"><span data-stu-id="78c05-125">INPUTS</span></span>

### <span data-ttu-id="78c05-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78c05-126">System.String</span></span>

## <span data-ttu-id="78c05-127">출력</span><span class="sxs-lookup"><span data-stu-id="78c05-127">OUTPUTS</span></span>

### <span data-ttu-id="78c05-128">IotHub. PSEventHubConsumerGroupInfo/. \*</span><span class="sxs-lookup"><span data-stu-id="78c05-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="78c05-129">상속자</span><span class="sxs-lookup"><span data-stu-id="78c05-129">NOTES</span></span>

## <span data-ttu-id="78c05-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78c05-130">RELATED LINKS</span></span>