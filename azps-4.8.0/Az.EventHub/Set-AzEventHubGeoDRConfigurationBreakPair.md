---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047767"
---
# <span data-ttu-id="e25eb-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="e25eb-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="e25eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e25eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e25eb-103">이 작업은 재해 복구를 사용 하지 않도록 설정 하 고 기본 네임 스페이스로 변경 내용 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="e25eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e25eb-104">SYNTAX</span></span>

### <span data-ttu-id="e25eb-105">GeoDRParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e25eb-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25eb-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e25eb-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e25eb-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e25eb-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25eb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e25eb-108">DESCRIPTION</span></span>
<span data-ttu-id="e25eb-109">**AzEventHubGeoDRConfigurationBreakPair** Cmdlet은 재해 복구를 사용 하지 않도록 설정 하 고 기본 네임 스페이스로 변경 내용 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="e25eb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e25eb-110">EXAMPLES</span></span>

### <span data-ttu-id="e25eb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e25eb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="e25eb-112">이 작업은 재해 복구를 사용 하지 않도록 설정 하 고 기본 네임 스페이스로 변경 내용 복제를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="e25eb-113">변수</span><span class="sxs-lookup"><span data-stu-id="e25eb-113">PARAMETERS</span></span>

### <span data-ttu-id="e25eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25eb-114">-DefaultProfile</span></span>
<span data-ttu-id="e25eb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e25eb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e25eb-116">-InputObject</span></span>
<span data-ttu-id="e25eb-117">Eventhub GeoDR 구성 개체</span><span class="sxs-lookup"><span data-stu-id="e25eb-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="e25eb-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e25eb-118">-Name</span></span>
<span data-ttu-id="e25eb-119">DR 구성 이름</span><span class="sxs-lookup"><span data-stu-id="e25eb-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="e25eb-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e25eb-120">-Namespace</span></span>
<span data-ttu-id="e25eb-121">네임 스페이스 이름-기본 네임 스페이스</span><span class="sxs-lookup"><span data-stu-id="e25eb-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="e25eb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e25eb-122">-PassThru</span></span>
<span data-ttu-id="e25eb-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e25eb-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e25eb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25eb-125">-ResourceGroupName</span></span>
<span data-ttu-id="e25eb-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e25eb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e25eb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e25eb-127">-ResourceId</span></span>
<span data-ttu-id="e25eb-128">GeoDRConfiguration 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="e25eb-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="e25eb-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e25eb-129">-Confirm</span></span>
<span data-ttu-id="e25eb-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25eb-131">-WhatIf</span></span>
<span data-ttu-id="e25eb-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25eb-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25eb-134">CommonParameters</span></span>
<span data-ttu-id="e25eb-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e25eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25eb-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25eb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25eb-137">입력</span><span class="sxs-lookup"><span data-stu-id="e25eb-137">INPUTS</span></span>

### <span data-ttu-id="e25eb-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e25eb-138">System.String</span></span>

### <span data-ttu-id="e25eb-139">PSEventHubDRConfigurationAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="e25eb-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="e25eb-140">출력</span><span class="sxs-lookup"><span data-stu-id="e25eb-140">OUTPUTS</span></span>

### <span data-ttu-id="e25eb-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e25eb-141">System.Boolean</span></span>

## <span data-ttu-id="e25eb-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e25eb-142">NOTES</span></span>

## <span data-ttu-id="e25eb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e25eb-143">RELATED LINKS</span></span>