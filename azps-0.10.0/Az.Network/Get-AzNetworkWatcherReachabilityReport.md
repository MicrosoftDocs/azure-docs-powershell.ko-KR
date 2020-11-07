---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875543"
---
# <span data-ttu-id="07b94-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="07b94-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="07b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b94-102">SYNOPSIS</span></span>
<span data-ttu-id="07b94-103">지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="07b94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07b94-104">SYNTAX</span></span>

### <span data-ttu-id="07b94-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="07b94-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07b94-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="07b94-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07b94-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="07b94-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07b94-108">설명은</span><span class="sxs-lookup"><span data-stu-id="07b94-108">DESCRIPTION</span></span>
<span data-ttu-id="07b94-109">Get-AzNetworkWatcherReachabilityReport는 지정 된 위치에서 Azure 지역 까지의 인터넷 서비스 공급자에 대 한 상대 대기 시간 점수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="07b94-110">예제의</span><span class="sxs-lookup"><span data-stu-id="07b94-110">EXAMPLES</span></span>

### <span data-ttu-id="07b94-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="07b94-111">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="07b94-112">미국 내에서 2017-10-10부터 2017-10-12 까지의 Azure 데이터 센터에 대 한 상대적 대기 시간을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="07b94-113">변수</span><span class="sxs-lookup"><span data-stu-id="07b94-113">PARAMETERS</span></span>

### <span data-ttu-id="07b94-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07b94-114">-AsJob</span></span>
<span data-ttu-id="07b94-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="07b94-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-116">-구/군/시</span><span class="sxs-lookup"><span data-stu-id="07b94-116">-City</span></span>
<span data-ttu-id="07b94-117">구/군/시의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-117">The name of the city.</span></span>

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

### <span data-ttu-id="07b94-118">-국가</span><span class="sxs-lookup"><span data-stu-id="07b94-118">-Country</span></span>
<span data-ttu-id="07b94-119">국가의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-119">The name of the country.</span></span>

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

### <span data-ttu-id="07b94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b94-120">-DefaultProfile</span></span>
<span data-ttu-id="07b94-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07b94-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="07b94-122">-EndTime</span></span>
<span data-ttu-id="07b94-123">Azure 연결 가능성 보고서의 종료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-124">-위치</span><span class="sxs-lookup"><span data-stu-id="07b94-124">-Location</span></span>
<span data-ttu-id="07b94-125">쿼리 범위를 지정 하는 선택적 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-125">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07b94-126">-NetworkWatcher</span></span>
<span data-ttu-id="07b94-127">네트워크 감시자 리소스</span><span class="sxs-lookup"><span data-stu-id="07b94-127">The network watcher resource</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="07b94-128">-NetworkWatcherName</span></span>
<span data-ttu-id="07b94-129">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-130">-공급자</span><span class="sxs-lookup"><span data-stu-id="07b94-130">-Provider</span></span>
<span data-ttu-id="07b94-131">인터넷 서비스 공급자 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-131">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b94-132">-ResourceGroupName</span></span>
<span data-ttu-id="07b94-133">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-133">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07b94-134">-ResourceId</span></span>
<span data-ttu-id="07b94-135">네트워크 감시자 리소스의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-135">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-136">-StartTime</span><span class="sxs-lookup"><span data-stu-id="07b94-136">-StartTime</span></span>
<span data-ttu-id="07b94-137">Azure 연결 가능성 보고서의 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b94-138">-상태</span><span class="sxs-lookup"><span data-stu-id="07b94-138">-State</span></span>
<span data-ttu-id="07b94-139">상태의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-139">The name of the state.</span></span>

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

### <span data-ttu-id="07b94-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b94-140">CommonParameters</span></span>
<span data-ttu-id="07b94-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07b94-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b94-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07b94-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b94-143">입력</span><span class="sxs-lookup"><span data-stu-id="07b94-143">INPUTS</span></span>

### <span data-ttu-id="07b94-144">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07b94-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="07b94-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07b94-145">System.String</span></span>

## <span data-ttu-id="07b94-146">출력</span><span class="sxs-lookup"><span data-stu-id="07b94-146">OUTPUTS</span></span>

### <span data-ttu-id="07b94-147">PSAzureReachabilityReport에 대 한.</span><span class="sxs-lookup"><span data-stu-id="07b94-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="07b94-148">상속자</span><span class="sxs-lookup"><span data-stu-id="07b94-148">NOTES</span></span>
<span data-ttu-id="07b94-149">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결성, 보고서</span><span class="sxs-lookup"><span data-stu-id="07b94-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="07b94-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07b94-150">RELATED LINKS</span></span>

[<span data-ttu-id="07b94-151">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07b94-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="07b94-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07b94-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="07b94-153">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07b94-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="07b94-154">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07b94-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="07b94-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="07b94-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="07b94-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="07b94-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="07b94-157">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="07b94-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="07b94-158">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07b94-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07b94-159">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="07b94-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="07b94-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07b94-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07b94-161">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07b94-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07b94-162">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07b94-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)