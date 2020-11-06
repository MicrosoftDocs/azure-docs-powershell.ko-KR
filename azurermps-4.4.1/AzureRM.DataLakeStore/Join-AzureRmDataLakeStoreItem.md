---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533092"
---
# <span data-ttu-id="f44cd-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f44cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f44cd-102">SYNOPSIS</span></span>
<span data-ttu-id="f44cd-103">하나 이상의 파일을 조인 하 여 Data Lake Store에 하나의 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f44cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f44cd-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f44cd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f44cd-105">DESCRIPTION</span></span>
<span data-ttu-id="f44cd-106">AzureRmDataLakeStoreItem cmdlet은 하나 이상의 파일을 **연결** 하 여 Data Lake store에 하나의 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="f44cd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f44cd-107">EXAMPLES</span></span>

### <span data-ttu-id="f44cd-108">예제 1: 두 항목 연결</span><span class="sxs-lookup"><span data-stu-id="f44cd-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="f44cd-109">이 명령은 File01.txt를 결합 하 고 File02.txt CombinedFile.txt 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="f44cd-110">변수</span><span class="sxs-lookup"><span data-stu-id="f44cd-110">PARAMETERS</span></span>

### <span data-ttu-id="f44cd-111">-계정</span><span class="sxs-lookup"><span data-stu-id="f44cd-111">-Account</span></span>
<span data-ttu-id="f44cd-112">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f44cd-113">-대상</span><span class="sxs-lookup"><span data-stu-id="f44cd-113">-Destination</span></span>
<span data-ttu-id="f44cd-114">루트 디렉터리 (/)부터 시작 하 여 조인 된 항목에 대 한 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44cd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f44cd-115">-Force</span></span>
<span data-ttu-id="f44cd-116">이 작업이 이미 있는 경우 대상 파일을 덮어쓸 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44cd-117">-경로</span><span class="sxs-lookup"><span data-stu-id="f44cd-117">-Paths</span></span>
<span data-ttu-id="f44cd-118">루트 디렉터리 (/)로 시작 하 여 결합할 파일의 Data Lake Store 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44cd-119">-확인</span><span class="sxs-lookup"><span data-stu-id="f44cd-119">-Confirm</span></span>
<span data-ttu-id="f44cd-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f44cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f44cd-121">-WhatIf</span></span>
<span data-ttu-id="f44cd-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f44cd-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f44cd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44cd-124">-DefaultProfile</span></span>
<span data-ttu-id="f44cd-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f44cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44cd-126">CommonParameters</span></span>
<span data-ttu-id="f44cd-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44cd-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44cd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44cd-129">입력</span><span class="sxs-lookup"><span data-stu-id="f44cd-129">INPUTS</span></span>

## <span data-ttu-id="f44cd-130">출력</span><span class="sxs-lookup"><span data-stu-id="f44cd-130">OUTPUTS</span></span>

### <span data-ttu-id="f44cd-131">이름</span><span class="sxs-lookup"><span data-stu-id="f44cd-131">string</span></span>
<span data-ttu-id="f44cd-132">조인 된 파일의 결과 파일에 대 한 전체 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f44cd-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="f44cd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f44cd-133">NOTES</span></span>

## <span data-ttu-id="f44cd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f44cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="f44cd-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f44cd-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f44cd-137">가져오기-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f44cd-138">새로운 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f44cd-139">제거-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f44cd-140">테스트-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f44cd-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)

