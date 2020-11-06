---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 0641fdf635bce2bbb545e50ecc99a39329fabc9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529673"
---
# <span data-ttu-id="33406-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="33406-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="33406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33406-102">SYNOPSIS</span></span>
<span data-ttu-id="33406-103">파일의 내용을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33406-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33406-104">SYNTAX</span></span>

### <span data-ttu-id="33406-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="33406-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33406-106">공유</span><span class="sxs-lookup"><span data-stu-id="33406-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33406-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="33406-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33406-108">파일</span><span class="sxs-lookup"><span data-stu-id="33406-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33406-109">설명은</span><span class="sxs-lookup"><span data-stu-id="33406-109">DESCRIPTION</span></span>
<span data-ttu-id="33406-110">**AzureStorageFileContent** cmdlet은 파일의 콘텐츠를 다운로드 한 다음 지정 된 대상에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="33406-111">이 cmdlet은 파일의 내용을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33406-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="33406-112">예제의</span><span class="sxs-lookup"><span data-stu-id="33406-112">EXAMPLES</span></span>

### <span data-ttu-id="33406-113">예제 1: 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="33406-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="33406-114">이 명령은 파일 공유 ContosoShare06에서 현재 폴더로 ContosoWorkingFolder 폴더의 CurrentDataFile 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="33406-115">예제 2: 샘플 파일 공유 아래에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="33406-116">이 예제에서는 예제 파일 공유 아래에 있는 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="33406-117">변수</span><span class="sxs-lookup"><span data-stu-id="33406-117">PARAMETERS</span></span>

### <span data-ttu-id="33406-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="33406-118">-CheckMd5</span></span>
<span data-ttu-id="33406-119">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-120">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-121">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-122">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33406-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="33406-124">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-125">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-126">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-127">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="33406-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="33406-129">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-130">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-131">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-132">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-133">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="33406-133">-Context</span></span>
<span data-ttu-id="33406-134">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-135">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-136">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-137">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33406-138">-DefaultProfile</span></span>
<span data-ttu-id="33406-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33406-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33406-140">-대상</span><span class="sxs-lookup"><span data-stu-id="33406-140">-Destination</span></span>
<span data-ttu-id="33406-141">대상 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-141">Specifies the destination path.</span></span>
<span data-ttu-id="33406-142">이 cmdlet은이 매개 변수에서 지정 하는 위치에 파일 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="33406-143">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-144">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-145">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-146">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33406-147">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="33406-147">-Directory</span></span>
<span data-ttu-id="33406-148">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="33406-149">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일에 대 한 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33406-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="33406-150">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="33406-151">또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33406-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33406-152">-파일</span><span class="sxs-lookup"><span data-stu-id="33406-152">-File</span></span>
<span data-ttu-id="33406-153">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="33406-154">이 cmdlet은이 매개 변수에서 지정 하는 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33406-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="33406-155">**Cloudfile** 개체를 얻으려면 Get-AzureStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33406-156">-Force</span><span class="sxs-lookup"><span data-stu-id="33406-156">-Force</span></span>
<span data-ttu-id="33406-157">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-158">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-159">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-160">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33406-161">-PassThru</span></span>
<span data-ttu-id="33406-162">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-163">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-164">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-165">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-166">-Path</span><span class="sxs-lookup"><span data-stu-id="33406-166">-Path</span></span>
<span data-ttu-id="33406-167">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-167">Specifies the path of a file.</span></span>
<span data-ttu-id="33406-168">이 cmdlet은이 매개 변수에서 지정 하는 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33406-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="33406-169">파일이 없는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="33406-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33406-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="33406-171">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="33406-172">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="33406-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="33406-173">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33406-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="33406-174">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="33406-175">-공유</span><span class="sxs-lookup"><span data-stu-id="33406-175">-Share</span></span>
<span data-ttu-id="33406-176">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="33406-177">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="33406-178">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="33406-179">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-179">This object contains the storage context.</span></span>
<span data-ttu-id="33406-180">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="33406-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33406-181">-ShareName</span><span class="sxs-lookup"><span data-stu-id="33406-181">-ShareName</span></span>
<span data-ttu-id="33406-182">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="33406-183">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="33406-184">-확인</span><span class="sxs-lookup"><span data-stu-id="33406-184">-Confirm</span></span>
<span data-ttu-id="33406-185">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33406-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33406-186">-WhatIf</span></span>
<span data-ttu-id="33406-187">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33406-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33406-188">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33406-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33406-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33406-189">CommonParameters</span></span>
<span data-ttu-id="33406-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33406-191">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33406-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33406-192">입력</span><span class="sxs-lookup"><span data-stu-id="33406-192">INPUTS</span></span>

### <span data-ttu-id="33406-193">WindowsAzure 파일. c a c 공유</span><span class="sxs-lookup"><span data-stu-id="33406-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="33406-194">매개 변수: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33406-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="33406-195">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="33406-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="33406-196">매개 변수: Directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33406-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="33406-197">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="33406-198">매개 변수: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33406-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="33406-199">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="33406-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="33406-200">출력</span><span class="sxs-lookup"><span data-stu-id="33406-200">OUTPUTS</span></span>

### <span data-ttu-id="33406-201">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="33406-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="33406-202">상속자</span><span class="sxs-lookup"><span data-stu-id="33406-202">NOTES</span></span>

## <span data-ttu-id="33406-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33406-203">RELATED LINKS</span></span>

[<span data-ttu-id="33406-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="33406-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="33406-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="33406-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)

