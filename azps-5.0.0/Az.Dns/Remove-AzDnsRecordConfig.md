---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: aa67873ba55f815e7fdd8ada4658370c16e65c4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217471"
---
# <span data-ttu-id="b6cee-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b6cee-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="b6cee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6cee-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cee-103">로컬 레코드 집합 개체에서 DNS 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="b6cee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6cee-104">SYNTAX</span></span>

### <span data-ttu-id="b6cee-105">에서</span><span class="sxs-lookup"><span data-stu-id="b6cee-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6cee-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="b6cee-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6cee-107">NS</span><span class="sxs-lookup"><span data-stu-id="b6cee-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cee-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="b6cee-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6cee-109">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="b6cee-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6cee-110">라는</span><span class="sxs-lookup"><span data-stu-id="b6cee-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cee-111">SRV</span><span class="sxs-lookup"><span data-stu-id="b6cee-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6cee-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="b6cee-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6cee-113">Caa</span><span class="sxs-lookup"><span data-stu-id="b6cee-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6cee-114">설명은</span><span class="sxs-lookup"><span data-stu-id="b6cee-114">DESCRIPTION</span></span>
<span data-ttu-id="b6cee-115">**AzDnsRecordConfig** cmdlet은 레코드 집합에서 DNS (Domain Name System) 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="b6cee-116">**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="b6cee-117">레코드를 제거 하려면 해당 레코드 종류에 대 한 모든 필드가 정확히 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="b6cee-118">SOA 레코드를 추가 하거나 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="b6cee-119">SOA 레코드는 dns 영역이 생성 될 때 자동으로 만들어지고 DNS 영역이 삭제 되 면 자동으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="b6cee-120">이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="b6cee-121">예제의</span><span class="sxs-lookup"><span data-stu-id="b6cee-121">EXAMPLES</span></span>

### <span data-ttu-id="b6cee-122">예제 1: 레코드 집합에서 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-123">이 예제에서는 기존 레코드 집합에서 A 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="b6cee-124">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="b6cee-125">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b6cee-126">예제 2: 레코드 집합에서 AAAA 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-127">이 예제에서는 기존 레코드 집합에서 AAAA 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="b6cee-128">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="b6cee-129">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b6cee-130">예제 3: 레코드 집합에서 CNAME 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-131">이 예제에서는 기존 레코드 집합에서 CNAME 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="b6cee-132">CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="b6cee-133">예제 4: 레코드 집합에서 MX 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-134">이 예제에서는 기존 레코드 집합에서 MX 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="b6cee-135">레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="b6cee-136">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b6cee-137">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b6cee-138">예제 5: 레코드 집합에서 NS 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-139">이 예제에서는 기존 레코드 집합에서 NS 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="b6cee-140">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b6cee-141">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b6cee-142">예제 6: 레코드 집합에서 PTR 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-143">이 예제에서는 기존 레코드 집합에서 PTR 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="b6cee-144">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b6cee-145">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b6cee-146">예제 7: 레코드 집합에서 SRV 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-147">이 예제에서는 기존 레코드 집합에서 SRV 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="b6cee-148">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b6cee-149">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="b6cee-150">예제 8: 레코드 집합에서 TXT 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="b6cee-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="b6cee-151">이 예제에서는 기존 레코드 집합에서 TXT 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="b6cee-152">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="b6cee-153">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b6cee-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="b6cee-154">변수</span><span class="sxs-lookup"><span data-stu-id="b6cee-154">PARAMETERS</span></span>

### <span data-ttu-id="b6cee-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="b6cee-155">-CaaFlags</span></span>
<span data-ttu-id="b6cee-156">추가할 CAA 레코드에 대 한 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="b6cee-157">0에서 255 사이의 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-157">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="b6cee-158">-CaaTag</span></span>
<span data-ttu-id="b6cee-159">추가할 CAA 레코드의 tag 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-159">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="b6cee-160">-CaaValue</span></span>
<span data-ttu-id="b6cee-161">추가할 CAA 레코드에 대 한 값 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-161">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-162">-Cname</span><span class="sxs-lookup"><span data-stu-id="b6cee-162">-Cname</span></span>
<span data-ttu-id="b6cee-163">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cee-164">-DefaultProfile</span></span>
<span data-ttu-id="b6cee-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6cee-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6cee-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="b6cee-166">-Exchange</span></span>
<span data-ttu-id="b6cee-167">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="b6cee-168">-Ipv4Address</span></span>
<span data-ttu-id="b6cee-169">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-169">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="b6cee-170">-Ipv6Address</span></span>
<span data-ttu-id="b6cee-171">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-171">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="b6cee-172">-Nsdname</span></span>
<span data-ttu-id="b6cee-173">NS (이름 서버) 레코드에 대 한 이름 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-173">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-174">-포트</span><span class="sxs-lookup"><span data-stu-id="b6cee-174">-Port</span></span>
<span data-ttu-id="b6cee-175">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-175">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-176">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="b6cee-176">-Preference</span></span>
<span data-ttu-id="b6cee-177">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-177">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-178">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="b6cee-178">-Priority</span></span>
<span data-ttu-id="b6cee-179">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-179">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="b6cee-180">-Ptrdname</span></span>
<span data-ttu-id="b6cee-181">포인터 (PTR) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-182">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="b6cee-182">-RecordSet</span></span>
<span data-ttu-id="b6cee-183">제거할 레코드가 포함 된 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-184">-대상</span><span class="sxs-lookup"><span data-stu-id="b6cee-184">-Target</span></span>
<span data-ttu-id="b6cee-185">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-185">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-186">-값</span><span class="sxs-lookup"><span data-stu-id="b6cee-186">-Value</span></span>
<span data-ttu-id="b6cee-187">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-187">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-188">-중량</span><span class="sxs-lookup"><span data-stu-id="b6cee-188">-Weight</span></span>
<span data-ttu-id="b6cee-189">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-189">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6cee-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cee-190">CommonParameters</span></span>
<span data-ttu-id="b6cee-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6cee-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cee-192">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6cee-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cee-193">입력</span><span class="sxs-lookup"><span data-stu-id="b6cee-193">INPUTS</span></span>

### <span data-ttu-id="b6cee-194">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b6cee-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="b6cee-195">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b6cee-195">System.String</span></span>

### <span data-ttu-id="b6cee-196">시스템 UInt16</span><span class="sxs-lookup"><span data-stu-id="b6cee-196">System.UInt16</span></span>

### <span data-ttu-id="b6cee-197">시스템 바이트</span><span class="sxs-lookup"><span data-stu-id="b6cee-197">System.Byte</span></span>

## <span data-ttu-id="b6cee-198">출력</span><span class="sxs-lookup"><span data-stu-id="b6cee-198">OUTPUTS</span></span>

### <span data-ttu-id="b6cee-199">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b6cee-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b6cee-200">상속자</span><span class="sxs-lookup"><span data-stu-id="b6cee-200">NOTES</span></span>

## <span data-ttu-id="b6cee-201">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6cee-201">RELATED LINKS</span></span>

[<span data-ttu-id="b6cee-202">추가-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b6cee-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="b6cee-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b6cee-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="b6cee-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b6cee-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)