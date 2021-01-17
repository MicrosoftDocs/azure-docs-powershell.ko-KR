---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326605"
---
# <span data-ttu-id="918ca-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="918ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="918ca-102">SYNOPSIS</span></span>
<span data-ttu-id="918ca-103">Runbook 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-103">Starts a runbook job.</span></span>

## <span data-ttu-id="918ca-104">구문</span><span class="sxs-lookup"><span data-stu-id="918ca-104">SYNTAX</span></span>

### <span data-ttu-id="918ca-105">ByAsynchronousReturnJob(기본값)</span><span class="sxs-lookup"><span data-stu-id="918ca-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="918ca-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="918ca-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="918ca-107">설명</span><span class="sxs-lookup"><span data-stu-id="918ca-107">DESCRIPTION</span></span>
<span data-ttu-id="918ca-108">**Start-AzAutomationRunbook** cmdlet은 Azure Automation Runbook 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="918ca-109">Runbook의 ID 또는 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="918ca-110">예제</span><span class="sxs-lookup"><span data-stu-id="918ca-110">EXAMPLES</span></span>

### <span data-ttu-id="918ca-111">예제 1: Runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="918ca-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="918ca-112">이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbk01이라는 Runbook에 대한 Runbook 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="918ca-113">예제 2: 매개 변수를 사용하여 Python 2 Runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="918ca-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="918ca-114">이 명령은 첫 번째 위치 매개 변수로 "ValueForPosition1"과 두 번째 위치 매개 변수로 "ValueForPosition2"를 사용하여 Contoso17이라는 Azure Automation 계정에서 RunbkPy01이라는 Python 2 Runbook에 대한 Runbook 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="918ca-115">예제 3: Runbook 작업을 시작하고 결과를 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="918ca-116">이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbk01이라는 Runbook에 대한 Runbook 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="918ca-117">이 명령은 Wait 매개 _변수를 지정합니다._</span><span class="sxs-lookup"><span data-stu-id="918ca-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="918ca-118">따라서 작업이 완료된 후 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="918ca-119">cmdlet은 결과를 위해 최대 1000초 동안 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="918ca-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="918ca-120">PARAMETERS</span></span>

### <span data-ttu-id="918ca-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="918ca-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="918ca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918ca-122">-DefaultProfile</span></span>
<span data-ttu-id="918ca-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="918ca-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="918ca-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="918ca-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="918ca-125">이 cmdlet이 작업을 중단하기 전에 작업이 완료될 때까지 대기하는 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="918ca-126">기본값은 10800 또는 3시간입니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="918ca-127">-Name</span><span class="sxs-lookup"><span data-stu-id="918ca-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="918ca-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="918ca-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="918ca-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="918ca-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="918ca-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="918ca-130">-RunOn</span></span>
<span data-ttu-id="918ca-131">Runbook을 실행할 Hybrid Worker 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="918ca-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="918ca-132">-Wait</span></span>
<span data-ttu-id="918ca-133">이 cmdlet은 작업이 완료, 일시 중단 또는 실패할 때까지 기다렸다가 Azure PowerShell에 제어를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="918ca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918ca-134">CommonParameters</span></span>
<span data-ttu-id="918ca-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="918ca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918ca-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="918ca-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918ca-137">입력</span><span class="sxs-lookup"><span data-stu-id="918ca-137">INPUTS</span></span>

### <span data-ttu-id="918ca-138">System.String</span><span class="sxs-lookup"><span data-stu-id="918ca-138">System.String</span></span>

## <span data-ttu-id="918ca-139">출력</span><span class="sxs-lookup"><span data-stu-id="918ca-139">OUTPUTS</span></span>

### <span data-ttu-id="918ca-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="918ca-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="918ca-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="918ca-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="918ca-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="918ca-142">NOTES</span></span>

## <span data-ttu-id="918ca-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="918ca-143">RELATED LINKS</span></span>

[<span data-ttu-id="918ca-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="918ca-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="918ca-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)