---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216172"
---
# <span data-ttu-id="02fbe-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="02fbe-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="02fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="02fbe-103">작업 내에서 변환을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="02fbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02fbe-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02fbe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02fbe-105">DESCRIPTION</span></span>
<span data-ttu-id="02fbe-106">**AzStreamAnalyticsTransformation** Cmdlet은 Stream Analytics 작업 내에서 변환을 만들거나 기존 변환을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="02fbe-107">변환의 이름은에 지정 될 수 있습니다. JSON 파일 또는 명령줄</span><span class="sxs-lookup"><span data-stu-id="02fbe-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="02fbe-108">둘 다 지정 된 경우 명령줄의 name 명령은 파일의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="02fbe-109">이미 존재 하 고 Force 매개 변수를 지정 하지 않은 변환을 지정 하는 경우 cmdlet은 기존 변환을 바꿀지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="02fbe-110">*Force* 매개 변수를 지정 하 고 기존 변형 이름을 지정 하면 확인 없이 변환이 대체 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="02fbe-111">예제의</span><span class="sxs-lookup"><span data-stu-id="02fbe-111">EXAMPLES</span></span>

### <span data-ttu-id="02fbe-112">예제 1: 작업에서 변형 만들기 또는 바꾸기</span><span class="sxs-lookup"><span data-stu-id="02fbe-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="02fbe-113">이 명령은 StreamingJob 이라는 작업에서 StreamingJobTransform 이라는 변환을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="02fbe-114">기존 변환이 해당 이름으로 이미 정의 되어 있으면 cmdlet에서 해당 이름을 바꿀지 여부를 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="02fbe-115">예제 2: 작업에서 변형 바꾸기</span><span class="sxs-lookup"><span data-stu-id="02fbe-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="02fbe-116">이 명령은 확인 없이 job StreamingJob의 StreamingJobTransform 정의를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="02fbe-117">변수</span><span class="sxs-lookup"><span data-stu-id="02fbe-117">PARAMETERS</span></span>

### <span data-ttu-id="02fbe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fbe-118">-DefaultProfile</span></span>
<span data-ttu-id="02fbe-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02fbe-120">-파일</span><span class="sxs-lookup"><span data-stu-id="02fbe-120">-File</span></span>
<span data-ttu-id="02fbe-121">만들 Azure Stream Analytics 변환의 JSON 표시를 포함 하는 JSON 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="02fbe-122">-Force</span><span class="sxs-lookup"><span data-stu-id="02fbe-122">-Force</span></span>
<span data-ttu-id="02fbe-123">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02fbe-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="02fbe-124">-JobName</span></span>
<span data-ttu-id="02fbe-125">Azure Stream Analytics 변환을 만들 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="02fbe-126">-이름</span><span class="sxs-lookup"><span data-stu-id="02fbe-126">-Name</span></span>
<span data-ttu-id="02fbe-127">만들 Azure Stream Analytics 변환의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="02fbe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02fbe-128">-ResourceGroupName</span></span>
<span data-ttu-id="02fbe-129">Azure Stream Analytics 변환을 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="02fbe-130">-확인</span><span class="sxs-lookup"><span data-stu-id="02fbe-130">-Confirm</span></span>
<span data-ttu-id="02fbe-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02fbe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fbe-132">-WhatIf</span></span>
<span data-ttu-id="02fbe-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02fbe-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02fbe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fbe-135">CommonParameters</span></span>
<span data-ttu-id="02fbe-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02fbe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fbe-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02fbe-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fbe-138">입력</span><span class="sxs-lookup"><span data-stu-id="02fbe-138">INPUTS</span></span>

### <span data-ttu-id="02fbe-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02fbe-139">System.String</span></span>

## <span data-ttu-id="02fbe-140">출력</span><span class="sxs-lookup"><span data-stu-id="02fbe-140">OUTPUTS</span></span>

### <span data-ttu-id="02fbe-141">PSTransformation를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="02fbe-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="02fbe-142">상속자</span><span class="sxs-lookup"><span data-stu-id="02fbe-142">NOTES</span></span>

## <span data-ttu-id="02fbe-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02fbe-143">RELATED LINKS</span></span>

[<span data-ttu-id="02fbe-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="02fbe-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)

