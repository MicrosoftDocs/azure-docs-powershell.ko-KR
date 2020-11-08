---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: d103a2bc3d23ff37857592ed9496e625302ed144
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212771"
---
# <span data-ttu-id="25a2d-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="25a2d-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="25a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="25a2d-103">클러스터 구성 개체에 스크립트 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="25a2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25a2d-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25a2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="25a2d-106">**AzHDInsightScriptAction** cmdlet은 New-AzHDInsightClusterConfig cmdlet에서 만든 HDInsight 구성 개체에 스크립트 작업을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="25a2d-107">스크립트 동작은 추가 소프트웨어를 설치 하거나 Windows PowerShell 또는 Bash 스크립트 (Windows 또는 Linux 클러스터의 경우)를 사용 하 여 Hadoop 클러스터에서 실행 되는 응용 프로그램의 구성을 변경 하는 데 사용 되는 기능을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="25a2d-108">HDInsight 클러스터를 배포할 때 클러스터 노드에서 스크립트 작업을 실행 하 고 클러스터 전체 HDInsight 구성의 노드 이후 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="25a2d-109">스크립트 동작은 시스템 관리자 계정 권한으로 실행 되며 클러스터 노드에 대 한 전체 액세스 권한을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="25a2d-110">각 클러스터에 대해 지정 된 순서로 실행할 스크립트 작업 목록을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="25a2d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="25a2d-111">EXAMPLES</span></span>

### <span data-ttu-id="25a2d-112">예제 1: 클러스터 구성 개체에 스크립트 동작 추가</span><span class="sxs-lookup"><span data-stu-id="25a2d-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="25a2d-113">이 명령은 클러스터 생성 종료 시 실행 될 hadoop-001 클러스터의 Head 및 Worker 노드에 대 한 스크립트 동작을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="25a2d-114">변수</span><span class="sxs-lookup"><span data-stu-id="25a2d-114">PARAMETERS</span></span>

### <span data-ttu-id="25a2d-115">-구성</span><span class="sxs-lookup"><span data-stu-id="25a2d-115">-Config</span></span>
<span data-ttu-id="25a2d-116">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="25a2d-117">이 개체는 **AzHDInsightClusterConfig** cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a2d-118">-DefaultProfile</span></span>
<span data-ttu-id="25a2d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="25a2d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25a2d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="25a2d-120">-Name</span></span>
<span data-ttu-id="25a2d-121">스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-121">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a2d-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="25a2d-122">-NodeType</span></span>
<span data-ttu-id="25a2d-123">스크립트 작업을 실행할 노드 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="25a2d-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25a2d-125">인원 노드</span><span class="sxs-lookup"><span data-stu-id="25a2d-125">HeadNode</span></span>
- <span data-ttu-id="25a2d-126">. 노드</span><span class="sxs-lookup"><span data-stu-id="25a2d-126">WorkerNode</span></span>
- <span data-ttu-id="25a2d-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="25a2d-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a2d-128">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="25a2d-128">-Parameters</span></span>
<span data-ttu-id="25a2d-129">스크립트 작업에 대 한 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a2d-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="25a2d-130">-Uri</span></span>
<span data-ttu-id="25a2d-131">스크립트 작업 (PowerShell 또는 Bash 스크립트)에 대 한 공용 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a2d-132">CommonParameters</span></span>
<span data-ttu-id="25a2d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25a2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a2d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a2d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a2d-135">입력</span><span class="sxs-lookup"><span data-stu-id="25a2d-135">INPUTS</span></span>

### <span data-ttu-id="25a2d-136">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="25a2d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="25a2d-137">출력</span><span class="sxs-lookup"><span data-stu-id="25a2d-137">OUTPUTS</span></span>

### <span data-ttu-id="25a2d-138">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="25a2d-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="25a2d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="25a2d-139">NOTES</span></span>

## <span data-ttu-id="25a2d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25a2d-140">RELATED LINKS</span></span>

[<span data-ttu-id="25a2d-141">새로운 AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="25a2d-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

