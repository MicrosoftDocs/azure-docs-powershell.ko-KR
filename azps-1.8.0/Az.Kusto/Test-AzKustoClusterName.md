---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: 9a3d8397914317d733c8da47e7d095e1acb541e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867782"
---
# <span data-ttu-id="ba387-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="ba387-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="ba387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba387-102">SYNOPSIS</span></span>
<span data-ttu-id="ba387-103">주어진 Kusto 클러스터 이름을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="ba387-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba387-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba387-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba387-105">DESCRIPTION</span></span>
<span data-ttu-id="ba387-106">주어진 Kusto 클러스터 이름을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="ba387-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba387-107">EXAMPLES</span></span>

### <span data-ttu-id="ba387-108">예제 1-사용 중인 클러스터 이름에 대 한 Kusto의 사용 가능 여부 확인</span><span class="sxs-lookup"><span data-stu-id="ba387-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="ba387-109">위 명령에 "mykustocluster" 이라는 클러스터의 Kusto "중앙 US" 지역에 존재 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="ba387-110">예제 2-사용 중이 아닌 클러스터 이름에 대 한 Kusto의 가용성 확인</span><span class="sxs-lookup"><span data-stu-id="ba387-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="ba387-111">위 명령에 "mykustocluster" 이라는 클러스터의 Kusto "중앙 US" 지역에 존재 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="ba387-112">변수</span><span class="sxs-lookup"><span data-stu-id="ba387-112">PARAMETERS</span></span>

### <span data-ttu-id="ba387-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba387-113">-DefaultProfile</span></span>
<span data-ttu-id="ba387-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba387-115">-위치</span><span class="sxs-lookup"><span data-stu-id="ba387-115">-Location</span></span>
<span data-ttu-id="ba387-116">검사할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-116">The location where to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba387-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ba387-117">-Name</span></span>
<span data-ttu-id="ba387-118">특정 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-118">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba387-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba387-119">CommonParameters</span></span>
<span data-ttu-id="ba387-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba387-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba387-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba387-122">입력</span><span class="sxs-lookup"><span data-stu-id="ba387-122">INPUTS</span></span>

### <span data-ttu-id="ba387-123">않아야</span><span class="sxs-lookup"><span data-stu-id="ba387-123">None</span></span>

## <span data-ttu-id="ba387-124">출력</span><span class="sxs-lookup"><span data-stu-id="ba387-124">OUTPUTS</span></span>

### <span data-ttu-id="ba387-125">PSKustoClusterNameAvailability를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ba387-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="ba387-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ba387-126">NOTES</span></span>

## <span data-ttu-id="ba387-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba387-127">RELATED LINKS</span></span>