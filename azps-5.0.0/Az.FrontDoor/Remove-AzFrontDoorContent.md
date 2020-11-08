---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorContent.md
ms.openlocfilehash: b7b01ec1b301741c07a0667931a63287cc503434
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215444"
---
# <span data-ttu-id="26275-101">Remove-AzFrontDoorContent</span><span class="sxs-lookup"><span data-stu-id="26275-101">Remove-AzFrontDoorContent</span></span>

## <span data-ttu-id="26275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26275-102">SYNOPSIS</span></span>
<span data-ttu-id="26275-103">앞면 도어 내용 제거</span><span class="sxs-lookup"><span data-stu-id="26275-103">Remove contents in Front Door</span></span>

## <span data-ttu-id="26275-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26275-104">SYNTAX</span></span>

```
Remove-AzFrontDoorContent -ResourceGroupName <String> -Name <String> -ContentPath <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26275-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26275-105">DESCRIPTION</span></span>
<span data-ttu-id="26275-106">Remove-AzFrontDoorContent를 통해 앞쪽 도어의 캐시 된 내용 제거</span><span class="sxs-lookup"><span data-stu-id="26275-106">Remove-AzFrontDoorContent purges cached contents in a Front Door</span></span>

## <span data-ttu-id="26275-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26275-107">EXAMPLES</span></span>

### <span data-ttu-id="26275-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="26275-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorContent -ResourceGroupName $ResourceGroupName -Name $FrontDoorName -ContentPath "/*"
```

## <span data-ttu-id="26275-109">변수</span><span class="sxs-lookup"><span data-stu-id="26275-109">PARAMETERS</span></span>

### <span data-ttu-id="26275-110">-ContentPath</span><span class="sxs-lookup"><span data-stu-id="26275-110">-ContentPath</span></span>
<span data-ttu-id="26275-111">지울 콘텐츠의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="26275-111">The paths to the content to be purged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26275-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26275-112">-DefaultProfile</span></span>
<span data-ttu-id="26275-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26275-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26275-114">-이름</span><span class="sxs-lookup"><span data-stu-id="26275-114">-Name</span></span>
<span data-ttu-id="26275-115">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26275-115">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26275-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26275-116">-PassThru</span></span>
<span data-ttu-id="26275-117">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26275-117">Return object (if specified).</span></span>

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

### <span data-ttu-id="26275-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26275-118">-ResourceGroupName</span></span>
<span data-ttu-id="26275-119">앞면 도어의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="26275-119">The resource group name of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26275-120">-확인</span><span class="sxs-lookup"><span data-stu-id="26275-120">-Confirm</span></span>
<span data-ttu-id="26275-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26275-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26275-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26275-122">-WhatIf</span></span>
<span data-ttu-id="26275-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26275-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26275-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26275-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26275-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26275-125">CommonParameters</span></span>
<span data-ttu-id="26275-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26275-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26275-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26275-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26275-128">입력</span><span class="sxs-lookup"><span data-stu-id="26275-128">INPUTS</span></span>

### <span data-ttu-id="26275-129">않아야</span><span class="sxs-lookup"><span data-stu-id="26275-129">None</span></span>

## <span data-ttu-id="26275-130">출력</span><span class="sxs-lookup"><span data-stu-id="26275-130">OUTPUTS</span></span>

### <span data-ttu-id="26275-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="26275-131">System.Boolean</span></span>

## <span data-ttu-id="26275-132">상속자</span><span class="sxs-lookup"><span data-stu-id="26275-132">NOTES</span></span>

## <span data-ttu-id="26275-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26275-133">RELATED LINKS</span></span>