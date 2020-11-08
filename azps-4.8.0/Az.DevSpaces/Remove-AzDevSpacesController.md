---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215000"
---
# <span data-ttu-id="d1b44-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="d1b44-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="d1b44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1b44-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b44-103">DevSpaces 컨트롤러를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="d1b44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1b44-104">SYNTAX</span></span>

### <span data-ttu-id="d1b44-105">DevSpacesControllerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1b44-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1b44-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1b44-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1b44-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1b44-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1b44-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d1b44-108">DESCRIPTION</span></span>
<span data-ttu-id="d1b44-109">DevSpaces 컨트롤러를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="d1b44-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d1b44-110">EXAMPLES</span></span>

### <span data-ttu-id="d1b44-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1b44-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="d1b44-112">DevSpaceControllerName 라는 DevSpaces 컨트롤러를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="d1b44-113">변수</span><span class="sxs-lookup"><span data-stu-id="d1b44-113">PARAMETERS</span></span>

### <span data-ttu-id="d1b44-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1b44-114">-AsJob</span></span>
<span data-ttu-id="d1b44-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d1b44-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1b44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b44-116">-DefaultProfile</span></span>
<span data-ttu-id="d1b44-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1b44-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1b44-118">-InputObject</span></span>
<span data-ttu-id="d1b44-119">일반적으로 파이프라인을 통해 전달 되는 PSController 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b44-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d1b44-120">-Name</span></span>
<span data-ttu-id="d1b44-121">DevSpaces 컨트롤러 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b44-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1b44-122">-PassThru</span></span>
<span data-ttu-id="d1b44-123">삭제가 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="d1b44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b44-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1b44-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d1b44-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b44-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1b44-126">-ResourceId</span></span>
<span data-ttu-id="d1b44-127">DevSpaces 리소스 id</span><span class="sxs-lookup"><span data-stu-id="d1b44-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b44-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d1b44-128">-Confirm</span></span>
<span data-ttu-id="d1b44-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b44-130">-WhatIf</span></span>
<span data-ttu-id="d1b44-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1b44-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b44-133">CommonParameters</span></span>
<span data-ttu-id="d1b44-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1b44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b44-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b44-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b44-136">입력</span><span class="sxs-lookup"><span data-stu-id="d1b44-136">INPUTS</span></span>

### <span data-ttu-id="d1b44-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1b44-137">System.String</span></span>

### <span data-ttu-id="d1b44-138">Microsoft. Vspaces. 모델. PSController</span><span class="sxs-lookup"><span data-stu-id="d1b44-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="d1b44-139">출력</span><span class="sxs-lookup"><span data-stu-id="d1b44-139">OUTPUTS</span></span>

### <span data-ttu-id="d1b44-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d1b44-140">System.Boolean</span></span>

## <span data-ttu-id="d1b44-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d1b44-141">NOTES</span></span>

## <span data-ttu-id="d1b44-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1b44-142">RELATED LINKS</span></span>