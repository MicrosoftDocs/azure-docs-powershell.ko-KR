---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: c217a34bb89dcaa67dfc0794871e5d105ded6df1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047201"
---
# <span data-ttu-id="6983c-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6983c-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="6983c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6983c-102">SYNOPSIS</span></span>
<span data-ttu-id="6983c-103">작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="6983c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6983c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6983c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6983c-105">DESCRIPTION</span></span>
<span data-ttu-id="6983c-106">**AzOperationalInsightsWorkspace** cmdlet은 기존 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="6983c-107">작업 영역 이름을 지정 하는 경우이 cmdlet은 해당 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="6983c-108">이름을 지정 하지 않으면이 cmdlet은 리소스 그룹의 모든 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="6983c-109">이름과 리소스 그룹을 지정 하지 않으면이 cmdlet은 구독의 모든 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="6983c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6983c-110">EXAMPLES</span></span>

### <span data-ttu-id="6983c-111">예제 1: 이름으로 작업 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="6983c-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="6983c-112">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="6983c-113">변수</span><span class="sxs-lookup"><span data-stu-id="6983c-113">PARAMETERS</span></span>

### <span data-ttu-id="6983c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6983c-114">-DefaultProfile</span></span>
<span data-ttu-id="6983c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6983c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6983c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="6983c-116">-Name</span></span>
<span data-ttu-id="6983c-117">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6983c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6983c-118">-ResourceGroupName</span></span>
<span data-ttu-id="6983c-119">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6983c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6983c-120">CommonParameters</span></span>
<span data-ttu-id="6983c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6983c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6983c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6983c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6983c-123">입력</span><span class="sxs-lookup"><span data-stu-id="6983c-123">INPUTS</span></span>

### <span data-ttu-id="6983c-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6983c-124">System.String</span></span>

## <span data-ttu-id="6983c-125">출력</span><span class="sxs-lookup"><span data-stu-id="6983c-125">OUTPUTS</span></span>

### <span data-ttu-id="6983c-126">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="6983c-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="6983c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="6983c-127">NOTES</span></span>

## <span data-ttu-id="6983c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6983c-128">RELATED LINKS</span></span>

[<span data-ttu-id="6983c-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6983c-129">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

