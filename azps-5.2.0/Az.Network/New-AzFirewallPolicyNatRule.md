---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329489"
---
# <span data-ttu-id="8c94a-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="8c94a-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="8c94a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c94a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c94a-103">새 Azure Firewall 정책 NAT 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="8c94a-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="8c94a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c94a-104">SYNTAX</span></span>

### <span data-ttu-id="8c94a-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="8c94a-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c94a-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="8c94a-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c94a-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="8c94a-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c94a-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="8c94a-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c94a-109">설명</span><span class="sxs-lookup"><span data-stu-id="8c94a-109">DESCRIPTION</span></span>
<span data-ttu-id="8c94a-110">**New-AzFirewallPolicyNatRule** cmdlet은 Azure Firewall 정책에 대한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="8c94a-111">예제</span><span class="sxs-lookup"><span data-stu-id="8c94a-111">EXAMPLES</span></span>

### <span data-ttu-id="8c94a-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8c94a-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="8c94a-113">이 예제에서는 원본 주소, 프로토콜, 대상 주소, 대상 포트, 변환된 주소 및 변환된 포트를 사용하여 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="8c94a-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="8c94a-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="8c94a-115">이 예제에서는 원본 주소, 프로토콜, 대상 주소, 대상 포트, 변환된 fqdn 및 변환된 포트를 사용하여 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="8c94a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c94a-116">PARAMETERS</span></span>

### <span data-ttu-id="8c94a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c94a-117">-DefaultProfile</span></span>
<span data-ttu-id="8c94a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c94a-119">-Description</span><span class="sxs-lookup"><span data-stu-id="8c94a-119">-Description</span></span>
<span data-ttu-id="8c94a-120">규칙에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="8c94a-120">The description of the rule</span></span>

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

### <span data-ttu-id="8c94a-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8c94a-121">-DestinationAddress</span></span>
<span data-ttu-id="8c94a-122">규칙의 대상 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-122">The destination addresses of the rule.</span></span> <span data-ttu-id="8c94a-123">방화벽의 공용 IP가 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8c94a-124">-DestinationPort</span></span>
<span data-ttu-id="8c94a-125">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="8c94a-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8c94a-126">-Name</span></span>
<span data-ttu-id="8c94a-127">NAT 규칙 컬렉션의 이름</span><span class="sxs-lookup"><span data-stu-id="8c94a-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="8c94a-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8c94a-128">-Protocol</span></span>
<span data-ttu-id="8c94a-129">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="8c94a-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="8c94a-130">-SourceAddress</span></span>
<span data-ttu-id="8c94a-131">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="8c94a-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="8c94a-132">-SourceIpGroup</span></span>
<span data-ttu-id="8c94a-133">규칙의 원본 ipgroups</span><span class="sxs-lookup"><span data-stu-id="8c94a-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="8c94a-134">-TranslatedAddress</span></span>
<span data-ttu-id="8c94a-135">이 NAT 규칙에 대한 번역된 주소</span><span class="sxs-lookup"><span data-stu-id="8c94a-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="8c94a-136">-TranslatedFqdn</span></span>
<span data-ttu-id="8c94a-137">이 NAT 규칙에 대한 번역된 FQDN</span><span class="sxs-lookup"><span data-stu-id="8c94a-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c94a-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="8c94a-138">-TranslatedPort</span></span>
<span data-ttu-id="8c94a-139">이 NAT 규칙에 대한 변환된 포트</span><span class="sxs-lookup"><span data-stu-id="8c94a-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="8c94a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c94a-140">CommonParameters</span></span>
<span data-ttu-id="8c94a-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c94a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c94a-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c94a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c94a-143">입력</span><span class="sxs-lookup"><span data-stu-id="8c94a-143">INPUTS</span></span>

### <span data-ttu-id="8c94a-144">없음</span><span class="sxs-lookup"><span data-stu-id="8c94a-144">None</span></span>

## <span data-ttu-id="8c94a-145">출력</span><span class="sxs-lookup"><span data-stu-id="8c94a-145">OUTPUTS</span></span>

### <span data-ttu-id="8c94a-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="8c94a-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="8c94a-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c94a-147">NOTES</span></span>

## <span data-ttu-id="8c94a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c94a-148">RELATED LINKS</span></span>