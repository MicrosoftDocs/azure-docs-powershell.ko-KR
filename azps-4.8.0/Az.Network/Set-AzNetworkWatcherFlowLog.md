---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 04a9b4c0ca8b613ce4d4c590572d80a729a65147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212968"
---
# <span data-ttu-id="9a6f2-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9a6f2-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="9a6f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a6f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6f2-103">흐름 로그 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-103">Updates flow log resource.</span></span>

## <span data-ttu-id="9a6f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a6f2-104">SYNTAX</span></span>

### <span data-ttu-id="9a6f2-105">SetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a6f2-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9a6f2-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="9a6f2-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="9a6f2-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9a6f2-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="9a6f2-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6f2-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="9a6f2-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6f2-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a6f2-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a6f2-114">설명은</span><span class="sxs-lookup"><span data-stu-id="9a6f2-114">DESCRIPTION</span></span>
<span data-ttu-id="9a6f2-115">흐름 로그 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-115">Updates flow log resource.</span></span>

## <span data-ttu-id="9a6f2-116">예제의</span><span class="sxs-lookup"><span data-stu-id="9a6f2-116">EXAMPLES</span></span>

### <span data-ttu-id="9a6f2-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a6f2-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="9a6f2-118">Name: pstest Id:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid a/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: 성공 위치: e us TargetResourceId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/MyNSG StorageId:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/Storageid/MyStorage 사용: True 보존 정책: {"일": 0, "사용": false} 형식: {"Type": "JSON", "Version": 2} FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="9a6f2-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="9a6f2-119">변수</span><span class="sxs-lookup"><span data-stu-id="9a6f2-119">PARAMETERS</span></span>

### <span data-ttu-id="9a6f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6f2-120">-DefaultProfile</span></span>
<span data-ttu-id="9a6f2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-122">-사용</span><span class="sxs-lookup"><span data-stu-id="9a6f2-122">-Enabled</span></span>
<span data-ttu-id="9a6f2-123">흐름 로깅을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="9a6f2-124">-EnableRetention</span></span>
<span data-ttu-id="9a6f2-125">보존을 설정/해제 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="9a6f2-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="9a6f2-127">TrafficAnalytics를 사용 하거나 사용 하지 않도록 설정 하는 플래그</span><span class="sxs-lookup"><span data-stu-id="9a6f2-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-128">-Force</span><span class="sxs-lookup"><span data-stu-id="9a6f2-128">-Force</span></span>
<span data-ttu-id="9a6f2-129">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="9a6f2-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9a6f2-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="9a6f2-130">-FormatType</span></span>
<span data-ttu-id="9a6f2-131">흐름 로그의 파일 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-131">The file type of flow log.</span></span>
<span data-ttu-id="9a6f2-132">현재 ' JSON ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="9a6f2-133">-FormatVersion</span></span>
<span data-ttu-id="9a6f2-134">흐름 로그의 버전 (개정)입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a6f2-135">-InputObject</span></span>
<span data-ttu-id="9a6f2-136">흐름 lof 개체.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-137">-위치</span><span class="sxs-lookup"><span data-stu-id="9a6f2-137">-Location</span></span>
<span data-ttu-id="9a6f2-138">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-138">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-139">-이름</span><span class="sxs-lookup"><span data-stu-id="9a6f2-139">-Name</span></span>
<span data-ttu-id="9a6f2-140">흐름 로그 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a6f2-141">-NetworkWatcher</span></span>
<span data-ttu-id="9a6f2-142">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-142">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9a6f2-143">-NetworkWatcherName</span></span>
<span data-ttu-id="9a6f2-144">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-144">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a6f2-145">-ResourceGroupName</span></span>
<span data-ttu-id="9a6f2-146">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-146">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6f2-147">-ResourceId</span></span>
<span data-ttu-id="9a6f2-148">FlowLog 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-149">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="9a6f2-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="9a6f2-150">흐름 로그 기록을 유지할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-151">-StorageId</span><span class="sxs-lookup"><span data-stu-id="9a6f2-151">-StorageId</span></span>
<span data-ttu-id="9a6f2-152">흐름 로그를 저장 하는 데 사용 되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-153">태그</span><span class="sxs-lookup"><span data-stu-id="9a6f2-153">-Tag</span></span>
<span data-ttu-id="9a6f2-154">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9a6f2-155">-TargetResourceId</span></span>
<span data-ttu-id="9a6f2-156">흐름 로그가 적용 되는 네트워크 보안 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-157">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="9a6f2-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="9a6f2-158">TA 서비스에서 분석을 수행 하는 빈도를 결정 하는 간격 (분)입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="9a6f2-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="9a6f2-160">첨부 된 작업 영역의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-161">-확인</span><span class="sxs-lookup"><span data-stu-id="9a6f2-161">-Confirm</span></span>
<span data-ttu-id="9a6f2-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6f2-163">-WhatIf</span></span>
<span data-ttu-id="9a6f2-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a6f2-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a6f2-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6f2-166">CommonParameters</span></span>
<span data-ttu-id="9a6f2-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6f2-168">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a6f2-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6f2-169">입력</span><span class="sxs-lookup"><span data-stu-id="9a6f2-169">INPUTS</span></span>

### <span data-ttu-id="9a6f2-170">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a6f2-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9a6f2-171">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a6f2-171">System.String</span></span>

### <span data-ttu-id="9a6f2-172">Microsoft. 네트워크 모델. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9a6f2-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9a6f2-173">출력</span><span class="sxs-lookup"><span data-stu-id="9a6f2-173">OUTPUTS</span></span>

### <span data-ttu-id="9a6f2-174">Microsoft. 네트워크 모델. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9a6f2-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9a6f2-175">상속자</span><span class="sxs-lookup"><span data-stu-id="9a6f2-175">NOTES</span></span>

## <span data-ttu-id="9a6f2-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a6f2-176">RELATED LINKS</span></span>

[<span data-ttu-id="9a6f2-177">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a6f2-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9a6f2-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a6f2-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9a6f2-179">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a6f2-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9a6f2-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9a6f2-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9a6f2-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9a6f2-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9a6f2-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9a6f2-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9a6f2-183">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9a6f2-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9a6f2-184">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a6f2-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a6f2-185">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9a6f2-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9a6f2-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a6f2-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a6f2-187">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a6f2-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a6f2-188">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a6f2-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a6f2-189">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a6f2-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9a6f2-190">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9a6f2-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9a6f2-191">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9a6f2-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9a6f2-192">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a6f2-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a6f2-193">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a6f2-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a6f2-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a6f2-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a6f2-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9a6f2-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9a6f2-196">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a6f2-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a6f2-197">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a6f2-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a6f2-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9a6f2-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9a6f2-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9a6f2-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9a6f2-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9a6f2-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9a6f2-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9a6f2-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9a6f2-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9a6f2-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9a6f2-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a6f2-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="9a6f2-204">새로운 AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9a6f2-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="9a6f2-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9a6f2-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)

[<span data-ttu-id="9a6f2-206">제거-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9a6f2-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)