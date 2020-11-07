---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 4f8fcbc0e5eee5aea92493b54acc631ffd144d3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870113"
---
# <span data-ttu-id="86c40-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86c40-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="86c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86c40-102">SYNOPSIS</span></span>
<span data-ttu-id="86c40-103">이전에 실행 되었거나 현재 실행 중인 문제 해결 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="86c40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="86c40-104">SYNTAX</span></span>

### <span data-ttu-id="86c40-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="86c40-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86c40-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="86c40-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86c40-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86c40-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86c40-108">설명은</span><span class="sxs-lookup"><span data-stu-id="86c40-108">DESCRIPTION</span></span>
<span data-ttu-id="86c40-109">Get-AzNetworkWatcherTroubleshootingResult cmdlet은 이전에 실행 되거나 현재 실행 중인 Start-AzNetworkWatcherResourceTroubleshooting 작업의 문제 해결 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="86c40-110">현재 문제 해결 작업이 진행 중인 경우이 작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="86c40-111">현재 가상 네트워크 게이트웨이 및 연결이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="86c40-112">예제의</span><span class="sxs-lookup"><span data-stu-id="86c40-112">EXAMPLES</span></span>

### <span data-ttu-id="86c40-113">예제 1: 가상 네트워크 게이트웨이에서 문제 해결을 시작 하 고 결과 검색</span><span class="sxs-lookup"><span data-stu-id="86c40-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="86c40-114">위의 샘플에서는 가상 네트워크 게이트웨이에서 문제 해결을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="86c40-115">작업을 완료 하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="86c40-116">문제 해결이 시작 된 후에는이 통화의 결과를 검색 하기 위해 리소스에 대 한 Get-AzNetworkWatcherTroubleshootingResult 호출이 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="86c40-117">변수</span><span class="sxs-lookup"><span data-stu-id="86c40-117">PARAMETERS</span></span>

### <span data-ttu-id="86c40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c40-118">-DefaultProfile</span></span>
<span data-ttu-id="86c40-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86c40-120">-위치</span><span class="sxs-lookup"><span data-stu-id="86c40-120">-Location</span></span>
<span data-ttu-id="86c40-121">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-121">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c40-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86c40-122">-NetworkWatcher</span></span>
<span data-ttu-id="86c40-123">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="86c40-123">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c40-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="86c40-124">-NetworkWatcherName</span></span>
<span data-ttu-id="86c40-125">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-125">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86c40-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c40-126">-ResourceGroupName</span></span>
<span data-ttu-id="86c40-127">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-127">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c40-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="86c40-128">-TargetResourceId</span></span>
<span data-ttu-id="86c40-129">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-129">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c40-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c40-130">CommonParameters</span></span>
<span data-ttu-id="86c40-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86c40-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c40-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="86c40-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c40-133">입력</span><span class="sxs-lookup"><span data-stu-id="86c40-133">INPUTS</span></span>

### <span data-ttu-id="86c40-134">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86c40-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="86c40-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="86c40-135">System.String</span></span>

## <span data-ttu-id="86c40-136">출력</span><span class="sxs-lookup"><span data-stu-id="86c40-136">OUTPUTS</span></span>

### <span data-ttu-id="86c40-137">PSTroubleshootingResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="86c40-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="86c40-138">상속자</span><span class="sxs-lookup"><span data-stu-id="86c40-138">NOTES</span></span>
<span data-ttu-id="86c40-139">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 문제 해결, VPN, 연결</span><span class="sxs-lookup"><span data-stu-id="86c40-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="86c40-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86c40-140">RELATED LINKS</span></span>

[<span data-ttu-id="86c40-141">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86c40-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="86c40-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86c40-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="86c40-143">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86c40-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="86c40-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86c40-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="86c40-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86c40-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86c40-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86c40-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="86c40-147">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86c40-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="86c40-148">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86c40-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86c40-149">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86c40-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="86c40-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86c40-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86c40-151">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86c40-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86c40-152">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86c40-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86c40-153">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86c40-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="86c40-154">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86c40-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="86c40-155">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86c40-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="86c40-156">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86c40-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86c40-157">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86c40-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86c40-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86c40-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86c40-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86c40-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="86c40-160">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86c40-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86c40-161">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86c40-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86c40-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86c40-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="86c40-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86c40-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="86c40-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86c40-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="86c40-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86c40-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="86c40-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86c40-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="86c40-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86c40-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)