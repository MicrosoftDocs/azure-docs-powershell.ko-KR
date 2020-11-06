---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: dc4630359070e627a3c65c63f21c23f987cb9a31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530367"
---
# <span data-ttu-id="3beff-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3beff-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="3beff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3beff-102">SYNOPSIS</span></span>
<span data-ttu-id="3beff-103">데이터 팩터리에 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3beff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3beff-104">SYNTAX</span></span>

### <span data-ttu-id="3beff-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3beff-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3beff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3beff-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3beff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3beff-107">DESCRIPTION</span></span>
<span data-ttu-id="3beff-108">**AzureRmDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="3beff-109">이미 존재 하는 트리거의 이름을 지정 하면 cmdlet에서 트리거를 바꾸기 전에 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="3beff-110">_Force_ 매개 변수를 지정 하면 cmdlet은 확인 메시지를 표시 하지 않고 기존 트리거를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="3beff-111">트리거는 ' 중지 됨 ' 상태에서 만들어지고,이는 자신이 참조 하는 파이프라인 호출을 즉시 시작 하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="3beff-112">예제의</span><span class="sxs-lookup"><span data-stu-id="3beff-112">EXAMPLES</span></span>

### <span data-ttu-id="3beff-113">예제 1: 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="3beff-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="3beff-114">"WikiADF" 데이터 팩터리에 "ScheduledTrigger" 라는 새 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="3beff-115">트리거가 ' 중지 됨 ' 상태에 만들어지고,이는 즉시 시작 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="3beff-116">트리거는 cmdlet을 사용 하 여 시작할 수 있습니다 `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="3beff-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="3beff-117">변수</span><span class="sxs-lookup"><span data-stu-id="3beff-117">PARAMETERS</span></span>

### <span data-ttu-id="3beff-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3beff-118">-DataFactoryName</span></span>
<span data-ttu-id="3beff-119">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-119">The data factory name.</span></span>

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

### <span data-ttu-id="3beff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3beff-120">-DefaultProfile</span></span>
<span data-ttu-id="3beff-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3beff-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3beff-122">-DefinitionFile</span></span>
<span data-ttu-id="3beff-123">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-123">The JSON file path.</span></span>

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

### <span data-ttu-id="3beff-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3beff-124">-Force</span></span>
<span data-ttu-id="3beff-125">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3beff-126">-이름</span><span class="sxs-lookup"><span data-stu-id="3beff-126">-Name</span></span>
<span data-ttu-id="3beff-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3beff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3beff-128">-ResourceGroupName</span></span>
<span data-ttu-id="3beff-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-129">The resource group name.</span></span>

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

### <span data-ttu-id="3beff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3beff-130">-ResourceId</span></span>
<span data-ttu-id="3beff-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3beff-132">-확인</span><span class="sxs-lookup"><span data-stu-id="3beff-132">-Confirm</span></span>
<span data-ttu-id="3beff-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3beff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3beff-134">-WhatIf</span></span>
<span data-ttu-id="3beff-135">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3beff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3beff-136">CommonParameters</span></span>
<span data-ttu-id="3beff-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3beff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3beff-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3beff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3beff-139">입력</span><span class="sxs-lookup"><span data-stu-id="3beff-139">INPUTS</span></span>

### <span data-ttu-id="3beff-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3beff-140">System.String</span></span>

## <span data-ttu-id="3beff-141">출력</span><span class="sxs-lookup"><span data-stu-id="3beff-141">OUTPUTS</span></span>

### <span data-ttu-id="3beff-142">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="3beff-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="3beff-143">상속자</span><span class="sxs-lookup"><span data-stu-id="3beff-143">NOTES</span></span>

## <span data-ttu-id="3beff-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3beff-144">RELATED LINKS</span></span>

[<span data-ttu-id="3beff-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3beff-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3beff-146">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3beff-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3beff-147">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3beff-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="3beff-148">제거-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="3beff-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()