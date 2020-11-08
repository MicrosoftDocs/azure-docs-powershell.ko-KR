---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217219"
---
# <span data-ttu-id="8f3ba-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8f3ba-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="8f3ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3ba-103">피어 링을 만들거나 수정 하는 데 사용할 메모리 PSObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="8f3ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f3ba-104">SYNTAX</span></span>

### <span data-ttu-id="8f3ba-105">IPv4Address (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f3ba-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f3ba-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="8f3ba-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f3ba-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="8f3ba-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f3ba-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8f3ba-108">DESCRIPTION</span></span>
<span data-ttu-id="8f3ba-109">메모리 PSObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="8f3ba-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8f3ba-110">EXAMPLES</span></span>

### <span data-ttu-id="8f3ba-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8f3ba-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="8f3ba-112">로컬 연결 개체</span><span class="sxs-lookup"><span data-stu-id="8f3ba-112">Local connection object</span></span>

## <span data-ttu-id="8f3ba-113">변수</span><span class="sxs-lookup"><span data-stu-id="8f3ba-113">PARAMETERS</span></span>

### <span data-ttu-id="8f3ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3ba-114">-DefaultProfile</span></span>
<span data-ttu-id="8f3ba-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f3ba-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="8f3ba-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="8f3ba-117">알려진 최대 IPv4</span><span class="sxs-lookup"><span data-stu-id="8f3ba-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3ba-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="8f3ba-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="8f3ba-119">알려진 최대 IPv6</span><span class="sxs-lookup"><span data-stu-id="8f3ba-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3ba-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="8f3ba-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="8f3ba-121">세션에 대 한 MD5 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-121">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3ba-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="8f3ba-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="8f3ba-123">에서 찾은 피어 링 기능 Id https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="8f3ba-123">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3ba-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="8f3ba-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="8f3ba-125">피어 세션 IPv4 주소</span><span class="sxs-lookup"><span data-stu-id="8f3ba-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3ba-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="8f3ba-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="8f3ba-127">피어 세션 IPv6 주소</span><span class="sxs-lookup"><span data-stu-id="8f3ba-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3ba-128">CommonParameters</span></span>
<span data-ttu-id="8f3ba-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3ba-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3ba-131">입력</span><span class="sxs-lookup"><span data-stu-id="8f3ba-131">INPUTS</span></span>

### <span data-ttu-id="8f3ba-132">않아야</span><span class="sxs-lookup"><span data-stu-id="8f3ba-132">None</span></span>

## <span data-ttu-id="8f3ba-133">출력</span><span class="sxs-lookup"><span data-stu-id="8f3ba-133">OUTPUTS</span></span>

### <span data-ttu-id="8f3ba-134">PSExchangeConnection (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8f3ba-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="8f3ba-135">상속자</span><span class="sxs-lookup"><span data-stu-id="8f3ba-135">NOTES</span></span>

## <span data-ttu-id="8f3ba-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f3ba-136">RELATED LINKS</span></span>