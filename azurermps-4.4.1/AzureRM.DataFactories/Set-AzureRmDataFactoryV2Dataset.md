---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 4254a243894893e58c1c59ea19a8953ddcc8f101
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527655"
---
# <span data-ttu-id="c6788-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c6788-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="c6788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6788-102">SYNOPSIS</span></span>
<span data-ttu-id="c6788-103">Data Factory에서 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6788-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6788-104">SYNTAX</span></span>

### <span data-ttu-id="c6788-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6788-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6788-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6788-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6788-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c6788-107">DESCRIPTION</span></span>
<span data-ttu-id="c6788-108">Set-AzureRmDataFactoryV2Dataset cmdlet은 Azure Data Factory에서 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="c6788-109">이미 존재 하는 데이터 집합의 이름을 지정 하면이 cmdlet이 데이터 집합을 바꾸기 전에 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="c6788-110">Force 매개 변수를 지정 하면 cmdlet은 확인 없이 기존 데이터 집합을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="c6788-111">다음 순서 대로 이러한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="c6788-112">데이터 팩터리에 동일한 이름을 가진 데이터 집합이 이미 있는 경우이 cmdlet은 기존 데이터 집합을 새 데이터 집합으로 덮어쓸지 여부를 확인 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="c6788-113">기존 데이터 집합을 덮어쓰려고 한다는 것을 확인 하면 데이터 집합 정의도 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="c6788-114">예제의</span><span class="sxs-lookup"><span data-stu-id="c6788-114">EXAMPLES</span></span>

### <span data-ttu-id="c6788-115">예제 1: 데이터 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="c6788-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="c6788-116">이 명령은 WikiADF 이라는 data factory에 DA_WikipediaClickEvents 이라는 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="c6788-117">명령은 파일의 DAWikipediaClickEvents.js정보를 기준으로 데이터 집합을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="c6788-118">변수</span><span class="sxs-lookup"><span data-stu-id="c6788-118">PARAMETERS</span></span>

### <span data-ttu-id="c6788-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c6788-119">-Confirm</span></span>
<span data-ttu-id="c6788-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6788-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c6788-121">-DataFactoryName</span></span>
<span data-ttu-id="c6788-122">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c6788-123">이 cmdlet은이 매개 변수에서 지정 하는 데이터 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c6788-124">-DefinitionFile</span></span>
<span data-ttu-id="c6788-125">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c6788-126">-Force</span></span>
<span data-ttu-id="c6788-127">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c6788-128">-이름</span><span class="sxs-lookup"><span data-stu-id="c6788-128">-Name</span></span>
<span data-ttu-id="c6788-129">만들 데이터 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6788-130">-ResourceGroupName</span></span>
<span data-ttu-id="c6788-131">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6788-132">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 데이터 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6788-133">-ResourceId</span></span>
<span data-ttu-id="c6788-134">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-134">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6788-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6788-135">-WhatIf</span></span>
<span data-ttu-id="c6788-136">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c6788-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6788-137">-DefaultProfile</span></span>
<span data-ttu-id="c6788-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6788-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6788-139">CommonParameters</span></span>
<span data-ttu-id="c6788-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6788-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6788-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6788-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6788-142">입력</span><span class="sxs-lookup"><span data-stu-id="c6788-142">INPUTS</span></span>

### <span data-ttu-id="c6788-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6788-143">System.String</span></span>

## <span data-ttu-id="c6788-144">출력</span><span class="sxs-lookup"><span data-stu-id="c6788-144">OUTPUTS</span></span>

### <span data-ttu-id="c6788-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c6788-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="c6788-146">상속자</span><span class="sxs-lookup"><span data-stu-id="c6788-146">NOTES</span></span>
<span data-ttu-id="c6788-147">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="c6788-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c6788-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6788-148">RELATED LINKS</span></span>

[<span data-ttu-id="c6788-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c6788-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="c6788-150">제거-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c6788-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()