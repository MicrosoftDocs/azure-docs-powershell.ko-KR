---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: 7fde60c0bd1f400dd332782b6fbb9a92fefae4a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034785"
---
# <span data-ttu-id="fd6bf-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="fd6bf-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="fd6bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6bf-103">SignalR 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="fd6bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd6bf-104">SYNTAX</span></span>

### <span data-ttu-id="fd6bf-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd6bf-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6bf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6bf-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6bf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6bf-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd6bf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fd6bf-108">DESCRIPTION</span></span>
<span data-ttu-id="fd6bf-109">SignalR 서비스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="fd6bf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fd6bf-110">EXAMPLES</span></span>

### <span data-ttu-id="fd6bf-111">특정 SignalR 서비스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="fd6bf-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="fd6bf-112">기본 리소스 그룹은 \` set-AzDefault-ResourceGroupName myResourceGroup을 통해 설정할 수 있습니다 \` .</span><span class="sxs-lookup"><span data-stu-id="fd6bf-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="fd6bf-113">변수</span><span class="sxs-lookup"><span data-stu-id="fd6bf-113">PARAMETERS</span></span>

### <span data-ttu-id="fd6bf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd6bf-114">-AsJob</span></span>
<span data-ttu-id="fd6bf-115">백그라운드 작업에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="fd6bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6bf-116">-DefaultProfile</span></span>
<span data-ttu-id="fd6bf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd6bf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd6bf-118">-InputObject</span></span>
<span data-ttu-id="fd6bf-119">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6bf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="fd6bf-120">-Name</span></span>
<span data-ttu-id="fd6bf-121">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-121">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6bf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd6bf-122">-PassThru</span></span>
<span data-ttu-id="fd6bf-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="fd6bf-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="fd6bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd6bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd6bf-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-125">The resource group name.</span></span>
<span data-ttu-id="fd6bf-126">지정 되지 않은 경우 기본 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-126">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6bf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd6bf-127">-ResourceId</span></span>
<span data-ttu-id="fd6bf-128">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6bf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="fd6bf-129">-Confirm</span></span>
<span data-ttu-id="fd6bf-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6bf-131">-WhatIf</span></span>
<span data-ttu-id="fd6bf-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd6bf-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6bf-134">CommonParameters</span></span>
<span data-ttu-id="fd6bf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6bf-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6bf-137">입력</span><span class="sxs-lookup"><span data-stu-id="fd6bf-137">INPUTS</span></span>

### <span data-ttu-id="fd6bf-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd6bf-138">System.String</span></span>

### <span data-ttu-id="fd6bf-139">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="fd6bf-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="fd6bf-140">출력</span><span class="sxs-lookup"><span data-stu-id="fd6bf-140">OUTPUTS</span></span>

### <span data-ttu-id="fd6bf-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fd6bf-141">System.Boolean</span></span>

## <span data-ttu-id="fd6bf-142">상속자</span><span class="sxs-lookup"><span data-stu-id="fd6bf-142">NOTES</span></span>

## <span data-ttu-id="fd6bf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd6bf-143">RELATED LINKS</span></span>