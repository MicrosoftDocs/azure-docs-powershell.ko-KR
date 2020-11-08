---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049004"
---
# <span data-ttu-id="d3ebf-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d3ebf-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d3ebf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ebf-103">공간 앵커 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="d3ebf-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="d3ebf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3ebf-104">SYNTAX</span></span>

### <span data-ttu-id="d3ebf-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3ebf-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3ebf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3ebf-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3ebf-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3ebf-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3ebf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d3ebf-108">DESCRIPTION</span></span>
<span data-ttu-id="d3ebf-109">특정 구독 및 리소스 그룹에서 지정 된 공간 앵커 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="d3ebf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d3ebf-110">EXAMPLES</span></span>

### <span data-ttu-id="d3ebf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3ebf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="d3ebf-112">현재 구독 및 리소스 그룹 "rg1"에서 공간 앵커 계정 "예제"를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="d3ebf-113">변수</span><span class="sxs-lookup"><span data-stu-id="d3ebf-113">PARAMETERS</span></span>

### <span data-ttu-id="d3ebf-114">-확인</span><span class="sxs-lookup"><span data-stu-id="d3ebf-114">-Confirm</span></span>
<span data-ttu-id="d3ebf-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ebf-116">-DefaultProfile</span></span>
<span data-ttu-id="d3ebf-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3ebf-118">-InputObject</span></span>
<span data-ttu-id="d3ebf-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d3ebf-120">-Name</span></span>
<span data-ttu-id="d3ebf-121">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3ebf-122">-PassThru</span></span>
<span data-ttu-id="d3ebf-123">지정 된 경우 object 반환</span><span class="sxs-lookup"><span data-stu-id="d3ebf-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3ebf-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3ebf-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3ebf-126">-ResourceId</span></span>
<span data-ttu-id="d3ebf-127">공간 앵커 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ebf-128">-WhatIf</span></span>
<span data-ttu-id="d3ebf-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3ebf-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ebf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ebf-131">CommonParameters</span></span>
<span data-ttu-id="d3ebf-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ebf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d3ebf-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ebf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ebf-134">입력</span><span class="sxs-lookup"><span data-stu-id="d3ebf-134">INPUTS</span></span>

### <span data-ttu-id="d3ebf-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3ebf-135">System.String</span></span>

### <span data-ttu-id="d3ebf-136">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d3ebf-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="d3ebf-137">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3ebf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3ebf-138">출력</span><span class="sxs-lookup"><span data-stu-id="d3ebf-138">OUTPUTS</span></span>

### <span data-ttu-id="d3ebf-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d3ebf-139">System.Boolean</span></span>

## <span data-ttu-id="d3ebf-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d3ebf-140">NOTES</span></span>

## <span data-ttu-id="d3ebf-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3ebf-141">RELATED LINKS</span></span>