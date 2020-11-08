---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211677"
---
# <span data-ttu-id="96ebe-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="96ebe-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="96ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="96ebe-103">통합 계정 일괄 처리 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="96ebe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96ebe-104">SYNTAX</span></span>

### <span data-ttu-id="96ebe-105">ByIntegrationAccountAndParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="96ebe-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="96ebe-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="96ebe-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="96ebe-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="96ebe-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="96ebe-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="96ebe-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="96ebe-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96ebe-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="96ebe-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96ebe-114">설명은</span><span class="sxs-lookup"><span data-stu-id="96ebe-114">DESCRIPTION</span></span>
<span data-ttu-id="96ebe-115">**Set-AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정 일괄 처리 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="96ebe-116">예제의</span><span class="sxs-lookup"><span data-stu-id="96ebe-116">EXAMPLES</span></span>

### <span data-ttu-id="96ebe-117">예제 1: 로컬 파일을 사용 하 여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="96ebe-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="96ebe-118">"$BatchConfigurationFilePath"에 포함 된 파일 경로에 있는 로컬 파일을 사용 하 여 "sampleBatchConfig" 이라는 일괄 처리 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="96ebe-119">예제 2: JSON 문자열을 사용 하 여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="96ebe-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="96ebe-120">"$BatchConfigurationContent"에 포함 된 JSON 문자열을 사용 하 여 "sampleBatchConfig" 이라는 일괄 처리 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="96ebe-121">예제 3: 매개 변수를 사용 하 여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="96ebe-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="96ebe-122">필요한 모든 매개 변수를 수동으로 제공 하 여 "sampleBatchConfig" 이라는 일괄 처리 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="96ebe-123">변수</span><span class="sxs-lookup"><span data-stu-id="96ebe-123">PARAMETERS</span></span>

### <span data-ttu-id="96ebe-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="96ebe-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="96ebe-125">통합 계정 일괄 처리 구성 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="96ebe-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="96ebe-127">통합 계정 일괄 처리 구성 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="96ebe-128">-BatchGroupName</span></span>
<span data-ttu-id="96ebe-129">통합 계정 일괄 처리 구성 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="96ebe-130">-BatchSize</span></span>
<span data-ttu-id="96ebe-131">통합 계정 일괄 처리 구성 일괄 처리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ebe-132">-DefaultProfile</span></span>
<span data-ttu-id="96ebe-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96ebe-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96ebe-134">-InputObject</span></span>
<span data-ttu-id="96ebe-135">통합 계정 일괄 처리 구성.</span><span class="sxs-lookup"><span data-stu-id="96ebe-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="96ebe-136">-MessageCount</span></span>
<span data-ttu-id="96ebe-137">통합 계정 일괄 처리 구성 메시지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="96ebe-138">-Metadata</span></span>
<span data-ttu-id="96ebe-139">통합 계정 일괄 처리 구성 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-140">-이름</span><span class="sxs-lookup"><span data-stu-id="96ebe-140">-Name</span></span>
<span data-ttu-id="96ebe-141">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="96ebe-142">-ParentName</span></span>
<span data-ttu-id="96ebe-143">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96ebe-144">-ResourceGroupName</span></span>
<span data-ttu-id="96ebe-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96ebe-146">-ResourceId</span></span>
<span data-ttu-id="96ebe-147">통합 계정 일괄 처리 구성 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="96ebe-148">-ScheduleFrequency</span></span>
<span data-ttu-id="96ebe-149">통합 계정 일괄 처리 구성 일정 주파수입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="96ebe-150">-ScheduleInterval</span></span>
<span data-ttu-id="96ebe-151">통합 계정 일괄 처리 구성 일정 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="96ebe-152">-ScheduleStartTime</span></span>
<span data-ttu-id="96ebe-153">통합 계정 일괄 처리 구성 일정 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="96ebe-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="96ebe-155">통합 계정 일괄 처리 구성 일정 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="96ebe-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-156">-확인</span><span class="sxs-lookup"><span data-stu-id="96ebe-156">-Confirm</span></span>
<span data-ttu-id="96ebe-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96ebe-158">-WhatIf</span></span>
<span data-ttu-id="96ebe-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96ebe-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96ebe-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ebe-161">CommonParameters</span></span>
<span data-ttu-id="96ebe-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ebe-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ebe-163">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96ebe-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ebe-164">입력</span><span class="sxs-lookup"><span data-stu-id="96ebe-164">INPUTS</span></span>

### <span data-ttu-id="96ebe-165">LogicApp. PSIntegrationAccountBatchConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="96ebe-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="96ebe-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="96ebe-166">System.String</span></span>

## <span data-ttu-id="96ebe-167">출력</span><span class="sxs-lookup"><span data-stu-id="96ebe-167">OUTPUTS</span></span>

### <span data-ttu-id="96ebe-168">LogicApp. PSIntegrationAccountBatchConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="96ebe-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="96ebe-169">상속자</span><span class="sxs-lookup"><span data-stu-id="96ebe-169">NOTES</span></span>

## <span data-ttu-id="96ebe-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96ebe-170">RELATED LINKS</span></span>