---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215032"
---
# <span data-ttu-id="f2d2c-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f2d2c-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="f2d2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d2c-103">Data Lake Analytics 계정의 데이터 원본에 대 한 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2d2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2d2c-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2d2c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="f2d2c-106">**AzDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정의 데이터 원본에 대 한 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2d2c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2d2c-107">EXAMPLES</span></span>

### <span data-ttu-id="f2d2c-108">예제 1: 데이터 원본에 대 한 선택 키 변경</span><span class="sxs-lookup"><span data-stu-id="f2d2c-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="f2d2c-109">이 명령은 Azure Blob 저장소 데이터 원본에 대해 저장 된 선택 키를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="f2d2c-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2d2c-110">PARAMETERS</span></span>

### <span data-ttu-id="f2d2c-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="f2d2c-111">-AccessKey</span></span>
<span data-ttu-id="f2d2c-112">Azure Blob 저장소 데이터 원본의 새 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="f2d2c-113">-계정</span><span class="sxs-lookup"><span data-stu-id="f2d2c-113">-Account</span></span>
<span data-ttu-id="f2d2c-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f2d2c-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="f2d2c-115">-Blob</span></span>
<span data-ttu-id="f2d2c-116">Azure Blob 저장소 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d2c-117">-DefaultProfile</span></span>
<span data-ttu-id="f2d2c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2d2c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2d2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2d2c-120">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2d2c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d2c-121">CommonParameters</span></span>
<span data-ttu-id="f2d2c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2d2c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d2c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d2c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d2c-124">입력</span><span class="sxs-lookup"><span data-stu-id="f2d2c-124">INPUTS</span></span>

### <span data-ttu-id="f2d2c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2d2c-125">System.String</span></span>

## <span data-ttu-id="f2d2c-126">출력</span><span class="sxs-lookup"><span data-stu-id="f2d2c-126">OUTPUTS</span></span>

### <span data-ttu-id="f2d2c-127">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="f2d2c-127">System.Void</span></span>

## <span data-ttu-id="f2d2c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f2d2c-128">NOTES</span></span>

## <span data-ttu-id="f2d2c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2d2c-129">RELATED LINKS</span></span>

[<span data-ttu-id="f2d2c-130">추가-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f2d2c-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="f2d2c-131">제거-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="f2d2c-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

