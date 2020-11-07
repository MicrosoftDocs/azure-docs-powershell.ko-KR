---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872210"
---
# <span data-ttu-id="6c308-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6c308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c308-102">SYNOPSIS</span></span>
<span data-ttu-id="6c308-103">Traffic Manager 프로필에 대 한 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="6c308-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c308-104">SYNTAX</span></span>

### <span data-ttu-id="6c308-105">필드인</span><span class="sxs-lookup"><span data-stu-id="6c308-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c308-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="6c308-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c308-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6c308-107">DESCRIPTION</span></span>
<span data-ttu-id="6c308-108">**AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에 대 한 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="6c308-109">이 개체를 로컬로 수정한 다음 Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="6c308-110">*Name* 및 *Type* 매개 변수를 사용 하 여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="6c308-111">*/Profile* 및 *ResourceGroupName* 매개 변수를 사용 하거나 **TrafficManagerProfile** 개체를 지정 하 여 Traffic Manager 프로필을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6c308-112">또는 파이프라인을 사용 하 여 해당 값을 전달할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="6c308-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6c308-113">EXAMPLES</span></span>

### <span data-ttu-id="6c308-114">예제 1: 끝점 가져오기</span><span class="sxs-lookup"><span data-stu-id="6c308-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="6c308-115">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="6c308-116">변수</span><span class="sxs-lookup"><span data-stu-id="6c308-116">PARAMETERS</span></span>

### <span data-ttu-id="6c308-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c308-117">-DefaultProfile</span></span>
<span data-ttu-id="6c308-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c308-119">-이름</span><span class="sxs-lookup"><span data-stu-id="6c308-119">-Name</span></span>
<span data-ttu-id="6c308-120">이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c308-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="6c308-121">-ProfileName</span></span>
<span data-ttu-id="6c308-122">이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c308-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c308-123">-ResourceGroupName</span></span>
<span data-ttu-id="6c308-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6c308-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹의 Traffic Manager 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c308-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6c308-127">이 cmdlet이 가져오는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c308-128">-Type</span><span class="sxs-lookup"><span data-stu-id="6c308-128">-Type</span></span>
<span data-ttu-id="6c308-129">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="6c308-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-130">Valid values are:</span></span> 

- <span data-ttu-id="6c308-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="6c308-131">AzureEndpoints</span></span>
- <span data-ttu-id="6c308-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="6c308-132">ExternalEndpoints</span></span>
- <span data-ttu-id="6c308-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="6c308-133">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c308-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c308-134">CommonParameters</span></span>
<span data-ttu-id="6c308-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c308-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c308-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c308-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c308-137">입력</span><span class="sxs-lookup"><span data-stu-id="6c308-137">INPUTS</span></span>

### <span data-ttu-id="6c308-138">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="6c308-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6c308-139">출력</span><span class="sxs-lookup"><span data-stu-id="6c308-139">OUTPUTS</span></span>

### <span data-ttu-id="6c308-140">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="6c308-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6c308-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6c308-141">NOTES</span></span>

## <span data-ttu-id="6c308-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c308-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c308-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6c308-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6c308-145">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6c308-146">제거-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6c308-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c308-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

