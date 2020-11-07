---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876574"
---
# <span data-ttu-id="1e1e9-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e1e9-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="1e1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1e9-103">프로브 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="1e1e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e1e9-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e1e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e1e9-106">**AzLoadBalancerProbeConfig** cmdlet은 프로브 구성에 대 한 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="1e1e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="1e1e9-108">예제 1: 부하 분산 장치에서 프로브 구성 수정</span><span class="sxs-lookup"><span data-stu-id="1e1e9-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="1e1e9-109">첫 번째 명령은 MyLoadBalancer 라는 부하 분산 장치를 가져온 다음 $slb 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="1e1e9-110">두 번째 명령은 파이프라인 연산자를 사용 하 여 $slb의 부하 분산을 추가-AzLoadBalancerProbeConfig에 전달 하 여 새 프로브 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="1e1e9-111">세 번째 명령은 새 구성을 설정 하는 **AzLoadBalancerProbeConfig** 에 부하 분산을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="1e1e9-112">이전 명령에 지정 된 것과 동일한 매개 변수 중 몇 개는 현재 cmdlet에 필요 하므로 반드시 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="1e1e9-113">변수</span><span class="sxs-lookup"><span data-stu-id="1e1e9-113">PARAMETERS</span></span>

### <span data-ttu-id="1e1e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1e9-114">-DefaultProfile</span></span>
<span data-ttu-id="1e1e9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-116">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1e1e9-116">-IntervalInSeconds</span></span>
<span data-ttu-id="1e1e9-117">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e1e9-118">-LoadBalancer</span></span>
<span data-ttu-id="1e1e9-119">부하 분산 장치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-119">Specifies a load balancer.</span></span>
<span data-ttu-id="1e1e9-120">이 cmdlet은이 매개 변수에서 지정 하는 부하 분산 장치에 대 한 검색 구성의 목표 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1e1e9-121">-Name</span></span>
<span data-ttu-id="1e1e9-122">이 cmdlet이 설정 하는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-123">-포트</span><span class="sxs-lookup"><span data-stu-id="1e1e9-123">-Port</span></span>
<span data-ttu-id="1e1e9-124">프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="1e1e9-125">-ProbeCount</span></span>
<span data-ttu-id="1e1e9-126">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-127">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="1e1e9-127">-Protocol</span></span>
<span data-ttu-id="1e1e9-128">검색에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="1e1e9-129">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="1e1e9-130">-RequestPath</span></span>
<span data-ttu-id="1e1e9-131">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e1e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1e9-132">CommonParameters</span></span>
<span data-ttu-id="1e1e9-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1e9-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1e9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1e9-135">입력</span><span class="sxs-lookup"><span data-stu-id="1e1e9-135">INPUTS</span></span>

### <span data-ttu-id="1e1e9-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e1e9-136">PSLoadBalancer</span></span>
<span data-ttu-id="1e1e9-137">' LoadBalancer ' 매개 변수는 파이프라인에서 ' PSLoadBalancer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e1e9-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1e1e9-138">출력</span><span class="sxs-lookup"><span data-stu-id="1e1e9-138">OUTPUTS</span></span>

### <span data-ttu-id="1e1e9-139">Microsoft. 네트워크. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e1e9-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1e1e9-140">상속자</span><span class="sxs-lookup"><span data-stu-id="1e1e9-140">NOTES</span></span>

## <span data-ttu-id="1e1e9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e1e9-141">RELATED LINKS</span></span>

[<span data-ttu-id="1e1e9-142">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e1e9-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="1e1e9-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1e1e9-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1e1e9-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e1e9-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="1e1e9-145">새로운 AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e1e9-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="1e1e9-146">제거-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1e1e9-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

