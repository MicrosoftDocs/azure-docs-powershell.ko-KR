---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336441"
---
# <span data-ttu-id="513d1-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="513d1-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="513d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513d1-102">SYNOPSIS</span></span>
<span data-ttu-id="513d1-103">두 Redis Cache 간에 지역 복제 링크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="513d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="513d1-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="513d1-105">설명</span><span class="sxs-lookup"><span data-stu-id="513d1-105">DESCRIPTION</span></span>
<span data-ttu-id="513d1-106">두 Redis Cache 간에 지역 복제 링크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="513d1-107">예제</span><span class="sxs-lookup"><span data-stu-id="513d1-107">EXAMPLES</span></span>

### <span data-ttu-id="513d1-108">예제 1: 두 캐시 간의 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="513d1-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="513d1-109">이 명령은 Redis Cache mycache1과 mycache2 간에 지역 복제 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="513d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="513d1-110">PARAMETERS</span></span>

### <span data-ttu-id="513d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513d1-111">-DefaultProfile</span></span>
<span data-ttu-id="513d1-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="513d1-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="513d1-113">-PrimaryServerName</span></span>
<span data-ttu-id="513d1-114">링크에 있는 기본 redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="513d1-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="513d1-115">-SecondaryServerName</span></span>
<span data-ttu-id="513d1-116">링크에 있는 보조 Redis Cache의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="513d1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="513d1-117">-Confirm</span></span>
<span data-ttu-id="513d1-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513d1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513d1-119">-WhatIf</span></span>
<span data-ttu-id="513d1-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="513d1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513d1-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513d1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513d1-122">CommonParameters</span></span>
<span data-ttu-id="513d1-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="513d1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513d1-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="513d1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513d1-125">입력</span><span class="sxs-lookup"><span data-stu-id="513d1-125">INPUTS</span></span>

### <span data-ttu-id="513d1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="513d1-126">System.String</span></span>

## <span data-ttu-id="513d1-127">출력</span><span class="sxs-lookup"><span data-stu-id="513d1-127">OUTPUTS</span></span>

### <span data-ttu-id="513d1-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="513d1-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="513d1-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="513d1-129">NOTES</span></span>

## <span data-ttu-id="513d1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="513d1-130">RELATED LINKS</span></span>

[<span data-ttu-id="513d1-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="513d1-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="513d1-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="513d1-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="513d1-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="513d1-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="513d1-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="513d1-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="513d1-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="513d1-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="513d1-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="513d1-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)