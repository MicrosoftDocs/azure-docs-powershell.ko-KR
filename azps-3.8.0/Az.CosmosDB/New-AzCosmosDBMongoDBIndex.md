---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043647"
---
# <span data-ttu-id="a1763-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="a1763-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="a1763-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1763-102">SYNOPSIS</span></span>
<span data-ttu-id="a1763-103">새 CosmosDB MongoDB Index를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="a1763-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1763-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1763-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a1763-105">DESCRIPTION</span></span>
<span data-ttu-id="a1763-106">**AzCosmosDBMongoDBIndex** 는 새 CosmosDB MongoDB Index를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="a1763-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a1763-107">EXAMPLES</span></span>

### <span data-ttu-id="a1763-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a1763-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="a1763-109">변수</span><span class="sxs-lookup"><span data-stu-id="a1763-109">PARAMETERS</span></span>

### <span data-ttu-id="a1763-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1763-110">-DefaultProfile</span></span>
<span data-ttu-id="a1763-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1763-112">-키</span><span class="sxs-lookup"><span data-stu-id="a1763-112">-Key</span></span>
<span data-ttu-id="a1763-113">문자열로 된 키 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1763-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="a1763-114">-TtlInSeconds</span></span>
<span data-ttu-id="a1763-115">색인이 만료 되는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1763-116">-고유</span><span class="sxs-lookup"><span data-stu-id="a1763-116">-Unique</span></span>
<span data-ttu-id="a1763-117">인덱스가 고유한 지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1763-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1763-118">CommonParameters</span></span>
<span data-ttu-id="a1763-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1763-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1763-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a1763-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1763-121">입력</span><span class="sxs-lookup"><span data-stu-id="a1763-121">INPUTS</span></span>

### <span data-ttu-id="a1763-122">않아야</span><span class="sxs-lookup"><span data-stu-id="a1763-122">None</span></span>

## <span data-ttu-id="a1763-123">출력</span><span class="sxs-lookup"><span data-stu-id="a1763-123">OUTPUTS</span></span>

### <span data-ttu-id="a1763-124">CosmosDB. PSMongoIndex/.</span><span class="sxs-lookup"><span data-stu-id="a1763-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="a1763-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a1763-125">NOTES</span></span>

## <span data-ttu-id="a1763-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1763-126">RELATED LINKS</span></span>