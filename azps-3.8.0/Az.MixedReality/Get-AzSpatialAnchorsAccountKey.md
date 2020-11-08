---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: c5fc1c497bc0cb6f73aab4ddcfbc1ce127cc4545
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044516"
---
# <span data-ttu-id="dd3d4-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="dd3d4-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="dd3d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3d4-103">공간 앵커 계정의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="dd3d4-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="dd3d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd3d4-104">SYNTAX</span></span>

### <span data-ttu-id="dd3d4-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dd3d4-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd3d4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd3d4-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd3d4-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd3d4-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd3d4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dd3d4-108">DESCRIPTION</span></span>
<span data-ttu-id="dd3d4-109">공간 앵커 계정의 개발자 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="dd3d4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dd3d4-110">EXAMPLES</span></span>

### <span data-ttu-id="dd3d4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dd3d4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="dd3d4-112">현재 구독 및 리소스 그룹 "rg1"의 공간 앵커 계정에 대 한 개발자 키 가져오기 "예제".</span><span class="sxs-lookup"><span data-stu-id="dd3d4-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="dd3d4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dd3d4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="dd3d4-114">현재 구독 및 리소스 그룹 "rg1"에서 공간 앵커 계정의 개발자 키를 사용 하 여 "예"를 파이프로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="dd3d4-115">변수</span><span class="sxs-lookup"><span data-stu-id="dd3d4-115">PARAMETERS</span></span>

### <span data-ttu-id="dd3d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3d4-116">-DefaultProfile</span></span>
<span data-ttu-id="dd3d4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd3d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd3d4-118">-InputObject</span></span>
<span data-ttu-id="dd3d4-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-119">The custom domain object.</span></span>

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

### <span data-ttu-id="dd3d4-120">-이름</span><span class="sxs-lookup"><span data-stu-id="dd3d4-120">-Name</span></span>
<span data-ttu-id="dd3d4-121">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="dd3d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd3d4-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd3d4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd3d4-124">-ResourceId</span></span>
<span data-ttu-id="dd3d4-125">공간 앵커 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="dd3d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3d4-126">CommonParameters</span></span>
<span data-ttu-id="dd3d4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd3d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dd3d4-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd3d4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3d4-129">입력</span><span class="sxs-lookup"><span data-stu-id="dd3d4-129">INPUTS</span></span>

### <span data-ttu-id="dd3d4-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd3d4-130">System.String</span></span>

### <span data-ttu-id="dd3d4-131">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="dd3d4-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="dd3d4-132">출력</span><span class="sxs-lookup"><span data-stu-id="dd3d4-132">OUTPUTS</span></span>

### <span data-ttu-id="dd3d4-133">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dd3d4-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="dd3d4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="dd3d4-134">NOTES</span></span>

## <span data-ttu-id="dd3d4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd3d4-135">RELATED LINKS</span></span>