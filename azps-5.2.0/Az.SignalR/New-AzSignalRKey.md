---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330482"
---
# <span data-ttu-id="611fe-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="611fe-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="611fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611fe-102">SYNOPSIS</span></span>
<span data-ttu-id="611fe-103">SignalR 서비스에 대한 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="611fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="611fe-104">SYNTAX</span></span>

### <span data-ttu-id="611fe-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="611fe-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="611fe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="611fe-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="611fe-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="611fe-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="611fe-108">설명</span><span class="sxs-lookup"><span data-stu-id="611fe-108">DESCRIPTION</span></span>
<span data-ttu-id="611fe-109">SignalR 서비스에 대한 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="611fe-110">예제</span><span class="sxs-lookup"><span data-stu-id="611fe-110">EXAMPLES</span></span>

### <span data-ttu-id="611fe-111">기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="611fe-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="611fe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="611fe-112">PARAMETERS</span></span>

### <span data-ttu-id="611fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611fe-113">-DefaultProfile</span></span>
<span data-ttu-id="611fe-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="611fe-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="611fe-115">-InputObject</span></span>
<span data-ttu-id="611fe-116">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="611fe-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="611fe-117">-KeyType</span></span>
<span data-ttu-id="611fe-118">기본 또는 보조 키 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611fe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="611fe-119">-Name</span></span>
<span data-ttu-id="611fe-120">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-120">SignalR service name.</span></span>

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

### <span data-ttu-id="611fe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="611fe-121">-PassThru</span></span>
<span data-ttu-id="611fe-122">다시 재생성이 성공적으로 완료되면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="611fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="611fe-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-124">Resource group name.</span></span>

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

### <span data-ttu-id="611fe-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="611fe-125">-ResourceId</span></span>
<span data-ttu-id="611fe-126">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="611fe-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="611fe-127">-Confirm</span></span>
<span data-ttu-id="611fe-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="611fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="611fe-129">-WhatIf</span></span>
<span data-ttu-id="611fe-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="611fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="611fe-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="611fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611fe-132">CommonParameters</span></span>
<span data-ttu-id="611fe-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="611fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611fe-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="611fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611fe-135">입력</span><span class="sxs-lookup"><span data-stu-id="611fe-135">INPUTS</span></span>

### <span data-ttu-id="611fe-136">System.String</span><span class="sxs-lookup"><span data-stu-id="611fe-136">System.String</span></span>
### <span data-ttu-id="611fe-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="611fe-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="611fe-138">출력</span><span class="sxs-lookup"><span data-stu-id="611fe-138">OUTPUTS</span></span>

### <span data-ttu-id="611fe-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="611fe-139">System.Boolean</span></span>
## <span data-ttu-id="611fe-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="611fe-140">NOTES</span></span>

## <span data-ttu-id="611fe-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="611fe-141">RELATED LINKS</span></span>