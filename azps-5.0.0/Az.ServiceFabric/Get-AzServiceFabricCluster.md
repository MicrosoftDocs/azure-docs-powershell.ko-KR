---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 43e2ae9426d80b7762fb8afe7b9c57a53a232f8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217020"
---
# <span data-ttu-id="5da9a-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5da9a-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="5da9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da9a-102">SYNOPSIS</span></span>
<span data-ttu-id="5da9a-103">클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5da9a-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="5da9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5da9a-104">SYNTAX</span></span>

### <span data-ttu-id="5da9a-105">BySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="5da9a-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5da9a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5da9a-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5da9a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5da9a-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da9a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5da9a-108">DESCRIPTION</span></span>
<span data-ttu-id="5da9a-109">**AzServiceFabricCluster** 가 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5da9a-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="5da9a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5da9a-110">EXAMPLES</span></span>

### <span data-ttu-id="5da9a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5da9a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="5da9a-112">이 명령은 ' myCluster ' 클러스터에 대 한 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5da9a-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="5da9a-113">변수</span><span class="sxs-lookup"><span data-stu-id="5da9a-113">PARAMETERS</span></span>

### <span data-ttu-id="5da9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da9a-114">-DefaultProfile</span></span>
<span data-ttu-id="5da9a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5da9a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da9a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5da9a-116">-Name</span></span>
<span data-ttu-id="5da9a-117">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="5da9a-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="5da9a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da9a-118">-ResourceGroupName</span></span>
<span data-ttu-id="5da9a-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da9a-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5da9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da9a-120">CommonParameters</span></span>
<span data-ttu-id="5da9a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da9a-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5da9a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da9a-123">입력</span><span class="sxs-lookup"><span data-stu-id="5da9a-123">INPUTS</span></span>

### <span data-ttu-id="5da9a-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5da9a-124">System.String</span></span>

## <span data-ttu-id="5da9a-125">출력</span><span class="sxs-lookup"><span data-stu-id="5da9a-125">OUTPUTS</span></span>

### <span data-ttu-id="5da9a-126">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="5da9a-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5da9a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="5da9a-127">NOTES</span></span>

## <span data-ttu-id="5da9a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5da9a-128">RELATED LINKS</span></span>