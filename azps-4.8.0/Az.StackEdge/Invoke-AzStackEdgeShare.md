---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213831"
---
# <span data-ttu-id="c0a8f-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="c0a8f-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="c0a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a8f-103">공유에 대 한 특정 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="c0a8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0a8f-104">SYNTAX</span></span>

### <span data-ttu-id="c0a8f-105">InvokeByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0a8f-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0a8f-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0a8f-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0a8f-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0a8f-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0a8f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c0a8f-108">DESCRIPTION</span></span>
<span data-ttu-id="c0a8f-109">**AzStackEdgeShare** Cmdlet은 스택 가장자리 장치에서 공유에 있는 데이터를 새로 고치기 위한 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="c0a8f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c0a8f-110">EXAMPLES</span></span>

### <span data-ttu-id="c0a8f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0a8f-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="c0a8f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="c0a8f-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="c0a8f-113">변수</span><span class="sxs-lookup"><span data-stu-id="c0a8f-113">PARAMETERS</span></span>

### <span data-ttu-id="c0a8f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0a8f-114">-AsJob</span></span>
<span data-ttu-id="c0a8f-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c0a8f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0a8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a8f-116">-DefaultProfile</span></span>
<span data-ttu-id="c0a8f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0a8f-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="c0a8f-118">-DeviceName</span></span>
<span data-ttu-id="c0a8f-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="c0a8f-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a8f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0a8f-120">-InputObject</span></span>
<span data-ttu-id="c0a8f-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="c0a8f-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a8f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c0a8f-122">-Name</span></span>
<span data-ttu-id="c0a8f-123">자원 이름</span><span class="sxs-lookup"><span data-stu-id="c0a8f-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a8f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0a8f-124">-PassThru</span></span>
<span data-ttu-id="c0a8f-125">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-125">returns true if successful</span></span>

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

### <span data-ttu-id="c0a8f-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="c0a8f-126">-RefreshData</span></span>
<span data-ttu-id="c0a8f-127">클라우드의 데이터와 공유 메타 데이터를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="c0a8f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a8f-128">-ResourceGroupName</span></span>
<span data-ttu-id="c0a8f-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c0a8f-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a8f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0a8f-130">-ResourceId</span></span>
<span data-ttu-id="c0a8f-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0a8f-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a8f-132">-확인</span><span class="sxs-lookup"><span data-stu-id="c0a8f-132">-Confirm</span></span>
<span data-ttu-id="c0a8f-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0a8f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a8f-134">-WhatIf</span></span>
<span data-ttu-id="c0a8f-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0a8f-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0a8f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a8f-137">CommonParameters</span></span>
<span data-ttu-id="c0a8f-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a8f-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0a8f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a8f-140">입력</span><span class="sxs-lookup"><span data-stu-id="c0a8f-140">INPUTS</span></span>

### <span data-ttu-id="c0a8f-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0a8f-141">System.String</span></span>

### <span data-ttu-id="c0a8f-142">StackEdge. PSStackEdgeShare에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0a8f-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="c0a8f-143">출력</span><span class="sxs-lookup"><span data-stu-id="c0a8f-143">OUTPUTS</span></span>

### <span data-ttu-id="c0a8f-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c0a8f-144">System.Boolean</span></span>

## <span data-ttu-id="c0a8f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c0a8f-145">NOTES</span></span>

## <span data-ttu-id="c0a8f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0a8f-146">RELATED LINKS</span></span>