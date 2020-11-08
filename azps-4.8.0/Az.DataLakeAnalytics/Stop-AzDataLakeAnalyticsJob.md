---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204607"
---
# <span data-ttu-id="bcefc-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bcefc-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="bcefc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcefc-102">SYNOPSIS</span></span>
<span data-ttu-id="bcefc-103">작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-103">Cancels a job.</span></span>

## <span data-ttu-id="bcefc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bcefc-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcefc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bcefc-105">DESCRIPTION</span></span>
<span data-ttu-id="bcefc-106">**AzDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake 분석 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="bcefc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bcefc-107">EXAMPLES</span></span>

### <span data-ttu-id="bcefc-108">예제 1: 작업 취소</span><span class="sxs-lookup"><span data-stu-id="bcefc-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="bcefc-109">이 명령은 지정 된 ID의 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="bcefc-110">변수</span><span class="sxs-lookup"><span data-stu-id="bcefc-110">PARAMETERS</span></span>

### <span data-ttu-id="bcefc-111">-계정</span><span class="sxs-lookup"><span data-stu-id="bcefc-111">-Account</span></span>
<span data-ttu-id="bcefc-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcefc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcefc-113">-DefaultProfile</span></span>
<span data-ttu-id="bcefc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bcefc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcefc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bcefc-115">-Force</span></span>
<span data-ttu-id="bcefc-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcefc-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="bcefc-117">-JobId</span></span>
<span data-ttu-id="bcefc-118">취소할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcefc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcefc-119">-PassThru</span></span>
<span data-ttu-id="bcefc-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bcefc-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcefc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="bcefc-122">-Confirm</span></span>
<span data-ttu-id="bcefc-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcefc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcefc-124">-WhatIf</span></span>
<span data-ttu-id="bcefc-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcefc-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcefc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcefc-127">CommonParameters</span></span>
<span data-ttu-id="bcefc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcefc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcefc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcefc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcefc-130">입력</span><span class="sxs-lookup"><span data-stu-id="bcefc-130">INPUTS</span></span>

### <span data-ttu-id="bcefc-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bcefc-131">System.String</span></span>

### <span data-ttu-id="bcefc-132">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="bcefc-132">System.Guid</span></span>

### <span data-ttu-id="bcefc-133">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bcefc-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bcefc-134">출력</span><span class="sxs-lookup"><span data-stu-id="bcefc-134">OUTPUTS</span></span>

### <span data-ttu-id="bcefc-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bcefc-135">System.Boolean</span></span>

## <span data-ttu-id="bcefc-136">상속자</span><span class="sxs-lookup"><span data-stu-id="bcefc-136">NOTES</span></span>

## <span data-ttu-id="bcefc-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcefc-137">RELATED LINKS</span></span>

[<span data-ttu-id="bcefc-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bcefc-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="bcefc-139">제출-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bcefc-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="bcefc-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bcefc-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)

