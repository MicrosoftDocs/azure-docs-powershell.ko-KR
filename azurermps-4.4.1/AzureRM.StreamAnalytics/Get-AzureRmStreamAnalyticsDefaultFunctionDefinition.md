---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 307a07254f61bcbd37127a2a4d15bb41944a3508
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529981"
---
# <span data-ttu-id="e0291-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="e0291-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="e0291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0291-102">SYNOPSIS</span></span>
<span data-ttu-id="e0291-103">Stream Analytics의 함수에 대 한 기본 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0291-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0291-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0291-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e0291-105">DESCRIPTION</span></span>
<span data-ttu-id="e0291-106">**AzureRmStreamAnalyticsDefaultFunctionDefinition** Cmdlet은 Azure Stream Analytics의 함수에 대 한 기본 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="e0291-107">기본 정의와 New-AzureRmStreamAnalyticsFunction cmdlet을 사용 하 여 함수를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="e0291-108">함수를 만들기 전에 기본 정의를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="e0291-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e0291-109">EXAMPLES</span></span>

### <span data-ttu-id="e0291-110">예제 1: Stream Analytics 함수의 기본 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="e0291-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="e0291-111">이 명령은 파일의 RetrieveDefaultDefinitionRequest.js에 지정 된 매개 변수를 사용 하 여 ScoreTweet 이라는 함수의 기본 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="e0291-112">변수</span><span class="sxs-lookup"><span data-stu-id="e0291-112">PARAMETERS</span></span>

### <span data-ttu-id="e0291-113">-파일</span><span class="sxs-lookup"><span data-stu-id="e0291-113">-File</span></span>
<span data-ttu-id="e0291-114">기본 함수 정의 검색 요청에 대 한 요청 본문의 JSON (JavaScript 개체 표기) 표현을 포함 하는 json 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-114">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="e0291-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="e0291-115">-JobName</span></span>
<span data-ttu-id="e0291-116">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="e0291-117">이 cmdlet은이 매개 변수에서 지정 하는 작업의 함수에 대 한 기본 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-117">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0291-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e0291-118">-Name</span></span>
<span data-ttu-id="e0291-119">이 cmdlet이 기본 정의를 가져오는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-119">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0291-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0291-120">-ResourceGroupName</span></span>
<span data-ttu-id="e0291-121">스트림 분석 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="e0291-122">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 함수 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-122">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0291-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0291-123">-DefaultProfile</span></span>
<span data-ttu-id="e0291-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0291-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0291-125">CommonParameters</span></span>
<span data-ttu-id="e0291-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0291-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0291-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0291-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0291-128">입력</span><span class="sxs-lookup"><span data-stu-id="e0291-128">INPUTS</span></span>

## <span data-ttu-id="e0291-129">출력</span><span class="sxs-lookup"><span data-stu-id="e0291-129">OUTPUTS</span></span>

### <span data-ttu-id="e0291-130">Microsoft. i. a i m/. a i m/. i m a 함수</span><span class="sxs-lookup"><span data-stu-id="e0291-130">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="e0291-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e0291-131">NOTES</span></span>

## <span data-ttu-id="e0291-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0291-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0291-133">새로운 AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e0291-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

