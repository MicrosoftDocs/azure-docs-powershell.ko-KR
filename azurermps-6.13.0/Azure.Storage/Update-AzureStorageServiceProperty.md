---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: b78d0fe26d689719427bf09e5e521ad1dbe0f425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524763"
---
# <span data-ttu-id="04aec-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="04aec-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="04aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04aec-102">SYNOPSIS</span></span>
<span data-ttu-id="04aec-103">Azure 저장소 서비스의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04aec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04aec-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04aec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04aec-105">DESCRIPTION</span></span>
<span data-ttu-id="04aec-106">**업데이트 AzureStorageServiceProperty** Cmdlet은 Azure 저장소 서비스의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="04aec-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04aec-107">EXAMPLES</span></span>

### <span data-ttu-id="04aec-108">예제 1: Blob Service DefaultServiceVersion을 2017-04-17로 설정</span><span class="sxs-lookup"><span data-stu-id="04aec-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="04aec-109">이 명령은 DefaultServiceVersion의 Blob 서비스를 2017-04-17로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="04aec-110">변수</span><span class="sxs-lookup"><span data-stu-id="04aec-110">PARAMETERS</span></span>

### <span data-ttu-id="04aec-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="04aec-111">-Context</span></span>
<span data-ttu-id="04aec-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="04aec-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04aec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04aec-114">-DefaultProfile</span></span>
<span data-ttu-id="04aec-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04aec-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="04aec-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="04aec-117">DefaultServiceVersion은 들어오는 요청의 버전이 지정 되지 않은 경우 Blob 서비스에 대 한 요청에 사용할 기본 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="04aec-118">사용할 수 있는 값에는 버전 2008-10-27 및 최신 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="04aec-119">자세한 내용은 다음 항목을 참조 하세요. https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="04aec-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04aec-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04aec-120">-PassThru</span></span>
<span data-ttu-id="04aec-121">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="04aec-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="04aec-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="04aec-122">-ServiceType</span></span>
<span data-ttu-id="04aec-123">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-123">Specifies the storage service type.</span></span>
<span data-ttu-id="04aec-124">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="04aec-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04aec-126">블</span><span class="sxs-lookup"><span data-stu-id="04aec-126">Blob</span></span> 
- <span data-ttu-id="04aec-127">테이블로</span><span class="sxs-lookup"><span data-stu-id="04aec-127">Table</span></span>
- <span data-ttu-id="04aec-128">전담팀</span><span class="sxs-lookup"><span data-stu-id="04aec-128">Queue</span></span>
- <span data-ttu-id="04aec-129">파일</span><span class="sxs-lookup"><span data-stu-id="04aec-129">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04aec-130">-확인</span><span class="sxs-lookup"><span data-stu-id="04aec-130">-Confirm</span></span>
<span data-ttu-id="04aec-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04aec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04aec-132">-WhatIf</span></span>
<span data-ttu-id="04aec-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04aec-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04aec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04aec-135">CommonParameters</span></span>
<span data-ttu-id="04aec-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04aec-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04aec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04aec-138">입력</span><span class="sxs-lookup"><span data-stu-id="04aec-138">INPUTS</span></span>

### <span data-ttu-id="04aec-139">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04aec-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04aec-140">출력</span><span class="sxs-lookup"><span data-stu-id="04aec-140">OUTPUTS</span></span>

### <span data-ttu-id="04aec-141">WindowsAzure. ResourceModel를 PSSeriviceProperties로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04aec-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="04aec-142">상속자</span><span class="sxs-lookup"><span data-stu-id="04aec-142">NOTES</span></span>

## <span data-ttu-id="04aec-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04aec-143">RELATED LINKS</span></span>