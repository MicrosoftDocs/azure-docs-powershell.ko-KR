---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: c81199bb78a64ac2ed32a21e0f3822093a2b2b14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217531"
---
# <span data-ttu-id="b2e7b-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b2e7b-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="b2e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e7b-103">관리 되는 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="b2e7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2e7b-104">SYNTAX</span></span>

### <span data-ttu-id="b2e7b-105">BySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2e7b-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e7b-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b2e7b-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e7b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b2e7b-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e7b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b2e7b-108">DESCRIPTION</span></span>
<span data-ttu-id="b2e7b-109">관리 되는 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="b2e7b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b2e7b-110">EXAMPLES</span></span>

### <span data-ttu-id="b2e7b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2e7b-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="b2e7b-112">클러스터 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-112">Get cluster details.</span></span>

### <span data-ttu-id="b2e7b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b2e7b-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="b2e7b-114">지정 된 리소스 그룹에 있는 클러스터 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="b2e7b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="b2e7b-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="b2e7b-116">현재 구독에서 클러스터 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="b2e7b-117">변수</span><span class="sxs-lookup"><span data-stu-id="b2e7b-117">PARAMETERS</span></span>

### <span data-ttu-id="b2e7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e7b-118">-DefaultProfile</span></span>
<span data-ttu-id="b2e7b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e7b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b2e7b-120">-Name</span></span>
<span data-ttu-id="b2e7b-121">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e7b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e7b-122">-ResourceGroupName</span></span>
<span data-ttu-id="b2e7b-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2e7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e7b-124">CommonParameters</span></span>
<span data-ttu-id="b2e7b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e7b-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2e7b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e7b-127">입력</span><span class="sxs-lookup"><span data-stu-id="b2e7b-127">INPUTS</span></span>

### <span data-ttu-id="b2e7b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2e7b-128">System.String</span></span>

## <span data-ttu-id="b2e7b-129">출력</span><span class="sxs-lookup"><span data-stu-id="b2e7b-129">OUTPUTS</span></span>

### <span data-ttu-id="b2e7b-130">ServiceFabric. a m. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="b2e7b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="b2e7b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b2e7b-131">NOTES</span></span>

## <span data-ttu-id="b2e7b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2e7b-132">RELATED LINKS</span></span>