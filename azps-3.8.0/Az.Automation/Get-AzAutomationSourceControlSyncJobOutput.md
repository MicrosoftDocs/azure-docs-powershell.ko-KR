---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044992"
---
# <span data-ttu-id="5af5d-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="5af5d-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="5af5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5af5d-102">SYNOPSIS</span></span>
<span data-ttu-id="5af5d-103">Azure 자동화 소스 제어 동기화 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="5af5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5af5d-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5af5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5af5d-105">DESCRIPTION</span></span>
<span data-ttu-id="5af5d-106">**AzAutomationSourceControlSyncJobOutput** Cmdlet은 Azure Automation 소스 제어 동기화 작업에 대 한 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="5af5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5af5d-107">EXAMPLES</span></span>

### <span data-ttu-id="5af5d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5af5d-108">Example 1</span></span>
<span data-ttu-id="5af5d-109">이 명령은 원본 컨트롤 VSTSNative에 대 한 id 08d6d266-27b6-463c-beea-bc48a67ace15를 사용 하 여 소스 제어 동기화 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="5af5d-110">변수</span><span class="sxs-lookup"><span data-stu-id="5af5d-110">PARAMETERS</span></span>

### <span data-ttu-id="5af5d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5af5d-111">-AutomationAccountName</span></span>
<span data-ttu-id="5af5d-112">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-112">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af5d-113">-DefaultProfile</span></span>
<span data-ttu-id="5af5d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af5d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="5af5d-115">-JobId</span></span>
<span data-ttu-id="5af5d-116">소스 제어 동기화 작업 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af5d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5af5d-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5d-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="5af5d-119">-SourceControlName</span></span>
<span data-ttu-id="5af5d-120">소스 컨트롤 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-120">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5d-121">-스트림</span><span class="sxs-lookup"><span data-stu-id="5af5d-121">-Stream</span></span>
<span data-ttu-id="5af5d-122">스트림 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-122">The stream type.</span></span>
<span data-ttu-id="5af5d-123">기본적으로 모두로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5d-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="5af5d-124">-StreamId</span></span>
<span data-ttu-id="5af5d-125">스트림 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af5d-126">CommonParameters</span></span>
<span data-ttu-id="5af5d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af5d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af5d-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af5d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af5d-129">입력</span><span class="sxs-lookup"><span data-stu-id="5af5d-129">INPUTS</span></span>

### <span data-ttu-id="5af5d-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5af5d-130">System.String</span></span>

### <span data-ttu-id="5af5d-131">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="5af5d-131">System.Guid</span></span>

### <span data-ttu-id="5af5d-132">SourceControlSyncJobStreamType-. m m.</span><span class="sxs-lookup"><span data-stu-id="5af5d-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="5af5d-133">출력</span><span class="sxs-lookup"><span data-stu-id="5af5d-133">OUTPUTS</span></span>

### <span data-ttu-id="5af5d-134">SourceControlSyncJobStream를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="5af5d-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="5af5d-135">SourceControlSyncJobStreamRecord를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="5af5d-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="5af5d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="5af5d-136">NOTES</span></span>

## <span data-ttu-id="5af5d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5af5d-137">RELATED LINKS</span></span>