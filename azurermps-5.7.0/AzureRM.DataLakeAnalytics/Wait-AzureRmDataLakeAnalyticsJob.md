---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536019"
---
# <span data-ttu-id="9a73c-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a73c-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="9a73c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a73c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a73c-103">작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a73c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a73c-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a73c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a73c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a73c-106">**AzureRmDataLakeAnalyticsJob** Cmdlet은 Azure Data Lake Analytics 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="9a73c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9a73c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a73c-108">예제 1: 작업이 완료 될 때까지 대기</span><span class="sxs-lookup"><span data-stu-id="9a73c-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="9a73c-109">다음 명령은 지정 된 ID의 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="9a73c-110">변수</span><span class="sxs-lookup"><span data-stu-id="9a73c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a73c-111">-계정</span><span class="sxs-lookup"><span data-stu-id="9a73c-111">-Account</span></span>
<span data-ttu-id="9a73c-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a73c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a73c-113">-DefaultProfile</span></span>
<span data-ttu-id="9a73c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9a73c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a73c-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="9a73c-115">-JobId</span></span>
<span data-ttu-id="9a73c-116">대기할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a73c-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="9a73c-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="9a73c-118">대기 작업을 종료 하기 전에 대기할 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a73c-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9a73c-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="9a73c-120">각 작업 상태를 확인할 때 까지의 경과 시간을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a73c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a73c-121">CommonParameters</span></span>
<span data-ttu-id="9a73c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a73c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a73c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a73c-124">입력</span><span class="sxs-lookup"><span data-stu-id="9a73c-124">INPUTS</span></span>

### <span data-ttu-id="9a73c-125">Shap</span><span class="sxs-lookup"><span data-stu-id="9a73c-125">Guid</span></span>
<span data-ttu-id="9a73c-126">' JobId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="9a73c-127">출력</span><span class="sxs-lookup"><span data-stu-id="9a73c-127">OUTPUTS</span></span>

### <span data-ttu-id="9a73c-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="9a73c-128">JobInformation</span></span>
<span data-ttu-id="9a73c-129">완료 된 작업에 대 한 최종 작업 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="9a73c-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="9a73c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="9a73c-130">NOTES</span></span>

## <span data-ttu-id="9a73c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a73c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9a73c-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a73c-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="9a73c-133">중지-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a73c-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="9a73c-134">제출-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a73c-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

