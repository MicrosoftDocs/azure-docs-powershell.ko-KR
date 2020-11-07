---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: ef1c06c475b5de4984abf7859f033d68ad7d9dfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868194"
---
# <span data-ttu-id="6aa3a-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="6aa3a-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="6aa3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa3a-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa3a-103">Azure HDInsight 클러스터에 새 스크립트 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6aa3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6aa3a-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6aa3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6aa3a-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa3a-106">**AzHDInsightScriptAction** Cmdlet은 Azure HDInsight 클러스터에 새 스크립트 작업을 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="6aa3a-107">스크립트 작업이 처음에 성공 하는 한, 클러스터의 크기를 조정할 때마다 스크립트 작업이 실행 되도록 *Persistonsuccess* 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="6aa3a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6aa3a-108">EXAMPLES</span></span>

### <span data-ttu-id="6aa3a-109">예제 1: 실행 중인 HDInsight 클러스터에 새 스크립트 작업 제출</span><span class="sxs-lookup"><span data-stu-id="6aa3a-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="6aa3a-110">이 명령은 스크립트 동작을 실행 중인 HDInsight 클러스터에 제출 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="6aa3a-111">변수</span><span class="sxs-lookup"><span data-stu-id="6aa3a-111">PARAMETERS</span></span>

### <span data-ttu-id="6aa3a-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6aa3a-112">-ApplicationName</span></span>
<span data-ttu-id="6aa3a-113">스크립트 작업의 응용 프로그램 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="6aa3a-114">*ApplicationName* 이 지정 되 면 *Persistonsuccess* 가 False로 설정 되 고 노드는 edgenode만 포함 해야 하며 스크립트 동작 수는 1 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6aa3a-115">-ClusterName</span></span>
<span data-ttu-id="6aa3a-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6aa3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa3a-117">-DefaultProfile</span></span>
<span data-ttu-id="6aa3a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6aa3a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6aa3a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="6aa3a-119">-Name</span></span>
<span data-ttu-id="6aa3a-120">스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="6aa3a-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="6aa3a-121">-NodeTypes</span></span>
<span data-ttu-id="6aa3a-122">스크립트 작업을 실행할 노드 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3a-123">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="6aa3a-123">-Parameters</span></span>
<span data-ttu-id="6aa3a-124">스크립트 작업에 대 한 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3a-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="6aa3a-125">-PersistOnSuccess</span></span>
<span data-ttu-id="6aa3a-126">클러스터의 크기를 조정할 때마다 스크립트 동작이 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="6aa3a-127">스크립트 작업이 처음에 실패 하는 경우이 스위치 매개 변수는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa3a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6aa3a-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6aa3a-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="6aa3a-130">-Uri</span></span>
<span data-ttu-id="6aa3a-131">스크립트 작업 (PowerShell 또는 Bash 스크립트)에 대 한 공용 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa3a-132">CommonParameters</span></span>
<span data-ttu-id="6aa3a-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa3a-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa3a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa3a-135">입력</span><span class="sxs-lookup"><span data-stu-id="6aa3a-135">INPUTS</span></span>

### <span data-ttu-id="6aa3a-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6aa3a-136">System.String</span></span>

### <span data-ttu-id="6aa3a-137">시스템 Uri</span><span class="sxs-lookup"><span data-stu-id="6aa3a-137">System.Uri</span></span>

### <span data-ttu-id="6aa3a-138">RuntimeScriptActionClusterNodeType [] (으)로의 명령</span><span class="sxs-lookup"><span data-stu-id="6aa3a-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="6aa3a-139">출력</span><span class="sxs-lookup"><span data-stu-id="6aa3a-139">OUTPUTS</span></span>

### <span data-ttu-id="6aa3a-140">AzureHDInsightRuntimeScriptActionOperationResource를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="6aa3a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6aa3a-141">NOTES</span></span>

## <span data-ttu-id="6aa3a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6aa3a-142">RELATED LINKS</span></span>

[<span data-ttu-id="6aa3a-143">추가-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="6aa3a-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)

