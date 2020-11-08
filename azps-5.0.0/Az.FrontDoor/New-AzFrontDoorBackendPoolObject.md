---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217429"
---
# <span data-ttu-id="ef449-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="ef449-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="ef449-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef449-102">SYNOPSIS</span></span>
<span data-ttu-id="ef449-103">전방 도어 만들기에 대 한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ef449-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="ef449-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef449-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef449-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef449-105">DESCRIPTION</span></span>
<span data-ttu-id="ef449-106">전방 도어 만들기에 대 한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ef449-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="ef449-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef449-107">EXAMPLES</span></span>

### <span data-ttu-id="ef449-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef449-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="ef449-109">전방 도어 만들기에 대 한 PSBackendPool 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ef449-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="ef449-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef449-110">PARAMETERS</span></span>

### <span data-ttu-id="ef449-111">-백 엔드</span><span class="sxs-lookup"><span data-stu-id="ef449-111">-Backend</span></span>
<span data-ttu-id="ef449-112">이 풀의 백 엔드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef449-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef449-113">-DefaultProfile</span></span>
<span data-ttu-id="ef449-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef449-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="ef449-115">-FrontDoorName</span></span>
<span data-ttu-id="ef449-116">이 라우팅 규칙이 속한 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="ef449-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="ef449-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="ef449-118">이 백 엔드 풀에 대 한 상태 프로브 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="ef449-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="ef449-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="ef449-120">이 백 엔드 풀에 대 한 부하 분산 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="ef449-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ef449-121">-Name</span></span>
<span data-ttu-id="ef449-122">BackendPool 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-122">BackendPool name.</span></span>

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

### <span data-ttu-id="ef449-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef449-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef449-124">RoutingRule를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="ef449-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef449-125">CommonParameters</span></span>
<span data-ttu-id="ef449-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef449-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef449-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef449-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef449-128">입력</span><span class="sxs-lookup"><span data-stu-id="ef449-128">INPUTS</span></span>

### <span data-ttu-id="ef449-129">않아야</span><span class="sxs-lookup"><span data-stu-id="ef449-129">None</span></span>

## <span data-ttu-id="ef449-130">출력</span><span class="sxs-lookup"><span data-stu-id="ef449-130">OUTPUTS</span></span>

### <span data-ttu-id="ef449-131">FrontDoor. PSBackendPool/.</span><span class="sxs-lookup"><span data-stu-id="ef449-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="ef449-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ef449-132">NOTES</span></span>

## <span data-ttu-id="ef449-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef449-133">RELATED LINKS</span></span>

<span data-ttu-id="ef449-134">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [새로운 AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="ef449-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>