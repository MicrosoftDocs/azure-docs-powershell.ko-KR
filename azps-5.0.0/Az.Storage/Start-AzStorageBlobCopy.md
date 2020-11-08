---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215746"
---
# <span data-ttu-id="8af96-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8af96-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="8af96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af96-102">SYNOPSIS</span></span>
<span data-ttu-id="8af96-103">Blob 복사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="8af96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8af96-104">SYNTAX</span></span>

### <span data-ttu-id="8af96-105">ContainerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8af96-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8af96-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="8af96-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8af96-107">Blobinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="8af96-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8af96-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8af96-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8af96-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="8af96-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af96-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="8af96-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af96-111">해당 인스턴스</span><span class="sxs-lookup"><span data-stu-id="8af96-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af96-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="8af96-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af96-113">Fileinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="8af96-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8af96-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="8af96-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af96-115">설명은</span><span class="sxs-lookup"><span data-stu-id="8af96-115">DESCRIPTION</span></span>
<span data-ttu-id="8af96-116">**AzStorageBlobCopy** cmdlet을 시작 하 여 blob을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="8af96-117">예제의</span><span class="sxs-lookup"><span data-stu-id="8af96-117">EXAMPLES</span></span>

### <span data-ttu-id="8af96-118">예제 1: 명명 된 blob 복사</span><span class="sxs-lookup"><span data-stu-id="8af96-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="8af96-119">이 명령은 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob의 복사 작업을 ContosoArchives 이라는 컨테이너에 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="8af96-120">예제 2: 복사할 blob을 지정 하는 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="8af96-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="8af96-121">이 명령은 **AzStorageContainer** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 컨테이너를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8af96-122">해당 cmdlet은 ContosoPlanning2015 이라는 blob의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="8af96-123">이전 cmdlet은 원본 컨테이너를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="8af96-124">*Destcontainer* 매개 변수는 ContosoArchives를 대상 컨테이너로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="8af96-125">예제 3: 컨테이너의 모든 blob 가져오기 및 복사</span><span class="sxs-lookup"><span data-stu-id="8af96-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="8af96-126">이 명령은 **AzStorageBlob** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너의 blob을 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 결과를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8af96-127">해당 cmdlet은 ContosoArchives 이라는 컨테이너에 대 한 blob의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="8af96-128">예제 4: 개체로 지정 된 blob 복사</span><span class="sxs-lookup"><span data-stu-id="8af96-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="8af96-129">첫 번째 명령은 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="8af96-130">명령이 $SrcBlob 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="8af96-131">두 번째 명령은 ContosoArchives 이라는 컨테이너에서 ContosoPlanning2015Archived 라는 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="8af96-132">명령이 $DestBlob 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="8af96-133">마지막 명령은 원본 컨테이너에서 대상 컨테이너로 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="8af96-134">명령에서는 표준 점 표기법을 사용 하 여 $SrcBlob 및 $DestBlob blob에 대 한 **ICloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="8af96-135">예제 5: URI에서 blob 복사</span><span class="sxs-lookup"><span data-stu-id="8af96-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="8af96-136">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 키를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="8af96-137">두 번째 명령은 지정 된 URI의 파일을 ContosoArchive 이라는 컨테이너에 있는 ContosoPlanning 이라는 blob에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="8af96-138">이 명령은 $Context에 저장 된 대상 컨텍스트에 대 한 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="8af96-139">원본 저장소 컨텍스트가 없으므로 원본 Uri에 원본 개체에 대 한 액세스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="8af96-140">예: 소스가 없음 공용 Azure blob 인 경우 Uri에는 blob에 대 한 읽기 권한이 있는 SAS 토큰이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="8af96-141">예제 6: 블록 blob을 새 blob 이름으로 대상 컨테이너에 복사 하 고 대상 blob StandardBlobTier Hot로 RehydratePriority를 높게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="8af96-142">이 명령은 블록 blob의 복사 작업을 새 blob 이름으로 대상 컨테이너로 시작 하 고, 대상 blob StandardBlobTier Hot로 RehydratePriority를 높게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="8af96-143">변수</span><span class="sxs-lookup"><span data-stu-id="8af96-143">PARAMETERS</span></span>

### <span data-ttu-id="8af96-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="8af96-144">-AbsoluteUri</span></span>
<span data-ttu-id="8af96-145">Azure Storage blob에 복사할 파일의 절대 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="8af96-146">-BlobBaseClient</span></span>
<span data-ttu-id="8af96-147">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="8af96-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8af96-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8af96-149">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8af96-150">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8af96-151">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8af96-152">-CloudBlob</span></span>
<span data-ttu-id="8af96-153">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8af96-154">**CloudBlob** 개체를 가져오려면 Get-AzStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8af96-155">-CloudBlobContainer</span></span>
<span data-ttu-id="8af96-156">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8af96-157">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에서 blob을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="8af96-158">**CloudBlobContainer** 개체를 가져오려면 Get-AzStorageContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8af96-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8af96-160">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8af96-161">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8af96-162">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8af96-163">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8af96-164">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-164">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-165">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8af96-165">-Context</span></span>
<span data-ttu-id="8af96-166">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8af96-167">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af96-168">-DefaultProfile</span></span>
<span data-ttu-id="8af96-169">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="8af96-170">-DestBlob</span></span>
<span data-ttu-id="8af96-171">대상 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="8af96-172">-DestCloudBlob</span></span>
<span data-ttu-id="8af96-173">대상 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="8af96-174">-DestContainer</span></span>
<span data-ttu-id="8af96-175">대상 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-176">DestContext</span><span class="sxs-lookup"><span data-stu-id="8af96-176">-DestContext</span></span>
<span data-ttu-id="8af96-177">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8af96-178">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-179">-Force</span><span class="sxs-lookup"><span data-stu-id="8af96-179">-Force</span></span>
<span data-ttu-id="8af96-180">이 cmdlet이 확인 메시지를 표시 하지 않고 대상 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8af96-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="8af96-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="8af96-182">프리미엄 페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="8af96-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="8af96-183">-RehydratePriority</span></span>
<span data-ttu-id="8af96-184">Block Blob RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="8af96-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="8af96-185">보관 된 blob을 rehydrate 하는 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="8af96-186">유효한 값은 높음/표준입니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8af96-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8af96-188">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="8af96-189">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="8af96-190">-SrcBlob</span></span>
<span data-ttu-id="8af96-191">원본 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="8af96-192">-SrcContainer</span></span>
<span data-ttu-id="8af96-193">원본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-193">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="8af96-194">-SrcDir</span></span>
<span data-ttu-id="8af96-195">Azure Storage 클라이언트 라이브러리에서 **Cloudfiledirectory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="8af96-196">-SrcFile</span></span>
<span data-ttu-id="8af96-197">Azure Storage 클라이언트 라이브러리에서 **Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8af96-198">이를 만들거나 Get-AzStorageFile cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="8af96-199">-SrcFilePath</span></span>
<span data-ttu-id="8af96-200">원본 디렉터리 또는 원본 공유의 원본 파일 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="8af96-201">-SrcShare</span></span>
<span data-ttu-id="8af96-202">Azure Storage 클라이언트 라이브러리에서 **Cloudfileshare** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="8af96-203">이를 만들거나 Get-AzStorageShare cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="8af96-204">-SrcShareName</span></span>
<span data-ttu-id="8af96-205">원본 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="8af96-206">-StandardBlobTier</span></span>
<span data-ttu-id="8af96-207">Block Blob 계층, 유효한 값은 Hot/Archive입니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="8af96-208">세부 정보 참조 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="8af96-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af96-209">-확인</span><span class="sxs-lookup"><span data-stu-id="8af96-209">-Confirm</span></span>
<span data-ttu-id="8af96-210">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af96-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af96-211">-WhatIf</span></span>
<span data-ttu-id="8af96-212">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af96-213">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af96-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af96-214">CommonParameters</span></span>
<span data-ttu-id="8af96-215">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af96-216">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af96-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af96-217">입력</span><span class="sxs-lookup"><span data-stu-id="8af96-217">INPUTS</span></span>

### <span data-ttu-id="8af96-218">CloudBlob를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="8af96-219">CloudBlobContainer를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8af96-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="8af96-220">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="8af96-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="8af96-221">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8af96-221">System.String</span></span>

### <span data-ttu-id="8af96-222">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8af96-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8af96-223">출력</span><span class="sxs-lookup"><span data-stu-id="8af96-223">OUTPUTS</span></span>

### <span data-ttu-id="8af96-224">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="8af96-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="8af96-225">상속자</span><span class="sxs-lookup"><span data-stu-id="8af96-225">NOTES</span></span>

## <span data-ttu-id="8af96-226">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8af96-226">RELATED LINKS</span></span>

[<span data-ttu-id="8af96-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="8af96-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="8af96-228">중지-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8af96-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)