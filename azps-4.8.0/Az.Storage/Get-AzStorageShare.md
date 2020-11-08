---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: b6323cd751d25038ff6705cee45594796d782326
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048600"
---
# <span data-ttu-id="d377c-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="d377c-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="d377c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d377c-102">SYNOPSIS</span></span>
<span data-ttu-id="d377c-103">파일 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="d377c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d377c-104">SYNTAX</span></span>

### <span data-ttu-id="d377c-105">MatchingPrefix (기본값)</span><span class="sxs-lookup"><span data-stu-id="d377c-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d377c-106">만</span><span class="sxs-lookup"><span data-stu-id="d377c-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d377c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d377c-107">DESCRIPTION</span></span>
<span data-ttu-id="d377c-108">**AzStorageShare** cmdlet은 저장소 계정의 파일 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="d377c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d377c-109">EXAMPLES</span></span>

### <span data-ttu-id="d377c-110">예제 1: 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="d377c-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="d377c-111">이 명령은 ContosoShare06 이라는 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="d377c-112">예제 2: 문자열로 시작 하는 모든 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="d377c-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="d377c-113">이 명령은 Contoso로 시작 하는 이름의 모든 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="d377c-114">예제 3: 지정 된 컨텍스트에서 모든 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="d377c-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="d377c-115">첫 번째 명령은 **New AzStorageContext** cmdlet을 사용 하 여 *Local* 매개 변수를 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트 개체를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="d377c-116">두 번째 명령은 $Context에 저장 된 컨텍스트 개체에 대 한 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="d377c-117">예제 4: 특정 공유 이름 및 SnapshotTime을 사용 하 여 파일 공유 스냅숏 가져오기</span><span class="sxs-lookup"><span data-stu-id="d377c-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="d377c-118">이 명령은 특정 공유 이름 및 SnapshotTime을 사용 하 여 파일 공유 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="d377c-119">변수</span><span class="sxs-lookup"><span data-stu-id="d377c-119">PARAMETERS</span></span>

### <span data-ttu-id="d377c-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d377c-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d377c-121">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d377c-122">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d377c-123">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d377c-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d377c-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d377c-125">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d377c-126">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d377c-127">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d377c-128">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d377c-129">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-129">The default value is 10.</span></span>

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

### <span data-ttu-id="d377c-130">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d377c-130">-Context</span></span>
<span data-ttu-id="d377c-131">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d377c-132">컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d377c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d377c-133">-DefaultProfile</span></span>
<span data-ttu-id="d377c-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d377c-135">-이름</span><span class="sxs-lookup"><span data-stu-id="d377c-135">-Name</span></span>
<span data-ttu-id="d377c-136">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="d377c-137">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유를 가져오거나 존재 하지 않는 파일 공유의 이름을 지정 하는 경우 아무 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d377c-138">-접두사</span><span class="sxs-lookup"><span data-stu-id="d377c-138">-Prefix</span></span>
<span data-ttu-id="d377c-139">파일 공유에 대 한 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="d377c-140">이 cmdlet은이 매개 변수에서 지정 하는 접두사와 일치 하는 파일 공유를 가져오거나 지정 된 접두사와 일치 하는 파일 공유가 없는 경우 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d377c-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d377c-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d377c-142">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d377c-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d377c-143">-SnapshotTime</span></span>
<span data-ttu-id="d377c-144">수신할 파일 공유 스냅숏의 SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="d377c-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d377c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d377c-145">CommonParameters</span></span>
<span data-ttu-id="d377c-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d377c-147">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d377c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d377c-148">입력</span><span class="sxs-lookup"><span data-stu-id="d377c-148">INPUTS</span></span>

### <span data-ttu-id="d377c-149">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d377c-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d377c-150">출력</span><span class="sxs-lookup"><span data-stu-id="d377c-150">OUTPUTS</span></span>

### <span data-ttu-id="d377c-151">WindowsAzure. ResourceModel를 AzureStorageFileShare로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d377c-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="d377c-152">상속자</span><span class="sxs-lookup"><span data-stu-id="d377c-152">NOTES</span></span>

## <span data-ttu-id="d377c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d377c-153">RELATED LINKS</span></span>

[<span data-ttu-id="d377c-154">새로운 AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="d377c-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="d377c-155">제거-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="d377c-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)