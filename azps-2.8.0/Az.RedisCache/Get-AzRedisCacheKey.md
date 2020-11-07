---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 96eed93e4020384b0c989a05f549aa21f5482493
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873460"
---
# <span data-ttu-id="475b4-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="475b4-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="475b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475b4-102">SYNOPSIS</span></span>
<span data-ttu-id="475b4-103">Redis 캐시에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="475b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="475b4-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="475b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="475b4-105">DESCRIPTION</span></span>
<span data-ttu-id="475b4-106">**AzRedisCacheKey** Cmdlet은 Azure Redis Cache에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="475b4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="475b4-107">EXAMPLES</span></span>

### <span data-ttu-id="475b4-108">예제 1: Redis 캐시에 대 한 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="475b4-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="475b4-109">이 명령은 MyCacheKey 라는 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="475b4-110">변수</span><span class="sxs-lookup"><span data-stu-id="475b4-110">PARAMETERS</span></span>

### <span data-ttu-id="475b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475b4-111">-DefaultProfile</span></span>
<span data-ttu-id="475b4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475b4-113">-이름</span><span class="sxs-lookup"><span data-stu-id="475b4-113">-Name</span></span>
<span data-ttu-id="475b4-114">Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475b4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="475b4-115">-ResourceGroupName</span></span>
<span data-ttu-id="475b4-116">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="475b4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475b4-117">CommonParameters</span></span>
<span data-ttu-id="475b4-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="475b4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475b4-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475b4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475b4-120">입력</span><span class="sxs-lookup"><span data-stu-id="475b4-120">INPUTS</span></span>

### <span data-ttu-id="475b4-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="475b4-121">System.String</span></span>

## <span data-ttu-id="475b4-122">출력</span><span class="sxs-lookup"><span data-stu-id="475b4-122">OUTPUTS</span></span>

### <span data-ttu-id="475b4-123">Redis. RedisAccessKeys.</span><span class="sxs-lookup"><span data-stu-id="475b4-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="475b4-124">상속자</span><span class="sxs-lookup"><span data-stu-id="475b4-124">NOTES</span></span>

## <span data-ttu-id="475b4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="475b4-125">RELATED LINKS</span></span>

[<span data-ttu-id="475b4-126">새로운 AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="475b4-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)

