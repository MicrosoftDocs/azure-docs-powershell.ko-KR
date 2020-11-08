---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204600"
---
# <span data-ttu-id="fa706-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="fa706-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="fa706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa706-102">SYNOPSIS</span></span>
<span data-ttu-id="fa706-103">Data Lake Store의 항목에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="fa706-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa706-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa706-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fa706-105">DESCRIPTION</span></span>
<span data-ttu-id="fa706-106">**Add-AzDataLakeStoreItemContent** Cmdlet은 Azure Data Lake store의 항목에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="fa706-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fa706-107">EXAMPLES</span></span>

### <span data-ttu-id="fa706-108">예제 1: 파일에 콘텐츠 추가</span><span class="sxs-lookup"><span data-stu-id="fa706-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="fa706-109">이 명령은 파일 myFile.txt에 콘텐츠를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="fa706-110">변수</span><span class="sxs-lookup"><span data-stu-id="fa706-110">PARAMETERS</span></span>

### <span data-ttu-id="fa706-111">-계정</span><span class="sxs-lookup"><span data-stu-id="fa706-111">-Account</span></span>
<span data-ttu-id="fa706-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fa706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa706-113">-DefaultProfile</span></span>
<span data-ttu-id="fa706-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fa706-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa706-115">-인코딩</span><span class="sxs-lookup"><span data-stu-id="fa706-115">-Encoding</span></span>
<span data-ttu-id="fa706-116">만들 항목에 대 한 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="fa706-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fa706-118">없는</span><span class="sxs-lookup"><span data-stu-id="fa706-118">Unknown</span></span>
- <span data-ttu-id="fa706-119">이름</span><span class="sxs-lookup"><span data-stu-id="fa706-119">String</span></span>
- <span data-ttu-id="fa706-120">유</span><span class="sxs-lookup"><span data-stu-id="fa706-120">Unicode</span></span>
- <span data-ttu-id="fa706-121">바이트만</span><span class="sxs-lookup"><span data-stu-id="fa706-121">Byte</span></span>
- <span data-ttu-id="fa706-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="fa706-122">BigEndianUnicode</span></span>
- <span data-ttu-id="fa706-123">F</span><span class="sxs-lookup"><span data-stu-id="fa706-123">UTF8</span></span>
- <span data-ttu-id="fa706-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="fa706-124">UTF7</span></span>
- <span data-ttu-id="fa706-125">이외의</span><span class="sxs-lookup"><span data-stu-id="fa706-125">Ascii</span></span>
- <span data-ttu-id="fa706-126">기본값</span><span class="sxs-lookup"><span data-stu-id="fa706-126">Default</span></span>
- <span data-ttu-id="fa706-127">이중</span><span class="sxs-lookup"><span data-stu-id="fa706-127">Oem</span></span>
- <span data-ttu-id="fa706-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="fa706-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa706-129">-Path</span><span class="sxs-lookup"><span data-stu-id="fa706-129">-Path</span></span>
<span data-ttu-id="fa706-130">루트 디렉터리 (/)로 시작 하 여 수정할 항목의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa706-131">-값</span><span class="sxs-lookup"><span data-stu-id="fa706-131">-Value</span></span>
<span data-ttu-id="fa706-132">항목에 추가할 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-132">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa706-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa706-133">CommonParameters</span></span>
<span data-ttu-id="fa706-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa706-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa706-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa706-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa706-136">입력</span><span class="sxs-lookup"><span data-stu-id="fa706-136">INPUTS</span></span>

### <span data-ttu-id="fa706-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fa706-137">System.String</span></span>

### <span data-ttu-id="fa706-138">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="fa706-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fa706-139">System. 개체</span><span class="sxs-lookup"><span data-stu-id="fa706-139">System.Object</span></span>

### <span data-ttu-id="fa706-140">시스템. 텍스트 인코딩</span><span class="sxs-lookup"><span data-stu-id="fa706-140">System.Text.Encoding</span></span>

## <span data-ttu-id="fa706-141">출력</span><span class="sxs-lookup"><span data-stu-id="fa706-141">OUTPUTS</span></span>

### <span data-ttu-id="fa706-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fa706-142">System.Boolean</span></span>

## <span data-ttu-id="fa706-143">상속자</span><span class="sxs-lookup"><span data-stu-id="fa706-143">NOTES</span></span>

## <span data-ttu-id="fa706-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa706-144">RELATED LINKS</span></span>

[<span data-ttu-id="fa706-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="fa706-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)

