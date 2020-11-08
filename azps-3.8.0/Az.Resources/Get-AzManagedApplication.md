---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041600"
---
# <span data-ttu-id="07de6-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="07de6-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="07de6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07de6-102">SYNOPSIS</span></span>
<span data-ttu-id="07de6-103">관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-103">Gets managed applications</span></span>

## <span data-ttu-id="07de6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07de6-104">SYNTAX</span></span>

### <span data-ttu-id="07de6-105">GetBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="07de6-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07de6-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="07de6-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07de6-107">GetById</span><span class="sxs-lookup"><span data-stu-id="07de6-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07de6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="07de6-108">DESCRIPTION</span></span>
<span data-ttu-id="07de6-109">**Get-AzManagedApplication** cmdlet은 관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="07de6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="07de6-110">EXAMPLES</span></span>

### <span data-ttu-id="07de6-111">예제 1: 리소스 그룹 아래에 모든 관리 되는 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="07de6-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="07de6-112">이 명령은 리소스 그룹 "MyRG"에서 관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="07de6-113">예제 2: 관리 되는 모든 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="07de6-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="07de6-114">이 명령은 현재 구독에서 관리 되는 모든 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="07de6-115">변수</span><span class="sxs-lookup"><span data-stu-id="07de6-115">PARAMETERS</span></span>

### <span data-ttu-id="07de6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="07de6-116">-ApiVersion</span></span>
<span data-ttu-id="07de6-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="07de6-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="07de6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07de6-119">-DefaultProfile</span></span>
<span data-ttu-id="07de6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07de6-121">-Id</span><span class="sxs-lookup"><span data-stu-id="07de6-121">-Id</span></span>
<span data-ttu-id="07de6-122">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="07de6-123">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="07de6-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07de6-124">-이름</span><span class="sxs-lookup"><span data-stu-id="07de6-124">-Name</span></span>
<span data-ttu-id="07de6-125">관리 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07de6-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="07de6-126">-Pre</span></span>
<span data-ttu-id="07de6-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="07de6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07de6-128">-ResourceGroupName</span></span>
<span data-ttu-id="07de6-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07de6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07de6-130">CommonParameters</span></span>
<span data-ttu-id="07de6-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07de6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07de6-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07de6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07de6-133">입력</span><span class="sxs-lookup"><span data-stu-id="07de6-133">INPUTS</span></span>

### <span data-ttu-id="07de6-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07de6-134">System.String</span></span>

## <span data-ttu-id="07de6-135">출력</span><span class="sxs-lookup"><span data-stu-id="07de6-135">OUTPUTS</span></span>

### <span data-ttu-id="07de6-136">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="07de6-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="07de6-137">상속자</span><span class="sxs-lookup"><span data-stu-id="07de6-137">NOTES</span></span>

## <span data-ttu-id="07de6-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07de6-138">RELATED LINKS</span></span>