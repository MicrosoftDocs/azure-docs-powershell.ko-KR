---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 17a6be37e62693f3e6d6e7c9089f72771fc0a9f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525208"
---
# <span data-ttu-id="a50f7-101">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a50f7-101">Get-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="a50f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a50f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a50f7-103">Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-103">Gets information about pipelines in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a50f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a50f7-104">SYNTAX</span></span>

### <span data-ttu-id="a50f7-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a50f7-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a50f7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a50f7-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a50f7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a50f7-107">DESCRIPTION</span></span>
<span data-ttu-id="a50f7-108">**AzureRmDataFactoryPipeline** Cmdlet은 Azure Data Factory의 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-108">The **Get-AzureRmDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="a50f7-109">파이프라인의 이름을 지정 하는 경우이 cmdlet은 해당 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="a50f7-110">이름을 지정 하지 않으면이 cmdlet은 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="a50f7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a50f7-111">EXAMPLES</span></span>

### <span data-ttu-id="a50f7-112">예제 1: 모든 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a50f7-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="a50f7-113">이 명령은 WikiADF 이라는 data factory의 모든 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="a50f7-114">다음 예제 명령 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="a50f7-115">두 번째는 **DataFactory** 개체를 매개 변수로 사용 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="a50f7-116">예제 2: 특정 파이프라인에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a50f7-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="a50f7-117">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="a50f7-118">이 명령은 파이프라인 연산자를 사용 하 여 Format-List cmdlet에 해당 정보를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a50f7-119">해당 cmdlet은 결과 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="a50f7-120">자세한 내용은을 입력 `Get-Help Format-List` 하세요.</span><span class="sxs-lookup"><span data-stu-id="a50f7-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="a50f7-121">예제 3: 특정 파이프라인의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="a50f7-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="a50f7-122">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **Properties** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="a50f7-123">예제 4: 특정 파이프라인에 대 한 활동 가져오기</span><span class="sxs-lookup"><span data-stu-id="a50f7-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="a50f7-124">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **작업** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="a50f7-125">예제 5: 특정 파이프라인에 대 한 런타임 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a50f7-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="a50f7-126">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **Runtimeinfo** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="a50f7-127">예제 6: 첫 번째 활동의 입력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a50f7-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="a50f7-128">이 명령은 WikiADF 이라는 데이터 팩터리에 DPWikisample 이라는 파이프라인에 대 한 정보를 가져온 다음 표준 점 표기법을 사용 하 여 해당 파이프라인과 연결 된 **작업** 속성을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="a50f7-129">명령에 **서식 목록을** 사용 하 여 **활동** 배열의 첫 번째 요소의 **입력** 속성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="a50f7-130">변수</span><span class="sxs-lookup"><span data-stu-id="a50f7-130">PARAMETERS</span></span>

### <span data-ttu-id="a50f7-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a50f7-131">-DataFactory</span></span>
<span data-ttu-id="a50f7-132">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a50f7-133">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50f7-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a50f7-134">-DataFactoryName</span></span>
<span data-ttu-id="a50f7-135">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a50f7-136">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50f7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a50f7-137">-DefaultProfile</span></span>
<span data-ttu-id="a50f7-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a50f7-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a50f7-139">-이름</span><span class="sxs-lookup"><span data-stu-id="a50f7-139">-Name</span></span>
<span data-ttu-id="a50f7-140">정보를 가져올 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50f7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a50f7-141">-ResourceGroupName</span></span>
<span data-ttu-id="a50f7-142">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a50f7-143">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 파이프라인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a50f7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a50f7-144">CommonParameters</span></span>
<span data-ttu-id="a50f7-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a50f7-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a50f7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a50f7-147">입력</span><span class="sxs-lookup"><span data-stu-id="a50f7-147">INPUTS</span></span>

### <span data-ttu-id="a50f7-148">않아야</span><span class="sxs-lookup"><span data-stu-id="a50f7-148">None</span></span>
<span data-ttu-id="a50f7-149">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a50f7-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a50f7-150">출력</span><span class="sxs-lookup"><span data-stu-id="a50f7-150">OUTPUTS</span></span>

### <span data-ttu-id="a50f7-151">System.webserver. List ' 1 [[WindowsAzure. PSPipeline, Microsoft WindowsAzure. 유틸리티, Version = 0.8.2.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. 유틸리티. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a50f7-151">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSPipeline, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="a50f7-152">상속자</span><span class="sxs-lookup"><span data-stu-id="a50f7-152">NOTES</span></span>
* <span data-ttu-id="a50f7-153">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="a50f7-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a50f7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a50f7-154">RELATED LINKS</span></span>

[<span data-ttu-id="a50f7-155">새로운 AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a50f7-155">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a50f7-156">제거-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a50f7-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a50f7-157">이력서-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a50f7-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="a50f7-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a50f7-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="a50f7-159">일시 중단-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a50f7-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)

