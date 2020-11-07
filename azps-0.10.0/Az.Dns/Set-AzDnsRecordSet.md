---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1b2ee31c136c24478ddd69d58c264ce44886c057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875955"
---
# <span data-ttu-id="59238-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59238-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="59238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59238-102">SYNOPSIS</span></span>
<span data-ttu-id="59238-103">DNS 레코드 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="59238-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59238-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59238-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59238-105">DESCRIPTION</span></span>
<span data-ttu-id="59238-106">**AzDnsRecordSet** cmdlet은 로컬 **RecordSet** 개체에서 Azure DNS 서비스의 레코드 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>

<span data-ttu-id="59238-107">**레코드 집합** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>

<span data-ttu-id="59238-108">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="59238-109">로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 된 경우에는 해당 레코드가 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="59238-110">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="59238-111">동시 변경 내용에 관계 없이 레코드 집합을 업데이트 하는 *Overwrite* 매개 변수를 사용 하 여이 동작을 억제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="59238-112">예제의</span><span class="sxs-lookup"><span data-stu-id="59238-112">EXAMPLES</span></span>

### <span data-ttu-id="59238-113">예제 1: 레코드 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="59238-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="59238-114">첫 번째 명령은 Get-AzDnsRecordSet cmdlet을 사용 하 여 지정 된 레코드 집합을 얻은 다음 $RecordSet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="59238-115">두 번째 및 세 번째 명령은 레코드 집합에 두 개의 레코드를 추가 하는 오프 라인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="59238-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>

<span data-ttu-id="59238-116">마지막 명령은 **Set-AzDnsRecordSet** cmdlet을 사용 하 여 업데이트를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="59238-117">예제 2: SOA 레코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="59238-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="59238-118">첫 번째 명령은 **AzDnsRecordset** cmdlet을 사용 하 여 지정 된 레코드 집합을 얻은 다음 $RecordSet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>

<span data-ttu-id="59238-119">두 번째 명령은 $RecordSet에서 지정 된 SOA 레코드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-119">The second command updates the specified SOA record in $RecordSet.</span></span>

<span data-ttu-id="59238-120">마지막 명령은 **Set-AzDnsRecordSet** cmdlet을 사용 하 여 $RecordSet에서 업데이트를 전파 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="59238-121">변수</span><span class="sxs-lookup"><span data-stu-id="59238-121">PARAMETERS</span></span>

### <span data-ttu-id="59238-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="59238-122">-Overwrite</span></span>
<span data-ttu-id="59238-123">동시 변경 내용에 관계 없이 레코드 집합을 업데이트 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59238-123">Indicates to update the record set regardless of concurrent changes.</span></span>

<span data-ttu-id="59238-124">로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-124">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="59238-125">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-125">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="59238-126">이 동작을 생략 하려면 *Overwrite* 매개 변수를 사용 하 여 동시 변경 내용에 관계 없이 레코드 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-126">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59238-127">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="59238-127">-RecordSet</span></span>
<span data-ttu-id="59238-128">업데이트할 **레코드 집합** 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-128">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59238-129">-확인</span><span class="sxs-lookup"><span data-stu-id="59238-129">-Confirm</span></span>
<span data-ttu-id="59238-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59238-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59238-131">-WhatIf</span></span>
<span data-ttu-id="59238-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59238-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59238-133">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59238-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59238-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59238-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59238-135">CommonParameters</span></span>
<span data-ttu-id="59238-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59238-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59238-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59238-138">입력</span><span class="sxs-lookup"><span data-stu-id="59238-138">INPUTS</span></span>

### <span data-ttu-id="59238-139">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59238-139">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="59238-140">이 cmdlet에 **RecordSet** 개체를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-140">You can pass a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="59238-141">출력</span><span class="sxs-lookup"><span data-stu-id="59238-141">OUTPUTS</span></span>

### <span data-ttu-id="59238-142">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59238-142">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="59238-143">이 cmdlet은 업데이트 된 **레코드 집합** 개체를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-143">This cmdlet returns an object that represents the updated **RecordSet** object.</span></span>

## <span data-ttu-id="59238-144">상속자</span><span class="sxs-lookup"><span data-stu-id="59238-144">NOTES</span></span>
<span data-ttu-id="59238-145">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="59238-146">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59238-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="59238-147">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59238-147">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="59238-148">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59238-148">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="59238-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59238-149">RELATED LINKS</span></span>

[<span data-ttu-id="59238-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59238-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="59238-151">새로운 AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59238-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="59238-152">제거-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59238-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)