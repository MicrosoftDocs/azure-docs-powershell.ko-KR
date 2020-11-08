---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226059"
---
# <span data-ttu-id="dad9e-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="dad9e-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="dad9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad9e-102">SYNOPSIS</span></span>
<span data-ttu-id="dad9e-103">지정 된 경로에서 재귀적으로 ACL을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="dad9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dad9e-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dad9e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dad9e-105">DESCRIPTION</span></span>
<span data-ttu-id="dad9e-106">**AzDataLakeGen2AclRecursive** cmdlet은 지정 된 경로에서 재귀적으로 ACL을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="dad9e-107">원본 ACL에서 AccessControlType, DefaultScope 및 EntityId를 사용 하 여 입력 ACL 항목이 있는 ACL 항목 (다른 권한이 있는 경우에도) 들으며 lbe.</span><span class="sxs-lookup"><span data-stu-id="dad9e-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="dad9e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dad9e-108">EXAMPLES</span></span>

### <span data-ttu-id="dad9e-109">예제 1: 파일 시스템의 루트 directiry에서 ACL을 재귀적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="dad9e-110">이 명령은 먼저 2 개의 acl 항목이 있는 ACL 개체를 만든 다음 파일 시스템의 루트 디렉터리에서 재귀적으로 ACL을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="dad9e-111">예제 2: 디렉터리에서 재귀적으로 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="dad9e-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="dad9e-112">이 명령은 먼저 디렉터리에서 ACL을 재귀적으로 제거 하 고 실패 한 다음, 사용자가 실패 한 파일을 수정한 후 ContinuationToken를 사용 하 여 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="dad9e-113">예제 3: 청크에 재귀적으로 청크 하는 ACL 제거</span><span class="sxs-lookup"><span data-stu-id="dad9e-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="dad9e-114">이 스크립트는 청크를 기준으로 디렉터리 청크에 대 한 ACL rescursively를 제거 합니다. 청크의 크기는 BatchSize \* MaxBatchCount입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="dad9e-115">청크 크기는이 스크립트의 5만입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="dad9e-116">예제 4: 디렉터리 및 ContinueOnFailure에서 ACL을 재귀적으로 제거한 다음 실패에서 다시 한 번에 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="dad9e-117">이 명령은 먼저 ContinueOnFailure를 사용 하 여 디렉터리에 대 한 ACL을 재귀적으로 제거 하 고 일부 항목은 실패 한 다음 실패 한 항목을 하나씩 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="dad9e-118">변수</span><span class="sxs-lookup"><span data-stu-id="dad9e-118">PARAMETERS</span></span>

### <span data-ttu-id="dad9e-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="dad9e-119">-Acl</span></span>
<span data-ttu-id="dad9e-120">파일 또는 디렉터리에 대해 재귀적으로 설정할 POSIX 액세스 제어 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad9e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dad9e-121">-AsJob</span></span>
<span data-ttu-id="dad9e-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dad9e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dad9e-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="dad9e-123">-BatchSize</span></span>
<span data-ttu-id="dad9e-124">데이터 집합 크기가 일괄 처리 크기를 초과 하면 작업은 여러 요청으로 분할 되므로 진행률을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="dad9e-125">일괄 처리 크기는 1에서 2000 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="dad9e-126">기본값은 2000입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad9e-127">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dad9e-127">-Context</span></span>
<span data-ttu-id="dad9e-128">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="dad9e-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="dad9e-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="dad9e-129">-ContinuationToken</span></span>
<span data-ttu-id="dad9e-130">연속 토큰.</span><span class="sxs-lookup"><span data-stu-id="dad9e-130">Continuation Token.</span></span>

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

### <span data-ttu-id="dad9e-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="dad9e-131">-ContinueOnFailure</span></span>
<span data-ttu-id="dad9e-132">오류를 무시 하 고 디렉터리의 다른 하위 엔터티에서 작업을 계속 proceeing이 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="dad9e-133">기본 작업은 오류가 발생할 때 신속 하 게 종료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="dad9e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad9e-134">-DefaultProfile</span></span>
<span data-ttu-id="dad9e-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad9e-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="dad9e-136">-FileSystem</span></span>
<span data-ttu-id="dad9e-137">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="dad9e-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad9e-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="dad9e-138">-MaxBatchCount</span></span>
<span data-ttu-id="dad9e-139">단일 변경 액세스 제어 작업을 실행할 수 있는 최대 일괄 처리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="dad9e-140">데이터 집합 크기가 MaxBatchCount 곱하기 BatchSize를 초과 하면 연속 토큰이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad9e-141">-Path</span><span class="sxs-lookup"><span data-stu-id="dad9e-141">-Path</span></span>
<span data-ttu-id="dad9e-142">지정 된 파일 시스템에서 Acl을 재귀적으로 변경 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="dad9e-143">파일 또는 디렉터리인 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-143">Can be a file or directory.</span></span>
<span data-ttu-id="dad9e-144">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="dad9e-145">Skip이 매개 변수를 설정 하 여 파일 시스템의 루트 디렉터리에서 재귀적으로 Acl을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad9e-146">-확인</span><span class="sxs-lookup"><span data-stu-id="dad9e-146">-Confirm</span></span>
<span data-ttu-id="dad9e-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad9e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad9e-148">-WhatIf</span></span>
<span data-ttu-id="dad9e-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad9e-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad9e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad9e-151">CommonParameters</span></span>
<span data-ttu-id="dad9e-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad9e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad9e-153">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad9e-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad9e-154">입력</span><span class="sxs-lookup"><span data-stu-id="dad9e-154">INPUTS</span></span>

### <span data-ttu-id="dad9e-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dad9e-155">System.String</span></span>

### <span data-ttu-id="dad9e-156">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dad9e-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dad9e-157">출력</span><span class="sxs-lookup"><span data-stu-id="dad9e-157">OUTPUTS</span></span>

### <span data-ttu-id="dad9e-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dad9e-158">System.String</span></span>

## <span data-ttu-id="dad9e-159">상속자</span><span class="sxs-lookup"><span data-stu-id="dad9e-159">NOTES</span></span>

## <span data-ttu-id="dad9e-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dad9e-160">RELATED LINKS</span></span>