---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: 37e641516ffc21a0984f97cb84f94d2564033fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873435"
---
# <span data-ttu-id="24b90-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="24b90-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="24b90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b90-102">SYNOPSIS</span></span>
<span data-ttu-id="24b90-103">새 릴레이 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="24b90-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24b90-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b90-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24b90-105">DESCRIPTION</span></span>
<span data-ttu-id="24b90-106">새 릴레이 네임 스페이스를 만드는 **AzRelayNamespace** cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24b90-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="24b90-107">네임 스페이스 리소스 매니페스트를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="24b90-108">예제의</span><span class="sxs-lookup"><span data-stu-id="24b90-108">EXAMPLES</span></span>

### <span data-ttu-id="24b90-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="24b90-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="24b90-110">지정 된 리소스 그룹 내에 새 릴레이 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="24b90-111">변수</span><span class="sxs-lookup"><span data-stu-id="24b90-111">PARAMETERS</span></span>

### <span data-ttu-id="24b90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b90-112">-DefaultProfile</span></span>
<span data-ttu-id="24b90-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b90-114">-위치</span><span class="sxs-lookup"><span data-stu-id="24b90-114">-Location</span></span>
<span data-ttu-id="24b90-115">릴레이 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="24b90-116">-이름</span><span class="sxs-lookup"><span data-stu-id="24b90-116">-Name</span></span>
<span data-ttu-id="24b90-117">릴레이 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="24b90-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b90-118">-ResourceGroupName</span></span>
<span data-ttu-id="24b90-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="24b90-120">태그</span><span class="sxs-lookup"><span data-stu-id="24b90-120">-Tag</span></span>
<span data-ttu-id="24b90-121">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="24b90-121">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b90-122">-확인</span><span class="sxs-lookup"><span data-stu-id="24b90-122">-Confirm</span></span>
<span data-ttu-id="24b90-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b90-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b90-124">-WhatIf</span></span>
<span data-ttu-id="24b90-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b90-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24b90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b90-127">CommonParameters</span></span>
<span data-ttu-id="24b90-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b90-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b90-130">입력</span><span class="sxs-lookup"><span data-stu-id="24b90-130">INPUTS</span></span>

### <span data-ttu-id="24b90-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24b90-131">System.String</span></span>

### <span data-ttu-id="24b90-132">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="24b90-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24b90-133">출력</span><span class="sxs-lookup"><span data-stu-id="24b90-133">OUTPUTS</span></span>

### <span data-ttu-id="24b90-134">PSRelayNamespaceAttributes에 대 한 자세한</span><span class="sxs-lookup"><span data-stu-id="24b90-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="24b90-135">상속자</span><span class="sxs-lookup"><span data-stu-id="24b90-135">NOTES</span></span>

## <span data-ttu-id="24b90-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24b90-136">RELATED LINKS</span></span>