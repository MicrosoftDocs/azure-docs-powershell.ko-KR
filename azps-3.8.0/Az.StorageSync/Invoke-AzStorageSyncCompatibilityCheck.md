---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043131"
---
# <span data-ttu-id="b12e2-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="b12e2-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="b12e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b12e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b12e2-103">시스템 및 Azure 파일 동기화 간에 발생할 수 있는 호환성 문제가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="b12e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b12e2-104">SYNTAX</span></span>

### <span data-ttu-id="b12e2-105">PathBased (기본값)</span><span class="sxs-lookup"><span data-stu-id="b12e2-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="b12e2-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="b12e2-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="b12e2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b12e2-107">DESCRIPTION</span></span>
<span data-ttu-id="b12e2-108">**AzStorageSyncCompatibilityCheck** cmdlet은 시스템 및 Azure 파일 동기화 간에 발생할 수 있는 잠재적인 호환성 문제를 검사 합니다. 로컬 또는 원격 경로를 지정 하면 시스템 및 파일 네임 스페이스에 대 한 유효성 검사 집합을 수행한 다음 발견 되는 호환성 문제를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="b12e2-109">시스템 검사:</span><span class="sxs-lookup"><span data-stu-id="b12e2-109">System checks:</span></span>
- <span data-ttu-id="b12e2-110">OS 호환성 파일 네임 스페이스 검사:</span><span class="sxs-lookup"><span data-stu-id="b12e2-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="b12e2-111">지원 되지 않는 문자</span><span class="sxs-lookup"><span data-stu-id="b12e2-111">Unsupported characters</span></span>
- <span data-ttu-id="b12e2-112">최대 파일 크기</span><span class="sxs-lookup"><span data-stu-id="b12e2-112">Maximum file size</span></span>
- <span data-ttu-id="b12e2-113">최대 경로 길이</span><span class="sxs-lookup"><span data-stu-id="b12e2-113">Maximum path length</span></span>
- <span data-ttu-id="b12e2-114">최대 파일 길이</span><span class="sxs-lookup"><span data-stu-id="b12e2-114">Maximum file length</span></span>
- <span data-ttu-id="b12e2-115">최대 데이터 집합 크기</span><span class="sxs-lookup"><span data-stu-id="b12e2-115">Maximum dataset size</span></span>
- <span data-ttu-id="b12e2-116">최대 디렉터리 깊이</span><span class="sxs-lookup"><span data-stu-id="b12e2-116">Maximum directory depth</span></span>

## <span data-ttu-id="b12e2-117">예제의</span><span class="sxs-lookup"><span data-stu-id="b12e2-117">EXAMPLES</span></span>

### <span data-ttu-id="b12e2-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="b12e2-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="b12e2-119">이 명령은 시스템의 호환성 및 C:\DATA. 파일 및 폴더도 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="b12e2-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="b12e2-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="b12e2-121">이 명령은 C:\DATA의 파일 및 폴더 호환성을 검사 하지만 시스템 호환성 검사를 수행 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="b12e2-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="b12e2-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="b12e2-123">이 명령은 시스템의 호환성 및 C:\DATA에서 파일 및 폴더를 검사 한 다음 결과를 CSV 파일로 서 C:\results.에 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="b12e2-124">변수</span><span class="sxs-lookup"><span data-stu-id="b12e2-124">PARAMETERS</span></span>

### <span data-ttu-id="b12e2-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="b12e2-125">-ComputerName</span></span>
<span data-ttu-id="b12e2-126">이 검사를 수행 하는 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12e2-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="b12e2-127">-Credential</span></span>
<span data-ttu-id="b12e2-128">유효성을 검사 중인 공유에 대 한 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12e2-129">-Path</span><span class="sxs-lookup"><span data-stu-id="b12e2-129">-Path</span></span>
<span data-ttu-id="b12e2-130">유효성을 검사할 공유의 UNC 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12e2-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="b12e2-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="b12e2-132">이 플래그를 설정 하 여 파일 네임 스페이스 유효성 검사를 건너뛰고 시스템 유효성 검사만 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b12e2-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="b12e2-133">-SkipSystemChecks</span></span>
<span data-ttu-id="b12e2-134">시스템 유효성 검사를 건너뛰고 파일 네임 스페이스 유효성 검사만 수행 하도록이 플래그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="b12e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12e2-135">CommonParameters</span></span>
<span data-ttu-id="b12e2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12e2-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b12e2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12e2-138">입력</span><span class="sxs-lookup"><span data-stu-id="b12e2-138">INPUTS</span></span>

### <span data-ttu-id="b12e2-139">않아야</span><span class="sxs-lookup"><span data-stu-id="b12e2-139">None</span></span>

## <span data-ttu-id="b12e2-140">출력</span><span class="sxs-lookup"><span data-stu-id="b12e2-140">OUTPUTS</span></span>

### <span data-ttu-id="b12e2-141">StorageSync. PSValidationResult를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b12e2-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="b12e2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b12e2-142">NOTES</span></span>
* <span data-ttu-id="b12e2-143">키워드: azure, Az, arm, resource, management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="b12e2-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="b12e2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b12e2-144">RELATED LINKS</span></span>