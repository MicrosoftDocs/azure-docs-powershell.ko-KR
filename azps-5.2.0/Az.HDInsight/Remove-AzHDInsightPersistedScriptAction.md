---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 4d3d88fb5a8cca2343403870233e89b0f2073e8e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328355"
---
# <span data-ttu-id="bed8e-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bed8e-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="bed8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bed8e-102">SYNOPSIS</span></span>
<span data-ttu-id="bed8e-103">HDInsight 클러스터에서 지속된 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="bed8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="bed8e-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed8e-105">설명</span><span class="sxs-lookup"><span data-stu-id="bed8e-105">DESCRIPTION</span></span>
<span data-ttu-id="bed8e-106">**Remove-AzHDInsightPersistedScriptAction** cmdlet은 지정된 Azure HDInsight 클러스터의 지속형 스크립트 작업 목록에서 지속형 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="bed8e-107">클러스터가 확장될 때 제거된 스크립트가 더 이상 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="bed8e-108">예제</span><span class="sxs-lookup"><span data-stu-id="bed8e-108">EXAMPLES</span></span>

### <span data-ttu-id="bed8e-109">예제 1: 클러스터의 지속된 스크립트 작업 목록에서 스크립트 작업 제거</span><span class="sxs-lookup"><span data-stu-id="bed8e-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="bed8e-110">이 명령은 지정된 클러스터의 지속된 스크립트 작업 목록에서 Scriptaction이라는 스크립트 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="bed8e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bed8e-111">PARAMETERS</span></span>

### <span data-ttu-id="bed8e-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bed8e-112">-ClusterName</span></span>
<span data-ttu-id="bed8e-113">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="bed8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed8e-114">-DefaultProfile</span></span>
<span data-ttu-id="bed8e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bed8e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bed8e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bed8e-116">-Name</span></span>
<span data-ttu-id="bed8e-117">제거할 지속된 스크립트 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed8e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bed8e-118">-ResourceGroupName</span></span>
<span data-ttu-id="bed8e-119">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bed8e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed8e-120">CommonParameters</span></span>
<span data-ttu-id="bed8e-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bed8e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed8e-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bed8e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed8e-123">입력</span><span class="sxs-lookup"><span data-stu-id="bed8e-123">INPUTS</span></span>

### <span data-ttu-id="bed8e-124">없음</span><span class="sxs-lookup"><span data-stu-id="bed8e-124">None</span></span>

## <span data-ttu-id="bed8e-125">출력</span><span class="sxs-lookup"><span data-stu-id="bed8e-125">OUTPUTS</span></span>

### <span data-ttu-id="bed8e-126">System.Void</span><span class="sxs-lookup"><span data-stu-id="bed8e-126">System.Void</span></span>

## <span data-ttu-id="bed8e-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bed8e-127">NOTES</span></span>

## <span data-ttu-id="bed8e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bed8e-128">RELATED LINKS</span></span>

[<span data-ttu-id="bed8e-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bed8e-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="bed8e-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="bed8e-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)

