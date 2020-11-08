---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044503"
---
# <span data-ttu-id="670ce-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="670ce-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="670ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="670ce-102">SYNOPSIS</span></span>
<span data-ttu-id="670ce-103">Windows 운영 체제를 실행 하는 컴퓨터에서 이벤트 로그를 수집 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="670ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="670ce-104">SYNTAX</span></span>

### <span data-ttu-id="670ce-105">ByWorkspaceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="670ce-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="670ce-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="670ce-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670ce-107">설명은</span><span class="sxs-lookup"><span data-stu-id="670ce-107">DESCRIPTION</span></span>
<span data-ttu-id="670ce-108">**AzOperationalInsightsWindowsEventDataSource** Cmdlet은 Azure Operational Insights에서 windows 운영 체제를 실행 하는 연결 된 컴퓨터에서 windows 이벤트 로그를 수집 하는 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="670ce-109">예제의</span><span class="sxs-lookup"><span data-stu-id="670ce-109">EXAMPLES</span></span>

### <span data-ttu-id="670ce-110">예제 1: 시스템 창 이벤트 데이터 원본 만들기</span><span class="sxs-lookup"><span data-stu-id="670ce-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="670ce-111">변수</span><span class="sxs-lookup"><span data-stu-id="670ce-111">PARAMETERS</span></span>

### <span data-ttu-id="670ce-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="670ce-112">-CollectErrors</span></span>
<span data-ttu-id="670ce-113">Operational Insights에서 오류 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-113">Indicates that Operational Insights collects error messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="670ce-114">-CollectInformation</span></span>
<span data-ttu-id="670ce-115">Operational Insights가 정보 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-115">Indicates that Operational Insights collects information messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="670ce-116">-CollectWarnings</span></span>
<span data-ttu-id="670ce-117">Operational Insights가 경고 메시지를 수집 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-117">Indicates that Operational Insights collects warning messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670ce-118">-DefaultProfile</span></span>
<span data-ttu-id="670ce-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="670ce-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="670ce-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="670ce-120">-EventLogName</span></span>
<span data-ttu-id="670ce-121">이벤트 로그의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-121">Specifies the name of the event log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-122">-Force</span><span class="sxs-lookup"><span data-stu-id="670ce-122">-Force</span></span>
<span data-ttu-id="670ce-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-124">-이름</span><span class="sxs-lookup"><span data-stu-id="670ce-124">-Name</span></span>
<span data-ttu-id="670ce-125">데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-125">Specifies a name for the data source.</span></span> <span data-ttu-id="670ce-126">이름이 Azure 포털에는 표시 되지 않으며, 모든 문자열이 고유 하기만 하는 경우 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670ce-127">-ResourceGroupName</span></span>
<span data-ttu-id="670ce-128">컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-128">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-129">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="670ce-129">-Workspace</span></span>
<span data-ttu-id="670ce-130">이 cmdlet이 작동 하는 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="670ce-131">-WorkspaceName</span></span>
<span data-ttu-id="670ce-132">이 cmdlet이 작동 하는 작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-133">-확인</span><span class="sxs-lookup"><span data-stu-id="670ce-133">-Confirm</span></span>
<span data-ttu-id="670ce-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670ce-135">-WhatIf</span></span>
<span data-ttu-id="670ce-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="670ce-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="670ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670ce-138">CommonParameters</span></span>
<span data-ttu-id="670ce-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670ce-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670ce-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670ce-141">입력</span><span class="sxs-lookup"><span data-stu-id="670ce-141">INPUTS</span></span>

### <span data-ttu-id="670ce-142">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="670ce-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="670ce-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="670ce-143">System.String</span></span>

## <span data-ttu-id="670ce-144">출력</span><span class="sxs-lookup"><span data-stu-id="670ce-144">OUTPUTS</span></span>

### <span data-ttu-id="670ce-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="670ce-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="670ce-146">상속자</span><span class="sxs-lookup"><span data-stu-id="670ce-146">NOTES</span></span>

## <span data-ttu-id="670ce-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="670ce-147">RELATED LINKS</span></span>