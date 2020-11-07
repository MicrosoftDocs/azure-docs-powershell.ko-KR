---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 689588e8b92b4b76c97f3972aa63c2f8cdc16535
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875722"
---
# <span data-ttu-id="60020-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="60020-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="60020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60020-102">SYNOPSIS</span></span>
<span data-ttu-id="60020-103">로그 알림 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="60020-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="60020-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60020-104">SYNTAX</span></span>

### <span data-ttu-id="60020-105">ByRuleName (기본값)</span><span class="sxs-lookup"><span data-stu-id="60020-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60020-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60020-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60020-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="60020-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60020-108">설명은</span><span class="sxs-lookup"><span data-stu-id="60020-108">DESCRIPTION</span></span>
<span data-ttu-id="60020-109">로그 알림 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="60020-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="60020-110">예제의</span><span class="sxs-lookup"><span data-stu-id="60020-110">EXAMPLES</span></span>

### <span data-ttu-id="60020-111">예제 1-규칙 이름으로 제거</span><span class="sxs-lookup"><span data-stu-id="60020-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="60020-112">예제 2-입력 개체에서 제거</span><span class="sxs-lookup"><span data-stu-id="60020-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="60020-113">예제 3-리소스 Id 별 제거</span><span class="sxs-lookup"><span data-stu-id="60020-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="60020-114">변수</span><span class="sxs-lookup"><span data-stu-id="60020-114">PARAMETERS</span></span>

### <span data-ttu-id="60020-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60020-115">-DefaultProfile</span></span>
<span data-ttu-id="60020-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60020-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60020-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60020-117">-InputObject</span></span>
<span data-ttu-id="60020-118">예약 된 쿼리 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="60020-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60020-119">-이름</span><span class="sxs-lookup"><span data-stu-id="60020-119">-Name</span></span>
<span data-ttu-id="60020-120">알림 이름</span><span class="sxs-lookup"><span data-stu-id="60020-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60020-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60020-121">-PassThru</span></span>
<span data-ttu-id="60020-122">성공 또는 실패를 나타내는 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="60020-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="60020-123">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60020-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60020-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60020-124">-ResourceGroupName</span></span>
<span data-ttu-id="60020-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="60020-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60020-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60020-126">-ResourceId</span></span>
<span data-ttu-id="60020-127">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="60020-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60020-128">-확인</span><span class="sxs-lookup"><span data-stu-id="60020-128">-Confirm</span></span>
<span data-ttu-id="60020-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60020-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60020-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60020-130">-WhatIf</span></span>
<span data-ttu-id="60020-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60020-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60020-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60020-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60020-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60020-133">CommonParameters</span></span>
<span data-ttu-id="60020-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60020-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60020-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60020-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60020-136">입력</span><span class="sxs-lookup"><span data-stu-id="60020-136">INPUTS</span></span>

### <span data-ttu-id="60020-137">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="60020-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="60020-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60020-138">System.String</span></span>

## <span data-ttu-id="60020-139">출력</span><span class="sxs-lookup"><span data-stu-id="60020-139">OUTPUTS</span></span>

### <span data-ttu-id="60020-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="60020-140">System.Boolean</span></span>

## <span data-ttu-id="60020-141">상속자</span><span class="sxs-lookup"><span data-stu-id="60020-141">NOTES</span></span>

## <span data-ttu-id="60020-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60020-142">RELATED LINKS</span></span>