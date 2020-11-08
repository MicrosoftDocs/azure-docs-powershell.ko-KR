---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043633"
---
# <span data-ttu-id="1adfd-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="1adfd-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="1adfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1adfd-102">SYNOPSIS</span></span>
<span data-ttu-id="1adfd-103">새 CosmosDB Sql UniqueKey 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1adfd-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="1adfd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1adfd-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1adfd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1adfd-105">DESCRIPTION</span></span>
<span data-ttu-id="1adfd-106">**AzCosmosDBSqlUniqueKey** Cmdlet은 PSUniqueKey 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1adfd-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="1adfd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1adfd-107">EXAMPLES</span></span>

### <span data-ttu-id="1adfd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1adfd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="1adfd-109">변수</span><span class="sxs-lookup"><span data-stu-id="1adfd-109">PARAMETERS</span></span>

### <span data-ttu-id="1adfd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adfd-110">-DefaultProfile</span></span>
<span data-ttu-id="1adfd-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1adfd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1adfd-112">-Path</span><span class="sxs-lookup"><span data-stu-id="1adfd-112">-Path</span></span>
<span data-ttu-id="1adfd-113">경로 값 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="1adfd-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1adfd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adfd-114">CommonParameters</span></span>
<span data-ttu-id="1adfd-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1adfd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adfd-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1adfd-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adfd-117">입력</span><span class="sxs-lookup"><span data-stu-id="1adfd-117">INPUTS</span></span>

### <span data-ttu-id="1adfd-118">않아야</span><span class="sxs-lookup"><span data-stu-id="1adfd-118">None</span></span>

## <span data-ttu-id="1adfd-119">출력</span><span class="sxs-lookup"><span data-stu-id="1adfd-119">OUTPUTS</span></span>

### <span data-ttu-id="1adfd-120">CosmosDB. PSSqlUniqueKey/.</span><span class="sxs-lookup"><span data-stu-id="1adfd-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="1adfd-121">상속자</span><span class="sxs-lookup"><span data-stu-id="1adfd-121">NOTES</span></span>

## <span data-ttu-id="1adfd-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1adfd-122">RELATED LINKS</span></span>