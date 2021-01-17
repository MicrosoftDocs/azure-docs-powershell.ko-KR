---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345866"
---
# <span data-ttu-id="5c9ab-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="5c9ab-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="5c9ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5c9ab-103">Linux 컴퓨터에서 syslog 데이터 수집을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="5c9ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c9ab-104">SYNTAX</span></span>

### <span data-ttu-id="5c9ab-105">ByWorkspaceName(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c9ab-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c9ab-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5c9ab-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c9ab-107">설명</span><span class="sxs-lookup"><span data-stu-id="5c9ab-107">DESCRIPTION</span></span>
<span data-ttu-id="5c9ab-108">**Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet은 작업 영역의 연결된 Linux 컴퓨터에서 syslog 데이터 수집을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="5c9ab-109">예제</span><span class="sxs-lookup"><span data-stu-id="5c9ab-109">EXAMPLES</span></span>

## <span data-ttu-id="5c9ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c9ab-110">PARAMETERS</span></span>

### <span data-ttu-id="5c9ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c9ab-111">-DefaultProfile</span></span>
<span data-ttu-id="5c9ab-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c9ab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c9ab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c9ab-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c9ab-114">Linux 컴퓨터를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="5c9ab-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="5c9ab-115">-Workspace</span></span>
<span data-ttu-id="5c9ab-116">이 cmdlet이 작동하는 작업 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5c9ab-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5c9ab-117">-WorkspaceName</span></span>
<span data-ttu-id="5c9ab-118">이 cmdlet이 작동하는 작업 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5c9ab-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c9ab-119">-Confirm</span></span>
<span data-ttu-id="5c9ab-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c9ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c9ab-121">-WhatIf</span></span>
<span data-ttu-id="5c9ab-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c9ab-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c9ab-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c9ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c9ab-124">CommonParameters</span></span>
<span data-ttu-id="5c9ab-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c9ab-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5c9ab-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c9ab-127">입력</span><span class="sxs-lookup"><span data-stu-id="5c9ab-127">INPUTS</span></span>

### <span data-ttu-id="5c9ab-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c9ab-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5c9ab-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5c9ab-129">System.String</span></span>

## <span data-ttu-id="5c9ab-130">출력</span><span class="sxs-lookup"><span data-stu-id="5c9ab-130">OUTPUTS</span></span>

### <span data-ttu-id="5c9ab-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5c9ab-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5c9ab-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c9ab-132">NOTES</span></span>
* <span data-ttu-id="5c9ab-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 운영, 인사이트</span><span class="sxs-lookup"><span data-stu-id="5c9ab-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5c9ab-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c9ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c9ab-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="5c9ab-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="5c9ab-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="5c9ab-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

