---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322160"
---
# <span data-ttu-id="c9080-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="c9080-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="c9080-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9080-102">SYNOPSIS</span></span>
<span data-ttu-id="c9080-103">GEO DR 장애 조치(failover)를 호출하고 보조 네임스페이스를 지점으로 별칭을 다시 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c9080-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9080-104">SYNTAX</span></span>

### <span data-ttu-id="c9080-105">GeoDRParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9080-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9080-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c9080-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9080-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9080-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9080-108">설명</span><span class="sxs-lookup"><span data-stu-id="c9080-108">DESCRIPTION</span></span>
<span data-ttu-id="c9080-109">**Set-AzEventHubGeoDRConfigurationFailOver** cmdlet은 GEO DR 장애 조치(failover)를 호출하고 보조 네임스페이스를 지점으로 별칭을 다시 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c9080-110">예제</span><span class="sxs-lookup"><span data-stu-id="c9080-110">EXAMPLES</span></span>

### <span data-ttu-id="c9080-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9080-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="c9080-112">별칭 "SampleDRConfigName"을 통해 장애 조치(Failover)를 호출하고, 다시 구성하고, 보조 네임스페이스 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="c9080-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="c9080-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9080-113">PARAMETERS</span></span>

### <span data-ttu-id="c9080-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9080-114">-DefaultProfile</span></span>
<span data-ttu-id="c9080-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9080-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9080-116">-InputObject</span></span>
<span data-ttu-id="c9080-117">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="c9080-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9080-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c9080-118">-Name</span></span>
<span data-ttu-id="c9080-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="c9080-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9080-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c9080-120">-Namespace</span></span>
<span data-ttu-id="c9080-121">네임스페이스 이름 - 보조 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="c9080-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9080-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9080-122">-PassThru</span></span>
<span data-ttu-id="c9080-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9080-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c9080-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9080-125">-ResourceGroupName</span></span>
<span data-ttu-id="c9080-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c9080-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9080-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9080-127">-ResourceId</span></span>
<span data-ttu-id="c9080-128">GeoDRConfiguration 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c9080-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9080-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9080-129">-Confirm</span></span>
<span data-ttu-id="c9080-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9080-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9080-131">-WhatIf</span></span>
<span data-ttu-id="c9080-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c9080-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9080-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9080-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9080-134">CommonParameters</span></span>
<span data-ttu-id="c9080-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9080-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9080-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9080-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9080-137">입력</span><span class="sxs-lookup"><span data-stu-id="c9080-137">INPUTS</span></span>

### <span data-ttu-id="c9080-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c9080-138">System.String</span></span>

### <span data-ttu-id="c9080-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c9080-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c9080-140">출력</span><span class="sxs-lookup"><span data-stu-id="c9080-140">OUTPUTS</span></span>

### <span data-ttu-id="c9080-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c9080-141">System.Boolean</span></span>

## <span data-ttu-id="c9080-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9080-142">NOTES</span></span>

## <span data-ttu-id="c9080-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9080-143">RELATED LINKS</span></span>