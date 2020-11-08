---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033973"
---
# <span data-ttu-id="2e5e7-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="2e5e7-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="2e5e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5e7-103">전체 트리의 속성 (디스크 사용 및 Acl)을 지정 된 경로에서 출력 경로로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="2e5e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e5e7-104">SYNTAX</span></span>

### <span data-ttu-id="2e5e7-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="2e5e7-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e5e7-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="2e5e7-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5e7-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="2e5e7-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e5e7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2e5e7-108">DESCRIPTION</span></span>
<span data-ttu-id="2e5e7-109">**Export-AzDataLakeStoreChildItemProperty** 는 지정 된 디렉터리와 하위 디렉터리 및 파일에 대 한 ADLS space 사용량 또는/및 ACL 사용량을 보고 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="2e5e7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2e5e7-110">EXAMPLES</span></span>

### <span data-ttu-id="2e5e7-111">예제 1: 모든 하위 디렉터리 및 파일의 디스크 사용 및 ACL 사용량 가져오기</span><span class="sxs-lookup"><span data-stu-id="2e5e7-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="2e5e7-112">/A 아래에 있는 모든 하위 디렉터리 및 파일의 디스크 사용 및 ACL 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="2e5e7-113">IncludeFile은 파일에 대 한 사용 현황도 보고 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="2e5e7-114">예제 2: 일관성 있는 ACL이 숨겨진 모든 하위 디렉터리 및 파일에 대 한 ACL 사용 가져오기</span><span class="sxs-lookup"><span data-stu-id="2e5e7-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="2e5e7-115">/A 아래에 있는 모든 하위 디렉터리 및 파일의 ACL 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="2e5e7-116">IncludeFile은 파일에 대 한 사용 현황도 보고 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="2e5e7-117">이 경우 HideconsistentAcl 모든 자식의 acl이/a와 동일 하므로 해당 자식이 아니라/a의 Acl이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="2e5e7-118">모든 acl이 루트와 동일한 경우이 플래그는 subtree의 acl 출력을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="2e5e7-119">변수</span><span class="sxs-lookup"><span data-stu-id="2e5e7-119">PARAMETERS</span></span>

### <span data-ttu-id="2e5e7-120">-계정</span><span class="sxs-lookup"><span data-stu-id="2e5e7-120">-Account</span></span>
<span data-ttu-id="2e5e7-121">파일 시스템 작업을 실행 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="2e5e7-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="2e5e7-122">-동시성</span><span class="sxs-lookup"><span data-stu-id="2e5e7-122">-Concurrency</span></span>
<span data-ttu-id="2e5e7-123">병렬로 처리 된 파일/디렉터리 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="2e5e7-124">기본값은 시스템 사양에 따라 가장 좋은 노력으로 계산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5e7-125">-DefaultProfile</span></span>
<span data-ttu-id="2e5e7-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5e7-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="2e5e7-127">-GetAcl</span></span>
<span data-ttu-id="2e5e7-128">루트 경로에서 시작 하는 acl을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="2e5e7-129">-GetDiskUsage</span></span>
<span data-ttu-id="2e5e7-130">루트 경로에서 시작 하는 디스크 사용량을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="2e5e7-131">-HideConsistentAcl</span></span>
<span data-ttu-id="2e5e7-132">Acl이 전체 하위 트리 전체에서 동일한 경우 디렉터리 하위 트리를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="2e5e7-133">이렇게 하면 Acl이 서로 다른 경로만 쉽게 볼 수 있습니다. 예를 들어/a/b의 모든 파일 및 폴더가 같은 경우 subtreeunder/a/b를 표시 하지 않고, IncludeFiles가 설정 되지 않은 경우에는 파일에 대 한 acl을 검색 하지 않고도 일관 된 Acl을 확인할 수 없기 때문에,이에 대 한 출력/a/b을 일관성 있는 ACL columnCannot으로 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="2e5e7-134">-IncludeFile</span></span>
<span data-ttu-id="2e5e7-135">파일 수준에 통계 표시 (기본적으로 디렉터리 수준 정보만 표시 됨)</span><span class="sxs-lookup"><span data-stu-id="2e5e7-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="2e5e7-136">-MaximumDepth</span></span>
<span data-ttu-id="2e5e7-137">디스크 사용 또는 acl이 표시 될 때까지 루트 디렉터리의 최대 깊이</span><span class="sxs-lookup"><span data-stu-id="2e5e7-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2e5e7-138">-OutputPath</span></span>
<span data-ttu-id="2e5e7-139">출력 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-139">Path to output file.</span></span> <span data-ttu-id="2e5e7-140">로컬 경로 또는 Adl 경로 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="2e5e7-141">기본적으로 로컬입니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-141">By default it is local.</span></span> <span data-ttu-id="2e5e7-142">SaveToAdl가 지정 된 경우 같은 계정의 ADL 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e5e7-143">-PassThru</span></span>
<span data-ttu-id="2e5e7-144">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-145">-Path</span><span class="sxs-lookup"><span data-stu-id="2e5e7-145">-Path</span></span>
<span data-ttu-id="2e5e7-146">지정 된 Data Lake account에서 검색 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="2e5e7-147">'/Folder/file.txt ' 형식으로 된 파일 또는 폴더 일 수 있으며, 여기에서 DNS 뒤의 첫 번째 '/'는 파일 시스템의 루트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="2e5e7-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="2e5e7-148">-SaveToAdl</span></span>
<span data-ttu-id="2e5e7-149">전달 된 후에는 덤프 파일을 ADL에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="2e5e7-150">DumpFile 들으며는이 경우 ADL 경로로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e5e7-151">-확인</span><span class="sxs-lookup"><span data-stu-id="2e5e7-151">-Confirm</span></span>
<span data-ttu-id="2e5e7-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5e7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5e7-153">-WhatIf</span></span>
<span data-ttu-id="2e5e7-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5e7-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5e7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5e7-156">CommonParameters</span></span>
<span data-ttu-id="2e5e7-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5e7-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5e7-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5e7-159">입력</span><span class="sxs-lookup"><span data-stu-id="2e5e7-159">INPUTS</span></span>

### <span data-ttu-id="2e5e7-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e5e7-160">System.String</span></span>

### <span data-ttu-id="2e5e7-161">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2e5e7-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2e5e7-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2e5e7-163">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="2e5e7-163">System.Int32</span></span>

## <span data-ttu-id="2e5e7-164">출력</span><span class="sxs-lookup"><span data-stu-id="2e5e7-164">OUTPUTS</span></span>

### <span data-ttu-id="2e5e7-165">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2e5e7-165">System.Boolean</span></span>

## <span data-ttu-id="2e5e7-166">상속자</span><span class="sxs-lookup"><span data-stu-id="2e5e7-166">NOTES</span></span>

## <span data-ttu-id="2e5e7-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e5e7-167">RELATED LINKS</span></span>