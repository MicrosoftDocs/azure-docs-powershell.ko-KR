---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: c67793371b6842e4aa8190055580b0cdfefd3e08
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875917"
---
# <span data-ttu-id="8a16a-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="8a16a-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="8a16a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a16a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a16a-103">지정 된 이벤트 허브를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="8a16a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a16a-104">SYNTAX</span></span>

### <span data-ttu-id="8a16a-105">EventhubDefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a16a-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a16a-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a16a-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a16a-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a16a-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a16a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8a16a-108">DESCRIPTION</span></span>
<span data-ttu-id="8a16a-109">Remove-AzEventHub cmdlet은 주어진 네임 스페이스에서 지정 된 이벤트 허브를 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="8a16a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8a16a-110">EXAMPLES</span></span>

### <span data-ttu-id="8a16a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a16a-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="8a16a-112">이벤트 허브 MyEventHubName를 \` 제거 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="8a16a-113">예제 2.1-InputObject-Using 변수:</span><span class="sxs-lookup"><span data-stu-id="8a16a-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="8a16a-114">예제 2.2-파이핑을 사용한 InputObject:</span><span class="sxs-lookup"><span data-stu-id="8a16a-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="8a16a-115">예제 3.1-ResourceId-변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="8a16a-116">예제 3.1-ResourceId-문자열을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="8a16a-117">변수</span><span class="sxs-lookup"><span data-stu-id="8a16a-117">PARAMETERS</span></span>

### <span data-ttu-id="8a16a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a16a-118">-AsJob</span></span>
<span data-ttu-id="8a16a-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8a16a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a16a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a16a-120">-DefaultProfile</span></span>
<span data-ttu-id="8a16a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a16a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a16a-122">-InputObject</span></span>
<span data-ttu-id="8a16a-123">Eventhub 개체</span><span class="sxs-lookup"><span data-stu-id="8a16a-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a16a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8a16a-124">-Name</span></span>
<span data-ttu-id="8a16a-125">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="8a16a-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a16a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8a16a-126">-Namespace</span></span>
<span data-ttu-id="8a16a-127">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="8a16a-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a16a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a16a-128">-PassThru</span></span>
<span data-ttu-id="8a16a-129">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8a16a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a16a-130">-ResourceGroupName</span></span>
<span data-ttu-id="8a16a-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8a16a-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a16a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a16a-132">-ResourceId</span></span>
<span data-ttu-id="8a16a-133">Eventhub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="8a16a-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a16a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="8a16a-134">-Confirm</span></span>
<span data-ttu-id="8a16a-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a16a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a16a-136">-WhatIf</span></span>
<span data-ttu-id="8a16a-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a16a-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a16a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a16a-139">CommonParameters</span></span>
<span data-ttu-id="8a16a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a16a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a16a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a16a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a16a-142">입력</span><span class="sxs-lookup"><span data-stu-id="8a16a-142">INPUTS</span></span>

### <span data-ttu-id="8a16a-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a16a-143">System.String</span></span>

### <span data-ttu-id="8a16a-144">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="8a16a-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="8a16a-145">출력</span><span class="sxs-lookup"><span data-stu-id="8a16a-145">OUTPUTS</span></span>

### <span data-ttu-id="8a16a-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8a16a-146">System.Boolean</span></span>

## <span data-ttu-id="8a16a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8a16a-147">NOTES</span></span>

## <span data-ttu-id="8a16a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a16a-148">RELATED LINKS</span></span>