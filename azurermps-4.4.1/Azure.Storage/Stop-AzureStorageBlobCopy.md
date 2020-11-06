---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b3e85a3cd5e892b34368e553821e888c230dfa94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531889"
---
# <span data-ttu-id="55132-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="55132-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="55132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55132-102">SYNOPSIS</span></span>
<span data-ttu-id="55132-103">복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55132-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55132-104">SYNTAX</span></span>

### <span data-ttu-id="55132-105">NamePipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="55132-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55132-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="55132-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55132-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="55132-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55132-108">설명은</span><span class="sxs-lookup"><span data-stu-id="55132-108">DESCRIPTION</span></span>
<span data-ttu-id="55132-109">**Stop-AzureStorageBlobCopy** cmdlet은 지정 된 대상 blob에 대 한 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="55132-110">예제의</span><span class="sxs-lookup"><span data-stu-id="55132-110">EXAMPLES</span></span>

### <span data-ttu-id="55132-111">예제 1: 이름으로 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="55132-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="55132-112">이 명령은 이름으로 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="55132-113">예제 2: 파이프라인을 사용 하 여 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="55132-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="55132-114">이 명령은 **AzureStorageContainer** 에서 파이프라인의 컨테이너를 전달 하 여 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="55132-115">예제 3: 파이프라인 및 Get-AzureStorageBlob를 사용 하 여 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="55132-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="55132-116">이 예제에서는 Get-AzureStorageBlob cmdlet에서 파이프라인에 컨테이너를 전달 하 여 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="55132-117">변수</span><span class="sxs-lookup"><span data-stu-id="55132-117">PARAMETERS</span></span>

### <span data-ttu-id="55132-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="55132-118">-Blob</span></span>
<span data-ttu-id="55132-119">Blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-119">Specifies the name of the blob.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="55132-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="55132-121">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="55132-122">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="55132-123">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="55132-124">-CloudBlob</span></span>
<span data-ttu-id="55132-125">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="55132-126">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55132-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="55132-127">-CloudBlobContainer</span></span>
<span data-ttu-id="55132-128">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="55132-129">개체를 만들거나 Get-AzureStorageContainer cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55132-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55132-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="55132-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="55132-131">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="55132-132">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55132-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="55132-133">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="55132-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="55132-134">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55132-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="55132-135">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="55132-135">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-136">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="55132-136">-Container</span></span>
<span data-ttu-id="55132-137">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-137">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-138">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="55132-138">-Context</span></span>
<span data-ttu-id="55132-139">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="55132-140">New-AzureStorageContext cmdlet을 사용 하 여 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="55132-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55132-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="55132-141">-CopyId</span></span>
<span data-ttu-id="55132-142">복사본 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-142">Specifies the copy ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-143">-Force</span><span class="sxs-lookup"><span data-stu-id="55132-143">-Force</span></span>
<span data-ttu-id="55132-144">확인 메시지 없이 지정 된 blob에서 현재 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-144">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="55132-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="55132-146">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="55132-147">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-148">-확인</span><span class="sxs-lookup"><span data-stu-id="55132-148">-Confirm</span></span>
<span data-ttu-id="55132-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55132-150">-WhatIf</span></span>
<span data-ttu-id="55132-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55132-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55132-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55132-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55132-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55132-153">CommonParameters</span></span>
<span data-ttu-id="55132-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55132-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55132-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55132-156">입력</span><span class="sxs-lookup"><span data-stu-id="55132-156">INPUTS</span></span>

### <span data-ttu-id="55132-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="55132-157">IStorageContext</span></span>

<span data-ttu-id="55132-158">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="55132-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="55132-159">출력</span><span class="sxs-lookup"><span data-stu-id="55132-159">OUTPUTS</span></span>

### <span data-ttu-id="55132-160">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="55132-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="55132-161">상속자</span><span class="sxs-lookup"><span data-stu-id="55132-161">NOTES</span></span>

## <span data-ttu-id="55132-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55132-162">RELATED LINKS</span></span>

[<span data-ttu-id="55132-163">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="55132-163">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="55132-164">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="55132-164">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="55132-165">시작-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="55132-165">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="55132-166">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="55132-166">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)