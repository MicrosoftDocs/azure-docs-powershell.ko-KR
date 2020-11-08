---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047677"
---
# <span data-ttu-id="fedf3-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fedf3-101">New-AzRedisCache</span></span>

## <span data-ttu-id="fedf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fedf3-102">SYNOPSIS</span></span>
<span data-ttu-id="fedf3-103">Redis 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="fedf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fedf3-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fedf3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fedf3-105">DESCRIPTION</span></span>
<span data-ttu-id="fedf3-106">**AzRedisCache** Cmdlet은 Azure Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="fedf3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fedf3-107">EXAMPLES</span></span>

### <span data-ttu-id="fedf3-108">예제 1: Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="fedf3-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="fedf3-109">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="fedf3-110">예제 2: 표준 SKU Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="fedf3-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="fedf3-111">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="fedf3-112">변수</span><span class="sxs-lookup"><span data-stu-id="fedf3-112">PARAMETERS</span></span>

### <span data-ttu-id="fedf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedf3-113">-DefaultProfile</span></span>
<span data-ttu-id="fedf3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fedf3-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="fedf3-115">-EnableNonSslPort</span></span>
<span data-ttu-id="fedf3-116">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="fedf3-117">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-117">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-118">-위치</span><span class="sxs-lookup"><span data-stu-id="fedf3-118">-Location</span></span>
<span data-ttu-id="fedf3-119">Redis 캐시를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="fedf3-120">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-120">Valid values are:</span></span> 
- <span data-ttu-id="fedf3-121">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="fedf3-121">North Central US</span></span>
- <span data-ttu-id="fedf3-122">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="fedf3-122">South Central US</span></span>
- <span data-ttu-id="fedf3-123">중부 US</span><span class="sxs-lookup"><span data-stu-id="fedf3-123">Central US</span></span>
- <span data-ttu-id="fedf3-124">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="fedf3-124">West Europe</span></span>
- <span data-ttu-id="fedf3-125">동유럽</span><span class="sxs-lookup"><span data-stu-id="fedf3-125">North Europe</span></span>
- <span data-ttu-id="fedf3-126">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="fedf3-126">West US</span></span>
- <span data-ttu-id="fedf3-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="fedf3-127">East US</span></span>
- <span data-ttu-id="fedf3-128">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="fedf3-128">East US 2</span></span>
- <span data-ttu-id="fedf3-129">일본 동부</span><span class="sxs-lookup"><span data-stu-id="fedf3-129">Japan East</span></span>
- <span data-ttu-id="fedf3-130">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="fedf3-130">Japan West</span></span>
- <span data-ttu-id="fedf3-131">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="fedf3-131">Brazil South</span></span>
- <span data-ttu-id="fedf3-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="fedf3-132">Southeast Asia</span></span>
- <span data-ttu-id="fedf3-133">동아시아</span><span class="sxs-lookup"><span data-stu-id="fedf3-133">East Asia</span></span>
- <span data-ttu-id="fedf3-134">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="fedf3-134">Australia East</span></span>
- <span data-ttu-id="fedf3-135">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="fedf3-135">Australia Southeast</span></span>

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

### <span data-ttu-id="fedf3-136">-없음 Tls 버전</span><span class="sxs-lookup"><span data-stu-id="fedf3-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="fedf3-137">클라이언트가 캐시에 연결 하는 데 필요한 TLS 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="fedf3-138">-이름</span><span class="sxs-lookup"><span data-stu-id="fedf3-138">-Name</span></span>
<span data-ttu-id="fedf3-139">만들 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="fedf3-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="fedf3-140">-RedisConfiguration</span></span>
<span data-ttu-id="fedf3-141">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="fedf3-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fedf3-143">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="fedf3-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="fedf3-144">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="fedf3-145">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="fedf3-145">Premium tier only.</span></span>
- <span data-ttu-id="fedf3-146">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="fedf3-147">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="fedf3-148">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="fedf3-148">Premium tier only.</span></span>
- <span data-ttu-id="fedf3-149">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="fedf3-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="fedf3-150">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="fedf3-151">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="fedf3-151">Premium tier only.</span></span> 
- <span data-ttu-id="fedf3-152">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="fedf3-152">maxmemory-reserved.</span></span>
<span data-ttu-id="fedf3-153">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="fedf3-154">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fedf3-155">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="fedf3-155">maxmemory-policy.</span></span>
<span data-ttu-id="fedf3-156">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="fedf3-157">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="fedf3-157">All pricing tiers.</span></span> 
- <span data-ttu-id="fedf3-158">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="fedf3-158">notify-keyspace-events.</span></span>
<span data-ttu-id="fedf3-159">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="fedf3-160">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="fedf3-161">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="fedf3-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="fedf3-162">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fedf3-163">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fedf3-164">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="fedf3-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="fedf3-165">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fedf3-166">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fedf3-167">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="fedf3-167">set-max-intset-entries.</span></span>
<span data-ttu-id="fedf3-168">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fedf3-169">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fedf3-170">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="fedf3-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="fedf3-171">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fedf3-172">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fedf3-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="fedf3-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="fedf3-174">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="fedf3-175">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="fedf3-176">databases.</span><span class="sxs-lookup"><span data-stu-id="fedf3-176">databases.</span></span>
<span data-ttu-id="fedf3-177">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-177">Configures the number of databases.</span></span>
<span data-ttu-id="fedf3-178">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="fedf3-179">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="fedf3-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="fedf3-180">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 http://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="fedf3-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fedf3-181">-ResourceGroupName</span></span>
<span data-ttu-id="fedf3-182">Redis 캐시를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="fedf3-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="fedf3-183">-ShardCount</span></span>
<span data-ttu-id="fedf3-184">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="fedf3-185">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fedf3-186">raid-1</span><span class="sxs-lookup"><span data-stu-id="fedf3-186">1</span></span>
- <span data-ttu-id="fedf3-187">2</span><span class="sxs-lookup"><span data-stu-id="fedf3-187">2</span></span>
- <span data-ttu-id="fedf3-188">3-4</span><span class="sxs-lookup"><span data-stu-id="fedf3-188">3</span></span>
- <span data-ttu-id="fedf3-189">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="fedf3-189">4</span></span>
- <span data-ttu-id="fedf3-190">5mb</span><span class="sxs-lookup"><span data-stu-id="fedf3-190">5</span></span>
- <span data-ttu-id="fedf3-191">26</span><span class="sxs-lookup"><span data-stu-id="fedf3-191">6</span></span>
- <span data-ttu-id="fedf3-192">7</span><span class="sxs-lookup"><span data-stu-id="fedf3-192">7</span></span>
- <span data-ttu-id="fedf3-193">20cm(8</span><span class="sxs-lookup"><span data-stu-id="fedf3-193">8</span></span>
- <span data-ttu-id="fedf3-194">되었는지</span><span class="sxs-lookup"><span data-stu-id="fedf3-194">9</span></span> 
- <span data-ttu-id="fedf3-195">1천만</span><span class="sxs-lookup"><span data-stu-id="fedf3-195">10</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-196">-크기</span><span class="sxs-lookup"><span data-stu-id="fedf3-196">-Size</span></span>
<span data-ttu-id="fedf3-197">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="fedf3-198">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-198">Valid values are:</span></span> 
- <span data-ttu-id="fedf3-199">P1</span><span class="sxs-lookup"><span data-stu-id="fedf3-199">P1</span></span>
- <span data-ttu-id="fedf3-200">즉</span><span class="sxs-lookup"><span data-stu-id="fedf3-200">P2</span></span>
- <span data-ttu-id="fedf3-201">P3</span><span class="sxs-lookup"><span data-stu-id="fedf3-201">P3</span></span>
- <span data-ttu-id="fedf3-202">P4</span><span class="sxs-lookup"><span data-stu-id="fedf3-202">P4</span></span>
- <span data-ttu-id="fedf3-203">P5</span><span class="sxs-lookup"><span data-stu-id="fedf3-203">P5</span></span>
- <span data-ttu-id="fedf3-204">C0</span><span class="sxs-lookup"><span data-stu-id="fedf3-204">C0</span></span>
- <span data-ttu-id="fedf3-205">C1</span><span class="sxs-lookup"><span data-stu-id="fedf3-205">C1</span></span>
- <span data-ttu-id="fedf3-206">만족할</span><span class="sxs-lookup"><span data-stu-id="fedf3-206">C2</span></span>
- <span data-ttu-id="fedf3-207">C3</span><span class="sxs-lookup"><span data-stu-id="fedf3-207">C3</span></span>
- <span data-ttu-id="fedf3-208">C4</span><span class="sxs-lookup"><span data-stu-id="fedf3-208">C4</span></span>
- <span data-ttu-id="fedf3-209">C 5</span><span class="sxs-lookup"><span data-stu-id="fedf3-209">C5</span></span>
- <span data-ttu-id="fedf3-210">C6</span><span class="sxs-lookup"><span data-stu-id="fedf3-210">C6</span></span>
- <span data-ttu-id="fedf3-211">250MB</span><span class="sxs-lookup"><span data-stu-id="fedf3-211">250MB</span></span>
- <span data-ttu-id="fedf3-212">1GB</span><span class="sxs-lookup"><span data-stu-id="fedf3-212">1GB</span></span>
- <span data-ttu-id="fedf3-213">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="fedf3-213">2.5GB</span></span>
- <span data-ttu-id="fedf3-214">6GB</span><span class="sxs-lookup"><span data-stu-id="fedf3-214">6GB</span></span>
- <span data-ttu-id="fedf3-215">13GB</span><span class="sxs-lookup"><span data-stu-id="fedf3-215">13GB</span></span>
- <span data-ttu-id="fedf3-216">26GB</span><span class="sxs-lookup"><span data-stu-id="fedf3-216">26GB</span></span>
- <span data-ttu-id="fedf3-217">53GB 기본 값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="fedf3-218">-Sku</span><span class="sxs-lookup"><span data-stu-id="fedf3-218">-Sku</span></span>
<span data-ttu-id="fedf3-219">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="fedf3-220">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-220">Valid values are:</span></span> 
- <span data-ttu-id="fedf3-221">기본적</span><span class="sxs-lookup"><span data-stu-id="fedf3-221">Basic</span></span>
- <span data-ttu-id="fedf3-222">표준이</span><span class="sxs-lookup"><span data-stu-id="fedf3-222">Standard</span></span>
- <span data-ttu-id="fedf3-223">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-223">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="fedf3-224">-StaticIP</span></span>
<span data-ttu-id="fedf3-225">Redis 캐시에 대 한 서브넷의 고유한 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="fedf3-226">이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 서브넷에서 IP 주소를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="fedf3-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fedf3-227">-SubnetId</span></span>
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

### <span data-ttu-id="fedf3-228">태그</span><span class="sxs-lookup"><span data-stu-id="fedf3-228">-Tag</span></span>
<span data-ttu-id="fedf3-229">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-229">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="fedf3-230">-TenantSettings</span></span>
<span data-ttu-id="fedf3-231">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-231">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="fedf3-232">-Zone</span></span>
<span data-ttu-id="fedf3-233">영역 목록.</span><span class="sxs-lookup"><span data-stu-id="fedf3-233">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fedf3-234">-확인</span><span class="sxs-lookup"><span data-stu-id="fedf3-234">-Confirm</span></span>
<span data-ttu-id="fedf3-235">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fedf3-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fedf3-236">-WhatIf</span></span>
<span data-ttu-id="fedf3-237">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fedf3-238">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fedf3-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedf3-239">CommonParameters</span></span>
<span data-ttu-id="fedf3-240">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fedf3-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedf3-241">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fedf3-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedf3-242">입력</span><span class="sxs-lookup"><span data-stu-id="fedf3-242">INPUTS</span></span>

### <span data-ttu-id="fedf3-243">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fedf3-243">System.String</span></span>

### <span data-ttu-id="fedf3-244">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="fedf3-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fedf3-245">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fedf3-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fedf3-246">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="fedf3-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fedf3-247">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="fedf3-247">System.String[]</span></span>

## <span data-ttu-id="fedf3-248">출력</span><span class="sxs-lookup"><span data-stu-id="fedf3-248">OUTPUTS</span></span>

### <span data-ttu-id="fedf3-249">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="fedf3-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="fedf3-250">상속자</span><span class="sxs-lookup"><span data-stu-id="fedf3-250">NOTES</span></span>

## <span data-ttu-id="fedf3-251">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fedf3-251">RELATED LINKS</span></span>

[<span data-ttu-id="fedf3-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fedf3-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="fedf3-253">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fedf3-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="fedf3-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="fedf3-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

