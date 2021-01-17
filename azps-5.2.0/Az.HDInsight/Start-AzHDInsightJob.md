---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 0225C7CA-74B4-4ACC-870C-9539DF6ECC47
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/start-azhdinsightjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Start-AzHDInsightJob.md
ms.openlocfilehash: 6eab5c80fa8c21d5b592f0e194a5aba50c4d3002
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328271"
---
# <span data-ttu-id="bb319-101">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bb319-101">Start-AzHDInsightJob</span></span>

## <span data-ttu-id="bb319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb319-102">SYNOPSIS</span></span>
<span data-ttu-id="bb319-103">지정된 클러스터에서 정의된 Azure HDInsight 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-103">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

## <span data-ttu-id="bb319-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb319-104">SYNTAX</span></span>

```
Start-AzHDInsightJob [-ClusterName] <String> [-JobDefinition] <AzureHDInsightJobDefinition>
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb319-105">설명</span><span class="sxs-lookup"><span data-stu-id="bb319-105">DESCRIPTION</span></span>
<span data-ttu-id="bb319-106">**Start-AzHDInsightJob** cmdlet은 지정된 클러스터에서 정의된 Azure HDInsight 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-106">The **Start-AzHDInsightJob** cmdlet starts a defined Azure HDInsight job on a specified cluster.</span></span>
<span data-ttu-id="bb319-107">MapReduce 작업, 스트리밍 MapReduce 작업, Hive 작업 또는 Pig 작업일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-107">This can be a MapReduce job, a Streaming MapReduce job, a Hive job, or a Pig job.</span></span>

## <span data-ttu-id="bb319-108">예제</span><span class="sxs-lookup"><span data-stu-id="bb319-108">EXAMPLES</span></span>

### <span data-ttu-id="bb319-109">예제 1: 지정된 클러스터에서 작업 시작</span><span class="sxs-lookup"><span data-stu-id="bb319-109">Example 1: Start a job on the specified cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="bb319-110">이 명령은 your-hadoop-001이라는 클러스터에서 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-110">This command starts a job on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="bb319-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb319-111">PARAMETERS</span></span>

### <span data-ttu-id="bb319-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bb319-112">-ClusterName</span></span>
<span data-ttu-id="bb319-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb319-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb319-114">-DefaultProfile</span></span>
<span data-ttu-id="bb319-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bb319-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb319-116">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="bb319-116">-HttpCredential</span></span>
<span data-ttu-id="bb319-117">클러스터에 대한 클러스터 로그인(HTTP) 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-117">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb319-118">-JobDefinition</span><span class="sxs-lookup"><span data-stu-id="bb319-118">-JobDefinition</span></span>
<span data-ttu-id="bb319-119">Azure HDInsight 클러스터에서 시작할 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-119">Specifies the job to start on the Azure HDInsight cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb319-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb319-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb319-121">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bb319-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb319-122">CommonParameters</span></span>
<span data-ttu-id="bb319-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb319-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb319-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bb319-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb319-125">입력</span><span class="sxs-lookup"><span data-stu-id="bb319-125">INPUTS</span></span>

### <span data-ttu-id="bb319-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bb319-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJobDefinition</span></span>

## <span data-ttu-id="bb319-127">출력</span><span class="sxs-lookup"><span data-stu-id="bb319-127">OUTPUTS</span></span>

### <span data-ttu-id="bb319-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bb319-128">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightJob</span></span>

## <span data-ttu-id="bb319-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb319-129">NOTES</span></span>

## <span data-ttu-id="bb319-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb319-130">RELATED LINKS</span></span>

[<span data-ttu-id="bb319-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bb319-131">Get-AzHDInsightJob</span></span>](./Get-AzHDInsightJob.md)

[<span data-ttu-id="bb319-132">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="bb319-132">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="bb319-133">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bb319-133">Stop-AzHDInsightJob</span></span>](./Stop-AzHDInsightJob.md)

[<span data-ttu-id="bb319-134">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="bb319-134">Wait-AzHDInsightJob</span></span>](./Wait-AzHDInsightJob.md)

