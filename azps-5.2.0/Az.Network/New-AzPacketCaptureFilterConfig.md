---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335901"
---
# <span data-ttu-id="23b21-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="23b21-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="23b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b21-102">SYNOPSIS</span></span>
<span data-ttu-id="23b21-103">새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="23b21-104">구문</span><span class="sxs-lookup"><span data-stu-id="23b21-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23b21-105">설명</span><span class="sxs-lookup"><span data-stu-id="23b21-105">DESCRIPTION</span></span>
<span data-ttu-id="23b21-106">New-AzPacketCaptureFilterConfig cmdlet은 새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="23b21-107">이 개체는 지정된 조건을 사용하여 패킷 캡처 세션 중에 캡처되는 패킷 유형을 제한하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="23b21-108">New-AzNetworkWatcherPacketCapture cmdlet은 여러 필터 개체를 수락하여 구성 가능한 캡처 세션을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="23b21-109">예제</span><span class="sxs-lookup"><span data-stu-id="23b21-109">EXAMPLES</span></span>

### <span data-ttu-id="23b21-110">예제 1: 여러 필터를 사용하여 패킷 캡처 만들기</span><span class="sxs-lookup"><span data-stu-id="23b21-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="23b21-111">이 예제에서는 여러 필터와 시간 제한이 있는 "PacketCaptureTest"라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="23b21-112">세션이 완료되면 지정된 저장소 계정에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="23b21-113">참고: 패킷 캡처를 만들 대상 가상 머신에 Azure Network Watcher 확장을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="23b21-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23b21-114">PARAMETERS</span></span>

### <span data-ttu-id="23b21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b21-115">-DefaultProfile</span></span>
<span data-ttu-id="23b21-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23b21-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="23b21-117">-LocalIPAddress</span></span>
<span data-ttu-id="23b21-118">필터링할 로컬 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="23b21-119">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="23b21-120">범위에 대한 "127.0.0.1-127.0.0.255"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="23b21-121">여러 항목에 대한 "127.0.0.1;127.0.0.5;"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="23b21-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="23b21-122">-LocalPort</span></span>
<span data-ttu-id="23b21-123">필터링할 로컬 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="23b21-124">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="23b21-125">범위에 대한 "127.0.0.1-127.0.0.255"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="23b21-126">여러 항목에 대한 "127.0.0.1;127.0.0.5;"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="23b21-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="23b21-127">-Protocol</span></span>
<span data-ttu-id="23b21-128">필터링할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="23b21-129">허용되는 값 "TCP","UDP","Any"</span><span class="sxs-lookup"><span data-stu-id="23b21-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23b21-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="23b21-130">-RemoteIPAddress</span></span>
<span data-ttu-id="23b21-131">필터링할 원격 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="23b21-132">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="23b21-133">범위에 대한 "127.0.0.1-127.0.0.255"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="23b21-134">여러 항목에 대한 "127.0.0.1;127.0.0.5;"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="23b21-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="23b21-135">-RemotePort</span></span>
<span data-ttu-id="23b21-136">필터링할 원격 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="23b21-137">원격 포트 예제 입력: 단일 포트 항목의 경우 "80"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="23b21-138">범위의 경우 "80-85"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-138">"80-85" for range.</span></span>
<span data-ttu-id="23b21-139">여러 항목에 대한 "80;443;"입니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="23b21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b21-140">CommonParameters</span></span>
<span data-ttu-id="23b21-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23b21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b21-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="23b21-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b21-143">입력</span><span class="sxs-lookup"><span data-stu-id="23b21-143">INPUTS</span></span>

### <span data-ttu-id="23b21-144">System.String</span><span class="sxs-lookup"><span data-stu-id="23b21-144">System.String</span></span>

## <span data-ttu-id="23b21-145">출력</span><span class="sxs-lookup"><span data-stu-id="23b21-145">OUTPUTS</span></span>

### <span data-ttu-id="23b21-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="23b21-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="23b21-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23b21-147">NOTES</span></span>
<span data-ttu-id="23b21-148">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터</span><span class="sxs-lookup"><span data-stu-id="23b21-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="23b21-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23b21-149">RELATED LINKS</span></span>

[<span data-ttu-id="23b21-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23b21-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="23b21-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23b21-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="23b21-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="23b21-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="23b21-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="23b21-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="23b21-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="23b21-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="23b21-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="23b21-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="23b21-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="23b21-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="23b21-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23b21-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23b21-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="23b21-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="23b21-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23b21-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23b21-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23b21-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23b21-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23b21-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="23b21-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="23b21-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="23b21-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="23b21-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="23b21-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="23b21-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="23b21-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23b21-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23b21-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23b21-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23b21-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23b21-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23b21-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="23b21-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="23b21-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23b21-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23b21-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23b21-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="23b21-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="23b21-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="23b21-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="23b21-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="23b21-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="23b21-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="23b21-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="23b21-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="23b21-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="23b21-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="23b21-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="23b21-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)