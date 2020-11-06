---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d16b59ed089c4756cc83363f645bdd7c47bb7f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531576"
---
# <span data-ttu-id="4fec8-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4fec8-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="4fec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fec8-102">SYNOPSIS</span></span>
<span data-ttu-id="4fec8-103">작업 입력을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fec8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fec8-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fec8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fec8-105">DESCRIPTION</span></span>
<span data-ttu-id="4fec8-106">**AzureRmStreamAnalyticsInput** Cmdlet은 Stream Analytics 작업 내에 입력을 만들거나 기존 입력을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="4fec8-107">입력 이름은 JSON 파일 또는 명령줄에서 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="4fec8-108">둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="4fec8-109">이미 존재 하 고 *Force* 매개 변수를 지정 하지 않은 입력을 지정 하는 경우 cmdlet은 기존 입력을 바꿀지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="4fec8-110">*Force* 매개 변수를 지정 하 고 기존 입력 이름을 지정 하면 입력이 확인 없이 바뀝니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="4fec8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4fec8-111">EXAMPLES</span></span>

### <span data-ttu-id="4fec8-112">예제 1: 파일의 정의를 사용 하 여 작업 입력 만들기</span><span class="sxs-lookup"><span data-stu-id="4fec8-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="4fec8-113">이 명령은 파일 Input.js에 대 한 입력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="4fec8-114">입력 정의 파일에 지정 된 이름을 사용 하는 기존 입력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="4fec8-115">예제 2: 작업 입력 만들기</span><span class="sxs-lookup"><span data-stu-id="4fec8-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="4fec8-116">이 명령은 EntryStream 이라는 작업에 새 입력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="4fec8-117">이 이름을 사용 하는 기존 입력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="4fec8-118">예제 3: 작업 입력을 파일의 정의로 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4fec8-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="4fec8-119">이 명령은 확인 하지 않고 파일의 정의를 사용 하 여 EntryStream 이라는 기존 입력 원본의 정의를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="4fec8-120">변수</span><span class="sxs-lookup"><span data-stu-id="4fec8-120">PARAMETERS</span></span>

### <span data-ttu-id="4fec8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fec8-121">-DefaultProfile</span></span>
<span data-ttu-id="4fec8-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fec8-123">-파일</span><span class="sxs-lookup"><span data-stu-id="4fec8-123">-File</span></span>
<span data-ttu-id="4fec8-124">만들 Azure Stream Analytics 입력의 JSON 표현을 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4fec8-125">-Force</span></span>
<span data-ttu-id="4fec8-126">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="4fec8-127">-JobName</span></span>
<span data-ttu-id="4fec8-128">Azure Stream Analytics 입력을 만들 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-129">-이름</span><span class="sxs-lookup"><span data-stu-id="4fec8-129">-Name</span></span>
<span data-ttu-id="4fec8-130">만들 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fec8-131">-ResourceGroupName</span></span>
<span data-ttu-id="4fec8-132">Azure 스트리밍 입력을 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-133">-확인</span><span class="sxs-lookup"><span data-stu-id="4fec8-133">-Confirm</span></span>
<span data-ttu-id="4fec8-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fec8-135">-WhatIf</span></span>
<span data-ttu-id="4fec8-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fec8-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fec8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fec8-138">CommonParameters</span></span>
<span data-ttu-id="4fec8-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fec8-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fec8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fec8-141">입력</span><span class="sxs-lookup"><span data-stu-id="4fec8-141">INPUTS</span></span>

### <span data-ttu-id="4fec8-142">않아야</span><span class="sxs-lookup"><span data-stu-id="4fec8-142">None</span></span>
<span data-ttu-id="4fec8-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fec8-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fec8-144">출력</span><span class="sxs-lookup"><span data-stu-id="4fec8-144">OUTPUTS</span></span>

### <span data-ttu-id="4fec8-145">Microsoft. StreamAnalytics. PSInput</span><span class="sxs-lookup"><span data-stu-id="4fec8-145">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="4fec8-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4fec8-146">NOTES</span></span>

## <span data-ttu-id="4fec8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fec8-147">RELATED LINKS</span></span>

[<span data-ttu-id="4fec8-148">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4fec8-148">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="4fec8-149">제거-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4fec8-149">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="4fec8-150">테스트-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4fec8-150">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)

