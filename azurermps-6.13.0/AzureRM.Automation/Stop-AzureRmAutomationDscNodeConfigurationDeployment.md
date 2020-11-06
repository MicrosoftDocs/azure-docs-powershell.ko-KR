---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 466cb31bd5e05235085fbc4f9045cf201a806e11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526324"
---
# <span data-ttu-id="f3a24-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a24-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="f3a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3a24-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a24-103">자동화에서 DSC 노드 구성 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="f3a24-104">현재 배포 작업만 중지 하 고 이미 할당 된 노드 구성을 할당 취소 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3a24-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f3a24-105">SYNTAX</span></span>

### <span data-ttu-id="f3a24-106">ByJobId (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3a24-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a24-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3a24-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a24-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f3a24-108">DESCRIPTION</span></span>
<span data-ttu-id="f3a24-109">**AzureRmAutomationDscNodeConfigurationDeployment** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 노드 구성 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="f3a24-110">할당할 항목이 남아 있지만 이미 할당 된 노드를 할당 취소 하지 않는 경우 노드 그룹에 대 한 노드 구성 할당을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="f3a24-111">예약 된 작업의 등록을 취소 하려면 JobScheduleId와 함께 AzureRmAutomationScheduledRunbook를 사용 하 여 현재 예약 된 작업의 할당을 [취소](./Unregister-AzureRmAutomationScheduledRunbook.md) 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3a24-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="f3a24-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f3a24-112">EXAMPLES</span></span>

### <span data-ttu-id="f3a24-113">예제 1: 자동화에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="f3a24-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="f3a24-114">위 명령에서는 전달 된 jobId를 사용 하 여 DSC 노드 구성 배포 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="f3a24-115">변수</span><span class="sxs-lookup"><span data-stu-id="f3a24-115">PARAMETERS</span></span>

### <span data-ttu-id="f3a24-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3a24-116">-AutomationAccountName</span></span>
<span data-ttu-id="f3a24-117">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="f3a24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a24-118">-DefaultProfile</span></span>
<span data-ttu-id="f3a24-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f3a24-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a24-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f3a24-120">-Force</span></span>
<span data-ttu-id="f3a24-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="f3a24-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a24-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3a24-122">-InputObject</span></span>
<span data-ttu-id="f3a24-123">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="f3a24-123">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a24-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="f3a24-124">-JobId</span></span>
<span data-ttu-id="f3a24-125">기존 배포 작업의 작업 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a24-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3a24-126">-PassThru</span></span>
<span data-ttu-id="f3a24-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f3a24-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f3a24-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a24-129">-ResourceGroupName</span></span>
<span data-ttu-id="f3a24-130">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f3a24-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f3a24-131">-Confirm</span></span>
<span data-ttu-id="f3a24-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a24-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a24-133">-WhatIf</span></span>
<span data-ttu-id="f3a24-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a24-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a24-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a24-136">CommonParameters</span></span>
<span data-ttu-id="f3a24-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a24-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a24-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a24-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a24-139">입력</span><span class="sxs-lookup"><span data-stu-id="f3a24-139">INPUTS</span></span>

### <span data-ttu-id="f3a24-140">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="f3a24-140">System.Guid</span></span>

### <span data-ttu-id="f3a24-141">NodeConfigurationDeployment를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="f3a24-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>
<span data-ttu-id="f3a24-142">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f3a24-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f3a24-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3a24-143">System.String</span></span>

## <span data-ttu-id="f3a24-144">출력</span><span class="sxs-lookup"><span data-stu-id="f3a24-144">OUTPUTS</span></span>

### <span data-ttu-id="f3a24-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f3a24-145">System.Boolean</span></span>

## <span data-ttu-id="f3a24-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f3a24-146">NOTES</span></span>

## <span data-ttu-id="f3a24-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3a24-147">RELATED LINKS</span></span>

[<span data-ttu-id="f3a24-148">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f3a24-148">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="f3a24-149">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3a24-149">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f3a24-150">시작-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a24-150">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f3a24-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f3a24-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f3a24-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="f3a24-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)