---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056865"
---
# <span data-ttu-id="741b2-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="741b2-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="741b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741b2-102">SYNOPSIS</span></span>
<span data-ttu-id="741b2-103">Stream Analytics 작업의 출력을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="741b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="741b2-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="741b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="741b2-105">DESCRIPTION</span></span>
<span data-ttu-id="741b2-106">**AzStreamAnalyticsOutput** Cmdlet은 Stream Analytics 작업 내에 출력을 만들거나 기존 출력을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="741b2-107">출력 이름은에 지정 될 수 있습니다. JSON 파일 또는 명령줄</span><span class="sxs-lookup"><span data-stu-id="741b2-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="741b2-108">둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="741b2-109">이미 존재 하 고 *Force* 매개 변수를 지정 하지 않은 출력을 지정 하는 경우 cmdlet은 기존 출력을 바꿀지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="741b2-110">*Force* 매개 변수를 지정 하 고 기존 출력 이름을 지정 하면 출력이 확인 되지 않고 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="741b2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="741b2-111">EXAMPLES</span></span>

### <span data-ttu-id="741b2-112">예제 1: 작업에 출력 추가</span><span class="sxs-lookup"><span data-stu-id="741b2-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="741b2-113">이 명령은 StreamingJob 이라는 작업에서 출력 이라는 새 출력을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="741b2-114">이 이름을 가진 기존 출력이 이미 정의 되어 있는 경우 cmdlet은이를 바꿀 것인지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="741b2-115">예제 2: 작업 출력 정의 바꾸기</span><span class="sxs-lookup"><span data-stu-id="741b2-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="741b2-116">이 명령은 확인 하지 않고 StreamingJob 이라는 작업의 출력에 대 한 정의를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="741b2-117">변수</span><span class="sxs-lookup"><span data-stu-id="741b2-117">PARAMETERS</span></span>

### <span data-ttu-id="741b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741b2-118">-DefaultProfile</span></span>
<span data-ttu-id="741b2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="741b2-120">-파일</span><span class="sxs-lookup"><span data-stu-id="741b2-120">-File</span></span>
<span data-ttu-id="741b2-121">만들 Azure Stream Analytics 출력의 JSON 표현을 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741b2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="741b2-122">-Force</span></span>
<span data-ttu-id="741b2-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="741b2-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="741b2-124">-JobName</span></span>
<span data-ttu-id="741b2-125">Azure Stream Analytics 출력을 만들 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="741b2-126">-이름</span><span class="sxs-lookup"><span data-stu-id="741b2-126">-Name</span></span>
<span data-ttu-id="741b2-127">만들 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="741b2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741b2-128">-ResourceGroupName</span></span>
<span data-ttu-id="741b2-129">Azure Stream Analytics 출력을 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="741b2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="741b2-130">-Confirm</span></span>
<span data-ttu-id="741b2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741b2-132">-WhatIf</span></span>
<span data-ttu-id="741b2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="741b2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741b2-135">CommonParameters</span></span>
<span data-ttu-id="741b2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="741b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741b2-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="741b2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741b2-138">입력</span><span class="sxs-lookup"><span data-stu-id="741b2-138">INPUTS</span></span>

### <span data-ttu-id="741b2-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="741b2-139">System.String</span></span>

## <span data-ttu-id="741b2-140">출력</span><span class="sxs-lookup"><span data-stu-id="741b2-140">OUTPUTS</span></span>

### <span data-ttu-id="741b2-141">Microsoft. StreamAnalytics. PSOutput</span><span class="sxs-lookup"><span data-stu-id="741b2-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="741b2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="741b2-142">NOTES</span></span>

## <span data-ttu-id="741b2-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="741b2-143">RELATED LINKS</span></span>

[<span data-ttu-id="741b2-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="741b2-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="741b2-145">제거-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="741b2-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="741b2-146">테스트-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="741b2-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)

