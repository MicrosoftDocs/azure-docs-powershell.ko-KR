---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033943"
---
# <span data-ttu-id="cb7db-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cb7db-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="cb7db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7db-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7db-103">Azure Data Factory에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="cb7db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb7db-104">SYNTAX</span></span>

### <span data-ttu-id="cb7db-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="cb7db-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb7db-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cb7db-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb7db-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cb7db-107">DESCRIPTION</span></span>
<span data-ttu-id="cb7db-108">**AzDataFactoryPipeline** Cmdlet은 Azure Data Factory에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="cb7db-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cb7db-109">EXAMPLES</span></span>

### <span data-ttu-id="cb7db-110">예제 1: 파이프라인 제거</span><span class="sxs-lookup"><span data-stu-id="cb7db-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="cb7db-111">이 cmdlet은 WikiADF 이라는 data factory에서 DPWikisample 이라는 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="cb7db-112">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="cb7db-113">변수</span><span class="sxs-lookup"><span data-stu-id="cb7db-113">PARAMETERS</span></span>

### <span data-ttu-id="cb7db-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb7db-114">-DataFactory</span></span>
<span data-ttu-id="cb7db-115">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cb7db-116">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7db-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cb7db-117">-DataFactoryName</span></span>
<span data-ttu-id="cb7db-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cb7db-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb7db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7db-120">-DefaultProfile</span></span>
<span data-ttu-id="cb7db-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cb7db-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb7db-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cb7db-122">-Force</span></span>
<span data-ttu-id="cb7db-123">이 cmdlet이 확인을 묻지 않고 파이프라인이 제거 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="cb7db-124">-이름</span><span class="sxs-lookup"><span data-stu-id="cb7db-124">-Name</span></span>
<span data-ttu-id="cb7db-125">제거할 파이프라인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb7db-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb7db-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb7db-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cb7db-128">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 파이프라인을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb7db-129">-확인</span><span class="sxs-lookup"><span data-stu-id="cb7db-129">-Confirm</span></span>
<span data-ttu-id="cb7db-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb7db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb7db-131">-WhatIf</span></span>
<span data-ttu-id="cb7db-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb7db-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb7db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7db-134">CommonParameters</span></span>
<span data-ttu-id="cb7db-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb7db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7db-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb7db-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7db-137">입력</span><span class="sxs-lookup"><span data-stu-id="cb7db-137">INPUTS</span></span>

### <span data-ttu-id="cb7db-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cb7db-138">System.String</span></span>

### <span data-ttu-id="cb7db-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cb7db-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="cb7db-140">출력</span><span class="sxs-lookup"><span data-stu-id="cb7db-140">OUTPUTS</span></span>

### <span data-ttu-id="cb7db-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="cb7db-141">System.Void</span></span>

## <span data-ttu-id="cb7db-142">상속자</span><span class="sxs-lookup"><span data-stu-id="cb7db-142">NOTES</span></span>
* <span data-ttu-id="cb7db-143">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="cb7db-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cb7db-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb7db-144">RELATED LINKS</span></span>

[<span data-ttu-id="cb7db-145">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cb7db-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="cb7db-146">새로운 AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cb7db-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="cb7db-147">이력서-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cb7db-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="cb7db-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="cb7db-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="cb7db-149">일시 중단-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="cb7db-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)

