---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215806"
---
# <span data-ttu-id="1f3a5-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="1f3a5-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="1f3a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3a5-103">파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-103">Deletes a file.</span></span>

## <span data-ttu-id="1f3a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f3a5-104">SYNTAX</span></span>

### <span data-ttu-id="1f3a5-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f3a5-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f3a5-106">공유</span><span class="sxs-lookup"><span data-stu-id="1f3a5-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f3a5-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="1f3a5-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f3a5-108">파일</span><span class="sxs-lookup"><span data-stu-id="1f3a5-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f3a5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1f3a5-109">DESCRIPTION</span></span>
<span data-ttu-id="1f3a5-110">**제거-AzStorageFile** cmdlet은 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="1f3a5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1f3a5-111">EXAMPLES</span></span>

### <span data-ttu-id="1f3a5-112">예제 1: 파일 공유에서 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="1f3a5-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="1f3a5-113">이 명령은 ContosoShare06 이라는 파일 공유에서 ContosoFile22 라는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="1f3a5-114">예제 2: 파일 공유 개체를 사용 하 여 파일 공유에서 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f3a5-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="1f3a5-115">이 명령은 **AzStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1f3a5-116">현재 명령은 ContosoShare06에서 ContosoFile22 라는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="1f3a5-117">변수</span><span class="sxs-lookup"><span data-stu-id="1f3a5-117">PARAMETERS</span></span>

### <span data-ttu-id="1f3a5-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f3a5-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1f3a5-119">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1f3a5-120">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1f3a5-121">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1f3a5-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1f3a5-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1f3a5-123">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1f3a5-124">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1f3a5-125">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1f3a5-126">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1f3a5-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-127">The default value is 10.</span></span>

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

### <span data-ttu-id="1f3a5-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1f3a5-128">-Context</span></span>
<span data-ttu-id="1f3a5-129">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1f3a5-130">저장소 컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="1f3a5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3a5-131">-DefaultProfile</span></span>
<span data-ttu-id="1f3a5-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f3a5-133">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="1f3a5-133">-Directory</span></span>
<span data-ttu-id="1f3a5-134">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="1f3a5-135">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a5-136">-파일</span><span class="sxs-lookup"><span data-stu-id="1f3a5-136">-File</span></span>
<span data-ttu-id="1f3a5-137">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="1f3a5-138">이 cmdlet은이 매개 변수에서 지정 하는 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="1f3a5-139">**Cloudfile** 개체를 얻으려면 Get-AzStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f3a5-140">-PassThru</span></span>
<span data-ttu-id="1f3a5-141">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1f3a5-142">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1f3a5-143">-Path</span><span class="sxs-lookup"><span data-stu-id="1f3a5-143">-Path</span></span>
<span data-ttu-id="1f3a5-144">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-144">Specifies the path of a file.</span></span>
<span data-ttu-id="1f3a5-145">이 cmdlet은이 매개 변수에서 지정 하는 파일을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a5-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1f3a5-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1f3a5-147">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1f3a5-148">-공유</span><span class="sxs-lookup"><span data-stu-id="1f3a5-148">-Share</span></span>
<span data-ttu-id="1f3a5-149">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1f3a5-150">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="1f3a5-151">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="1f3a5-152">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-152">This object contains the storage context.</span></span>
<span data-ttu-id="1f3a5-153">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a5-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="1f3a5-154">-ShareName</span></span>
<span data-ttu-id="1f3a5-155">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="1f3a5-156">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="1f3a5-157">-확인</span><span class="sxs-lookup"><span data-stu-id="1f3a5-157">-Confirm</span></span>
<span data-ttu-id="1f3a5-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f3a5-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f3a5-159">-WhatIf</span></span>
<span data-ttu-id="1f3a5-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f3a5-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f3a5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3a5-162">CommonParameters</span></span>
<span data-ttu-id="1f3a5-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3a5-164">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f3a5-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3a5-165">입력</span><span class="sxs-lookup"><span data-stu-id="1f3a5-165">INPUTS</span></span>

### <span data-ttu-id="1f3a5-166">Microsoft. c m m. c a c 파일 공유</span><span class="sxs-lookup"><span data-stu-id="1f3a5-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="1f3a5-167">Microsoft. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="1f3a5-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="1f3a5-168">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="1f3a5-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="1f3a5-169">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f3a5-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1f3a5-170">출력</span><span class="sxs-lookup"><span data-stu-id="1f3a5-170">OUTPUTS</span></span>

### <span data-ttu-id="1f3a5-171">WindowsAzure. ResourceModel를 AzureStorageFile로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3a5-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="1f3a5-172">상속자</span><span class="sxs-lookup"><span data-stu-id="1f3a5-172">NOTES</span></span>

## <span data-ttu-id="1f3a5-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f3a5-173">RELATED LINKS</span></span>

[<span data-ttu-id="1f3a5-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="1f3a5-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="1f3a5-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1f3a5-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="1f3a5-176">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1f3a5-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)