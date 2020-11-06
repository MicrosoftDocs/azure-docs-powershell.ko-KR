---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 8525333f2be148b59053c62fc4d0f95dda8949a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532307"
---
# <span data-ttu-id="1f3ee-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="1f3ee-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="1f3ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3ee-103">Azure HDInsight 처리에서 로그 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f3ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f3ee-104">SYNTAX</span></span>

### <span data-ttu-id="1f3ee-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f3ee-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f3ee-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1f3ee-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f3ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f3ee-107">DESCRIPTION</span></span>
<span data-ttu-id="1f3ee-108">**AzureRmDataFactoryLog** Cmdlet은 문 돼지 또는 Hive 프로젝트의 Azure HDInsight 처리 또는 사용자 지정 작업을 로컬 하드 드라이브에 연결 하는 로그 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="1f3ee-109">먼저 Get-AzureRmDataFactoryRun cmdlet을 실행 하 여 데이터 조각에 대 한 활동의 ID를 가져온 다음 해당 ID를 사용 하 여 HDInsight 클러스터와 연결 된 BLOB (binary large object) 저장소에서 로그 파일을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>

<span data-ttu-id="1f3ee-110">*Downloadlogs* 매개 변수를 지정 하지 않으면 cmdlet은 로그 파일의 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>

<span data-ttu-id="1f3ee-111">출력 디렉터리 ( *output* 매개 변수)를 지정 하지 않고 *downloadlogs* 를 지정 하면 로그 파일이 기본 문서 폴더로 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>

<span data-ttu-id="1f3ee-112">출력 폴더 ( *출력* )와 함께 *downloadlogs* 를 지정 하면 로그 파일이 지정 된 폴더에 다운로드 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="1f3ee-113">예제의</span><span class="sxs-lookup"><span data-stu-id="1f3ee-113">EXAMPLES</span></span>

### <span data-ttu-id="1f3ee-114">예제 1: 특정 폴더에 로그 파일 저장</span><span class="sxs-lookup"><span data-stu-id="1f3ee-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="1f3ee-115">이 명령은 841b77c9-d56c-48d1-99a3-8c16c3e77d39의 ID를 사용 하 여 작업 실행에 대 한 로그 파일을 저장 합니다. 라는 리소스 그룹의 LogProcessingFactory 이라는 data factory의 파이프라인에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="1f3ee-116">로그 파일이 C:\Test 폴더에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="1f3ee-117">예제 2: 기본 문서 폴더에 로그 파일 저장</span><span class="sxs-lookup"><span data-stu-id="1f3ee-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="1f3ee-118">이 명령은 로그 파일을 문서 폴더에 저장 합니다 (기본값).</span><span class="sxs-lookup"><span data-stu-id="1f3ee-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="1f3ee-119">예제 3: 로그 파일의 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f3ee-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="1f3ee-120">이 명령은 로그 파일의 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-120">This command returns the location of log files.</span></span>
<span data-ttu-id="1f3ee-121">*Downloadlogs* 는 지정 되지 않음에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="1f3ee-122">변수</span><span class="sxs-lookup"><span data-stu-id="1f3ee-122">PARAMETERS</span></span>

### <span data-ttu-id="1f3ee-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1f3ee-123">-DataFactory</span></span>
<span data-ttu-id="1f3ee-124">**PSDataFactory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3ee-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1f3ee-125">-DataFactoryName</span></span>
<span data-ttu-id="1f3ee-126">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1f3ee-127">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 대 한 로그 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3ee-128">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="1f3ee-128">-DownloadLogs</span></span>
<span data-ttu-id="1f3ee-129">이 cmdlet이 로그 파일을 로컬 컴퓨터에 다운로드 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-129">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="1f3ee-130">폴더를 지정 하지 않은 경우 파일은 문서 폴더의 *하위 폴더에* 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-130">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="1f3ee-131">-Id</span><span class="sxs-lookup"><span data-stu-id="1f3ee-131">-Id</span></span>
<span data-ttu-id="1f3ee-132">데이터 조각에 대 한 활동 실행의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-132">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="1f3ee-133">Get-AzureRmDataFactoryRun cmdlet을 사용 하 여 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-133">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3ee-134">-출력</span><span class="sxs-lookup"><span data-stu-id="1f3ee-134">-Output</span></span>
<span data-ttu-id="1f3ee-135">다운로드 한 로그 파일이 저장 되는 출력 폴더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-135">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="1f3ee-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f3ee-136">-ResourceGroupName</span></span>
<span data-ttu-id="1f3ee-137">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1f3ee-138">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 속하는 data factory를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-138">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3ee-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3ee-139">-DefaultProfile</span></span>
<span data-ttu-id="1f3ee-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f3ee-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3ee-141">CommonParameters</span></span>
<span data-ttu-id="1f3ee-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f3ee-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3ee-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f3ee-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3ee-144">입력</span><span class="sxs-lookup"><span data-stu-id="1f3ee-144">INPUTS</span></span>

## <span data-ttu-id="1f3ee-145">출력</span><span class="sxs-lookup"><span data-stu-id="1f3ee-145">OUTPUTS</span></span>

### <span data-ttu-id="1f3ee-146">DataFactories를 실행 합니다. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="1f3ee-146">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="1f3ee-147">상속자</span><span class="sxs-lookup"><span data-stu-id="1f3ee-147">NOTES</span></span>
* <span data-ttu-id="1f3ee-148">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="1f3ee-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1f3ee-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f3ee-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f3ee-150">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="1f3ee-150">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="1f3ee-151">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f3ee-151">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1f3ee-152">새로운 AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f3ee-152">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1f3ee-153">제거-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f3ee-153">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="1f3ee-154">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="1f3ee-154">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="1f3ee-155">일시 중단-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="1f3ee-155">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)

