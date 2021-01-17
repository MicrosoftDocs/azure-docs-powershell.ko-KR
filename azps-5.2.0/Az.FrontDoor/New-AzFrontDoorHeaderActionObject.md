---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326409"
---
# <span data-ttu-id="074e3-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="074e3-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="074e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="074e3-102">SYNOPSIS</span></span>
<span data-ttu-id="074e3-103">PSHeaderAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="074e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="074e3-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="074e3-105">설명</span><span class="sxs-lookup"><span data-stu-id="074e3-105">DESCRIPTION</span></span>
<span data-ttu-id="074e3-106">PSRulesEngineAction 개체를 만들기 위한 PSHeaderAction 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="074e3-107">예제</span><span class="sxs-lookup"><span data-stu-id="074e3-107">EXAMPLES</span></span>

### <span data-ttu-id="074e3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="074e3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="074e3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="074e3-109">PARAMETERS</span></span>

### <span data-ttu-id="074e3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="074e3-110">-DefaultProfile</span></span>
<span data-ttu-id="074e3-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="074e3-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="074e3-112">-HeaderActionType</span></span>
<span data-ttu-id="074e3-113">헤더에 적용할 조작 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074e3-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="074e3-114">-HeaderName</span></span>
<span data-ttu-id="074e3-115">이 작업이 적용되는 헤더의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="074e3-116">-Value</span><span class="sxs-lookup"><span data-stu-id="074e3-116">-Value</span></span>
<span data-ttu-id="074e3-117">지정한 헤더 이름을 업데이트할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-117">The value to update the given header name with.</span></span>
<span data-ttu-id="074e3-118">actionType이 Delete인 경우 이 값은 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074e3-119">CommonParameters</span></span>
<span data-ttu-id="074e3-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="074e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074e3-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="074e3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074e3-122">입력</span><span class="sxs-lookup"><span data-stu-id="074e3-122">INPUTS</span></span>

### <span data-ttu-id="074e3-123">없음</span><span class="sxs-lookup"><span data-stu-id="074e3-123">None</span></span>

## <span data-ttu-id="074e3-124">출력</span><span class="sxs-lookup"><span data-stu-id="074e3-124">OUTPUTS</span></span>

### <span data-ttu-id="074e3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="074e3-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="074e3-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="074e3-126">NOTES</span></span>

## <span data-ttu-id="074e3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="074e3-127">RELATED LINKS</span></span>