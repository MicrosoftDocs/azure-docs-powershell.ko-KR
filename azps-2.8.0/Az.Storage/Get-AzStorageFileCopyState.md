---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 84d4abf2e06cf647e3674bcded88211ab727f8c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874169"
---
# <span data-ttu-id="11191-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="11191-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="11191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11191-102">SYNOPSIS</span></span>
<span data-ttu-id="11191-103">복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11191-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="11191-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11191-104">SYNTAX</span></span>

### <span data-ttu-id="11191-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="11191-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="11191-106">파일</span><span class="sxs-lookup"><span data-stu-id="11191-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="11191-107">설명은</span><span class="sxs-lookup"><span data-stu-id="11191-107">DESCRIPTION</span></span>
<span data-ttu-id="11191-108">**AzStorageFileCopyState** Cmdlet은 Azure 저장소 파일 복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11191-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="11191-109">예제의</span><span class="sxs-lookup"><span data-stu-id="11191-109">EXAMPLES</span></span>

### <span data-ttu-id="11191-110">예제 1: 파일 이름으로 복사 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="11191-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="11191-111">이 명령은 지정 된 이름을 가진 파일에 대 한 복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11191-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="11191-112">변수</span><span class="sxs-lookup"><span data-stu-id="11191-112">PARAMETERS</span></span>

### <span data-ttu-id="11191-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11191-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="11191-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="11191-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="11191-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="11191-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="11191-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="11191-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="11191-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11191-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="11191-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="11191-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="11191-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11191-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="11191-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="11191-122">The default value is 10.</span></span>

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

### <span data-ttu-id="11191-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="11191-123">-Context</span></span>
<span data-ttu-id="11191-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="11191-125">컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11191-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11191-126">-DefaultProfile</span></span>
<span data-ttu-id="11191-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11191-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11191-128">-파일</span><span class="sxs-lookup"><span data-stu-id="11191-128">-File</span></span>
<span data-ttu-id="11191-129">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="11191-130">클라우드 파일을 만들거나 Get-AzStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11191-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11191-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="11191-131">-FilePath</span></span>
<span data-ttu-id="11191-132">Azure 저장소 공유에 상대적인 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11191-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="11191-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="11191-134">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="11191-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="11191-135">-ShareName</span></span>
<span data-ttu-id="11191-136">공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-136">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11191-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="11191-137">-WaitForComplete</span></span>
<span data-ttu-id="11191-138">이 cmdlet이 복사가 완료 될 때까지 대기 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11191-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="11191-139">이 매개 변수를 지정 하지 않으면이 cmdlet은 결과를 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="11191-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11191-140">CommonParameters</span></span>
<span data-ttu-id="11191-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11191-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11191-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11191-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11191-143">입력</span><span class="sxs-lookup"><span data-stu-id="11191-143">INPUTS</span></span>

### <span data-ttu-id="11191-144">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="11191-144">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="11191-145">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11191-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="11191-146">출력</span><span class="sxs-lookup"><span data-stu-id="11191-146">OUTPUTS</span></span>

### <span data-ttu-id="11191-147">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="11191-147">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="11191-148">상속자</span><span class="sxs-lookup"><span data-stu-id="11191-148">NOTES</span></span>

## <span data-ttu-id="11191-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11191-149">RELATED LINKS</span></span>

[<span data-ttu-id="11191-150">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="11191-150">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="11191-151">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="11191-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="11191-152">시작-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11191-152">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="11191-153">중지-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="11191-153">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)