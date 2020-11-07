---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: f8e51258a56051edf99aa1ec0cfa5e252e0ac0d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869873"
---
# <span data-ttu-id="fd91a-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fd91a-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="fd91a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd91a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd91a-103">새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="fd91a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd91a-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd91a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fd91a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd91a-106">New-AzPacketCaptureFilterConfig cmdlet은 새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="fd91a-107">이 개체는 지정 된 기준을 사용 하 여 패킷 캡처 세션 중에 캡처한 패킷의 유형을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="fd91a-108">New-AzNetworkWatcherPacketCapture cmdlet은 여러 필터 개체를 허용 하 여 작성 가능한 캡처 세션을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="fd91a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fd91a-109">EXAMPLES</span></span>

### <span data-ttu-id="fd91a-110">예제 1: 여러 필터를 사용 하 여 패킷 캡처 만들기</span><span class="sxs-lookup"><span data-stu-id="fd91a-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="fd91a-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="fd91a-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="fd91a-113">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="fd91a-114">변수</span><span class="sxs-lookup"><span data-stu-id="fd91a-114">PARAMETERS</span></span>

### <span data-ttu-id="fd91a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd91a-115">-DefaultProfile</span></span>
<span data-ttu-id="fd91a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd91a-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="fd91a-117">-LocalIPAddress</span></span>
<span data-ttu-id="fd91a-118">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="fd91a-119">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="fd91a-120">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="fd91a-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="fd91a-121">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="fd91a-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="fd91a-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="fd91a-122">-LocalPort</span></span>
<span data-ttu-id="fd91a-123">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="fd91a-124">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="fd91a-125">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="fd91a-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="fd91a-126">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="fd91a-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="fd91a-127">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="fd91a-127">-Protocol</span></span>
<span data-ttu-id="fd91a-128">필터링 할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="fd91a-129">허용 되는 값 "TCP", "UDP", "모든"</span><span class="sxs-lookup"><span data-stu-id="fd91a-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="fd91a-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="fd91a-130">-RemoteIPAddress</span></span>
<span data-ttu-id="fd91a-131">필터링 할 원격 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="fd91a-132">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="fd91a-133">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="fd91a-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="fd91a-134">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="fd91a-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="fd91a-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="fd91a-135">-RemotePort</span></span>
<span data-ttu-id="fd91a-136">필터링 할 원격 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="fd91a-137">원격 포트 예제 입력: 단일 포트 항목의 경우 "80".</span><span class="sxs-lookup"><span data-stu-id="fd91a-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="fd91a-138">범위에 대 한 "80-85".</span><span class="sxs-lookup"><span data-stu-id="fd91a-138">"80-85" for range.</span></span>
<span data-ttu-id="fd91a-139">여러 항목에 대해 "80; 443;"</span><span class="sxs-lookup"><span data-stu-id="fd91a-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="fd91a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd91a-140">CommonParameters</span></span>
<span data-ttu-id="fd91a-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd91a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd91a-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd91a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd91a-143">입력</span><span class="sxs-lookup"><span data-stu-id="fd91a-143">INPUTS</span></span>

### <span data-ttu-id="fd91a-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd91a-144">System.String</span></span>

## <span data-ttu-id="fd91a-145">출력</span><span class="sxs-lookup"><span data-stu-id="fd91a-145">OUTPUTS</span></span>

### <span data-ttu-id="fd91a-146">PSPacketCaptureFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fd91a-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="fd91a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="fd91a-147">NOTES</span></span>
<span data-ttu-id="fd91a-148">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터</span><span class="sxs-lookup"><span data-stu-id="fd91a-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="fd91a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd91a-149">RELATED LINKS</span></span>

[<span data-ttu-id="fd91a-150">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd91a-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fd91a-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd91a-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="fd91a-152">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fd91a-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fd91a-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fd91a-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fd91a-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fd91a-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fd91a-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fd91a-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fd91a-156">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fd91a-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="fd91a-157">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd91a-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fd91a-158">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fd91a-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fd91a-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd91a-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fd91a-160">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd91a-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fd91a-161">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd91a-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fd91a-162">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd91a-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="fd91a-163">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fd91a-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fd91a-164">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fd91a-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="fd91a-165">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd91a-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fd91a-166">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd91a-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fd91a-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd91a-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fd91a-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fd91a-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="fd91a-169">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd91a-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fd91a-170">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd91a-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="fd91a-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fd91a-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="fd91a-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fd91a-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="fd91a-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fd91a-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="fd91a-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fd91a-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="fd91a-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fd91a-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="fd91a-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd91a-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)