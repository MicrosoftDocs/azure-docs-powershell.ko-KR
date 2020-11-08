---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: ff90a33b9ca54f805f2fa5e8f3579660480b73ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214829"
---
# <span data-ttu-id="9cf21-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9cf21-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="9cf21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cf21-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf21-103">부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="9cf21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9cf21-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf21-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9cf21-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf21-106">**AzLoadBalancerProbeConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9cf21-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9cf21-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf21-108">예제 1: 프로브 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="9cf21-108">Example 1: Create a probe configuration</span></span>
```powershell
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="9cf21-109">이 명령은 HTTP 프로토콜을 사용 하 여 MyProbe 라는 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="9cf21-110">새 프로브는 포트 80의 부하 분산 서비스에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-110">The new probe will connect to a load-balanced service on port 80.</span></span>

### <span data-ttu-id="9cf21-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="9cf21-111">Example 2</span></span>

<span data-ttu-id="9cf21-112">부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-112">Creates a probe configuration for a load balancer.</span></span> <span data-ttu-id="9cf21-113">생성</span><span class="sxs-lookup"><span data-stu-id="9cf21-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerProbeConfig -IntervalInSeconds 15 -Name 'MyProbe' -Port 80 -ProbeCount 15 -Protocol 'http' -RequestPath 'healthcheck.aspx'
```

## <span data-ttu-id="9cf21-114">변수</span><span class="sxs-lookup"><span data-stu-id="9cf21-114">PARAMETERS</span></span>

### <span data-ttu-id="9cf21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf21-115">-DefaultProfile</span></span>
<span data-ttu-id="9cf21-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf21-117">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9cf21-117">-IntervalInSeconds</span></span>
<span data-ttu-id="9cf21-118">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-118">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf21-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9cf21-119">-Name</span></span>
<span data-ttu-id="9cf21-120">만들려는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-120">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="9cf21-121">-포트</span><span class="sxs-lookup"><span data-stu-id="9cf21-121">-Port</span></span>
<span data-ttu-id="9cf21-122">새 프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-122">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf21-123">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="9cf21-123">-ProbeCount</span></span>
<span data-ttu-id="9cf21-124">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-124">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf21-125">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="9cf21-125">-Protocol</span></span>
<span data-ttu-id="9cf21-126">프로브 구성에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-126">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="9cf21-127">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-127">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf21-128">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="9cf21-128">-RequestPath</span></span>
<span data-ttu-id="9cf21-129">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-129">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf21-130">-확인</span><span class="sxs-lookup"><span data-stu-id="9cf21-130">-Confirm</span></span>
<span data-ttu-id="9cf21-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf21-132">-WhatIf</span></span>
<span data-ttu-id="9cf21-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cf21-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf21-135">CommonParameters</span></span>
<span data-ttu-id="9cf21-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9cf21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf21-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf21-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf21-138">입력</span><span class="sxs-lookup"><span data-stu-id="9cf21-138">INPUTS</span></span>

### <span data-ttu-id="9cf21-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9cf21-139">System.String</span></span>

### <span data-ttu-id="9cf21-140">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="9cf21-140">System.Int32</span></span>

## <span data-ttu-id="9cf21-141">출력</span><span class="sxs-lookup"><span data-stu-id="9cf21-141">OUTPUTS</span></span>

### <span data-ttu-id="9cf21-142">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="9cf21-142">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="9cf21-143">상속자</span><span class="sxs-lookup"><span data-stu-id="9cf21-143">NOTES</span></span>

## <span data-ttu-id="9cf21-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cf21-144">RELATED LINKS</span></span>

[<span data-ttu-id="9cf21-145">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9cf21-145">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9cf21-146">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9cf21-146">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9cf21-147">제거-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9cf21-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="9cf21-148">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9cf21-148">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)

