---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329454"
---
# <span data-ttu-id="7575b-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="7575b-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="7575b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7575b-102">SYNOPSIS</span></span>
<span data-ttu-id="7575b-103">새 네트워크 구성 진단 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="7575b-104">이 개체는 지정된 조건을 사용하여 진단 세션 중에 네트워크 구성을 제한하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="7575b-105">구문</span><span class="sxs-lookup"><span data-stu-id="7575b-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7575b-106">설명</span><span class="sxs-lookup"><span data-stu-id="7575b-106">DESCRIPTION</span></span>
<span data-ttu-id="7575b-107">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet은 새 진단 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="7575b-108">이 개체는 지정된 조건을 사용하여 네트워크 구성 진단 세션 중에 네트워크 구성을 제한하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="7575b-109">예제</span><span class="sxs-lookup"><span data-stu-id="7575b-109">EXAMPLES</span></span>

### <span data-ttu-id="7575b-110">예제 1: VM 및 지정된 네트워크 프로필에 대한 네트워크 구성 진단 세션 호출</span><span class="sxs-lookup"><span data-stu-id="7575b-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="7575b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7575b-111">PARAMETERS</span></span>

### <span data-ttu-id="7575b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7575b-112">-DefaultProfile</span></span>
<span data-ttu-id="7575b-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7575b-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="7575b-114">-Destination</span></span>
<span data-ttu-id="7575b-115">트래픽 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-115">Traffic destination.</span></span>
<span data-ttu-id="7575b-116">허용되는 값은 '\*', IP 주소/CIDR, 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="7575b-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7575b-117">-DestinationPort</span></span>
<span data-ttu-id="7575b-118">트래픽 대상 포트.</span><span class="sxs-lookup"><span data-stu-id="7575b-118">Traffic destination port.</span></span>
<span data-ttu-id="7575b-119">허용되는 값은 '\*', 포트(예: 3389) 및 포트 범위(예: 80-100)입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="7575b-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="7575b-120">-Direction</span></span>
<span data-ttu-id="7575b-121">트래픽의 방향입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-121">The direction of the traffic.</span></span>
<span data-ttu-id="7575b-122">허용되는 값은 '인바운드' 및 '아웃바운드'입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7575b-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7575b-123">-Protocol</span></span>
<span data-ttu-id="7575b-124">확인할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-124">Protocol to be verified on.</span></span>
<span data-ttu-id="7575b-125">허용되는 값은 '\*', TCP, UDP입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="7575b-126">-Source</span><span class="sxs-lookup"><span data-stu-id="7575b-126">-Source</span></span>
<span data-ttu-id="7575b-127">트래픽 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-127">Traffic source.</span></span>
<span data-ttu-id="7575b-128">허용되는 값은 '\*', IP 주소/CIDR, 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="7575b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7575b-129">CommonParameters</span></span>
<span data-ttu-id="7575b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7575b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7575b-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7575b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7575b-132">입력</span><span class="sxs-lookup"><span data-stu-id="7575b-132">INPUTS</span></span>

### <span data-ttu-id="7575b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7575b-133">System.String</span></span>

## <span data-ttu-id="7575b-134">출력</span><span class="sxs-lookup"><span data-stu-id="7575b-134">OUTPUTS</span></span>

### <span data-ttu-id="7575b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="7575b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="7575b-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7575b-136">NOTES</span></span>
<span data-ttu-id="7575b-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 감시자, 진단, 프로필</span><span class="sxs-lookup"><span data-stu-id="7575b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="7575b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7575b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7575b-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7575b-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7575b-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7575b-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7575b-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7575b-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7575b-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7575b-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7575b-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7575b-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7575b-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7575b-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7575b-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7575b-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7575b-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7575b-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7575b-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7575b-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7575b-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7575b-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7575b-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7575b-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7575b-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7575b-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7575b-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7575b-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7575b-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7575b-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7575b-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7575b-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="7575b-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7575b-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7575b-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7575b-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7575b-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7575b-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7575b-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7575b-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7575b-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7575b-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7575b-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7575b-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7575b-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7575b-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7575b-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7575b-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7575b-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7575b-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7575b-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7575b-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7575b-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7575b-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="7575b-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7575b-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)