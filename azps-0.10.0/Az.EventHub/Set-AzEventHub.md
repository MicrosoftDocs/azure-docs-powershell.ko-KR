---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: 2b1f3c0cd30b9f0ebc67a0b11f5b42a35b7e3394
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875897"
---
# <span data-ttu-id="504b2-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="504b2-101">Set-AzEventHub</span></span>

## <span data-ttu-id="504b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504b2-102">SYNOPSIS</span></span>
<span data-ttu-id="504b2-103">지정 된 이벤트 허브를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="504b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="504b2-104">SYNTAX</span></span>

### <span data-ttu-id="504b2-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="504b2-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="504b2-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="504b2-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="504b2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="504b2-107">DESCRIPTION</span></span>
<span data-ttu-id="504b2-108">Set-AzEventHub cmdlet은 지정 된 이벤트 허브의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="504b2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="504b2-109">EXAMPLES</span></span>

### <span data-ttu-id="504b2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="504b2-110">Example 1</span></span>
<span data-ttu-id="504b2-111">캡처 설명 속성을 사용 하 여 Eventhub를 업데이트 하려면 아래 단계를 수행 하세요.</span><span class="sxs-lookup"><span data-stu-id="504b2-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="504b2-112">\` \` MyCreatedEventHub 개체가 나타내는 이벤트 허브 MyEventHubName를 업데이트 \` 하 고 \` , 메시지 보존 기간을 4 일로 설정 하 고, 파티션 수를 2로, CaptureDescription 속성을</span><span class="sxs-lookup"><span data-stu-id="504b2-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="504b2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="504b2-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="504b2-114">MyCreatedEventHub 개체로 표시 되는 이벤트 허브 \` MyEventHubName \` 를 업데이트 하 고 \` \` , 메시지 보존 기간을 4 일로, 파티션 수를 2로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="504b2-115">변수</span><span class="sxs-lookup"><span data-stu-id="504b2-115">PARAMETERS</span></span>

### <span data-ttu-id="504b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504b2-116">-DefaultProfile</span></span>
<span data-ttu-id="504b2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="504b2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="504b2-118">-InputObject</span></span>
<span data-ttu-id="504b2-119">EventHub 개체</span><span class="sxs-lookup"><span data-stu-id="504b2-119">EventHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504b2-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="504b2-120">-messageRetentionInDays</span></span>
<span data-ttu-id="504b2-121">Eventhub 메시지 보존 기간 (일)</span><span class="sxs-lookup"><span data-stu-id="504b2-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504b2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="504b2-122">-Name</span></span>
<span data-ttu-id="504b2-123">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="504b2-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504b2-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="504b2-124">-Namespace</span></span>
<span data-ttu-id="504b2-125">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="504b2-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504b2-126">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="504b2-126">-partitionCount</span></span>
<span data-ttu-id="504b2-127">Eventhub/Count</span><span class="sxs-lookup"><span data-stu-id="504b2-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504b2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504b2-128">-ResourceGroupName</span></span>
<span data-ttu-id="504b2-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="504b2-129">Resource Group Name</span></span>

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

### <span data-ttu-id="504b2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="504b2-130">-Confirm</span></span>
<span data-ttu-id="504b2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="504b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="504b2-132">-WhatIf</span></span>
<span data-ttu-id="504b2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="504b2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="504b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504b2-135">CommonParameters</span></span>
<span data-ttu-id="504b2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="504b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504b2-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="504b2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504b2-138">입력</span><span class="sxs-lookup"><span data-stu-id="504b2-138">INPUTS</span></span>

### <span data-ttu-id="504b2-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="504b2-139">System.String</span></span>

### <span data-ttu-id="504b2-140">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="504b2-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="504b2-141">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="504b2-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="504b2-142">출력</span><span class="sxs-lookup"><span data-stu-id="504b2-142">OUTPUTS</span></span>

### <span data-ttu-id="504b2-143">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="504b2-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="504b2-144">상속자</span><span class="sxs-lookup"><span data-stu-id="504b2-144">NOTES</span></span>

## <span data-ttu-id="504b2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="504b2-145">RELATED LINKS</span></span>