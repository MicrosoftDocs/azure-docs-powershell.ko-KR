---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: 94375ba7d54095af131d7a61c7b06d50e2ba9521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330705"
---
# <span data-ttu-id="7b920-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7b920-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="7b920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b920-102">SYNOPSIS</span></span>
<span data-ttu-id="7b920-103">개인 링크 서비스 IP 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="7b920-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b920-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b920-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b920-105">DESCRIPTION</span></span>
<span data-ttu-id="7b920-106">**New-AzPrivateLinkServiceIpConfig** cmdlet은 개인 링크 서비스 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="7b920-107">이 구성은 개인 엔드포인트에서 들어오는 트래픽을 원본 NAT에 수신하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="7b920-108">예제</span><span class="sxs-lookup"><span data-stu-id="7b920-108">EXAMPLES</span></span>

### <span data-ttu-id="7b920-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b920-109">Example 1</span></span>
```powershell
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="7b920-110">이 예제에서는 메모리에 개인 링크 서비스 IP 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-110">This example create a private link service ip configuration in memory.</span></span>

### <span data-ttu-id="7b920-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="7b920-111">Example 2</span></span>

<span data-ttu-id="7b920-112">개인 링크 서비스 IP 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-112">Create a private link service ip configuration.</span></span> <span data-ttu-id="7b920-113">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="7b920-113">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -PrivateIpAddress '10.0.0.5' -Subnet <PSSubnet>
```

## <span data-ttu-id="7b920-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b920-114">PARAMETERS</span></span>

### <span data-ttu-id="7b920-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b920-115">-DefaultProfile</span></span>
<span data-ttu-id="7b920-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b920-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7b920-117">-Name</span></span>
<span data-ttu-id="7b920-118">IpConfiguration의 이름</span><span class="sxs-lookup"><span data-stu-id="7b920-118">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="7b920-119">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b920-119">-PrivateIpAddress</span></span>
<span data-ttu-id="7b920-120">고정 할당이 지정된 경우 ipConfiguration의 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-120">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

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

### <span data-ttu-id="7b920-121">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7b920-121">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7b920-122">IP 구성의 IP 버전</span><span class="sxs-lookup"><span data-stu-id="7b920-122">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b920-123">-Primary</span><span class="sxs-lookup"><span data-stu-id="7b920-123">-Primary</span></span>
<span data-ttu-id="7b920-124">현재 IP 구성이 기본 구성인지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-124">Indicate current ip configuration is primary or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b920-125">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7b920-125">-Subnet</span></span>
<span data-ttu-id="7b920-126">서브넷</span><span class="sxs-lookup"><span data-stu-id="7b920-126">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b920-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b920-127">CommonParameters</span></span>
<span data-ttu-id="7b920-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b920-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b920-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7b920-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b920-130">입력</span><span class="sxs-lookup"><span data-stu-id="7b920-130">INPUTS</span></span>

### <span data-ttu-id="7b920-131">없음</span><span class="sxs-lookup"><span data-stu-id="7b920-131">None</span></span>

## <span data-ttu-id="7b920-132">출력</span><span class="sxs-lookup"><span data-stu-id="7b920-132">OUTPUTS</span></span>

### <span data-ttu-id="7b920-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b920-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="7b920-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b920-134">NOTES</span></span>

## <span data-ttu-id="7b920-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b920-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b920-136">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7b920-136">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)