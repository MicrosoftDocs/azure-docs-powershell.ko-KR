---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 3cf1bea87824320b659def722d0d0f0166fa177d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339386"
---
# <span data-ttu-id="bee18-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bee18-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="bee18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee18-102">SYNOPSIS</span></span>
<span data-ttu-id="bee18-103">VPN 루트 인증서에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="bee18-104">구문</span><span class="sxs-lookup"><span data-stu-id="bee18-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bee18-105">설명</span><span class="sxs-lookup"><span data-stu-id="bee18-105">DESCRIPTION</span></span>
<span data-ttu-id="bee18-106">**Get-AzVpnClientRootCertificate** cmdlet은 가상 네트워크 게이트웨이에 할당된 루트 인증서에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="bee18-107">루트 인증서는 루트 인증 기관을 식별하는 X.509 인증서입니다. 게이트웨이에서 사용되는 다른 모든 인증서는 루트 인증서를 신뢰합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="bee18-108">기본적으로 **Get-AzVpnClientRootCertificate는** 게이트웨이에 할당된 모든 루트 인증서에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="bee18-109">(게이트웨이에는 루트 인증서가 두 개 이상일 수 있습니다.) 그러나 **VpnClientRootCertificateName** 매개 변수를 포함하면 반환된 데이터를 특정 인증서로 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="bee18-110">예제</span><span class="sxs-lookup"><span data-stu-id="bee18-110">EXAMPLES</span></span>

### <span data-ttu-id="bee18-111">예제 1: 모든 루트 인증서에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="bee18-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="bee18-112">이 명령은 ContosoVirtualNetwork라는 가상 네트워크 게이트웨이에 할당된 모든 루트 인증서에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="bee18-113">예제 2: 특정 루트 인증서에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="bee18-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="bee18-114">이 명령은 예제 1에 표시된 명령의 변형입니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="bee18-115">그러나 이 경우 반환된 데이터를 특정 루트 인증서인 ContosoRootClientCertificate로 제한하기 위해 *VpnClientRootCertificateName* 매개 변수가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="bee18-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bee18-116">PARAMETERS</span></span>

### <span data-ttu-id="bee18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee18-117">-DefaultProfile</span></span>
<span data-ttu-id="bee18-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bee18-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee18-119">-ResourceGroupName</span></span>
<span data-ttu-id="bee18-120">가상 네트워크 게이트웨이가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="bee18-121">리소스 그룹은 재고 관리 및 일반 Azure 관리를 간소화하는 데 도움이 되는 항목을 분류합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bee18-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bee18-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bee18-123">루트 인증서가 할당된 가상 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="bee18-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="bee18-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="bee18-125">이 cmdlet이 얻을 클라이언트 루트 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee18-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee18-126">CommonParameters</span></span>
<span data-ttu-id="bee18-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bee18-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee18-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bee18-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee18-129">입력</span><span class="sxs-lookup"><span data-stu-id="bee18-129">INPUTS</span></span>

### <span data-ttu-id="bee18-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bee18-130">System.String</span></span>

## <span data-ttu-id="bee18-131">출력</span><span class="sxs-lookup"><span data-stu-id="bee18-131">OUTPUTS</span></span>

### <span data-ttu-id="bee18-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bee18-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="bee18-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bee18-133">NOTES</span></span>

## <span data-ttu-id="bee18-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bee18-134">RELATED LINKS</span></span>

[<span data-ttu-id="bee18-135">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bee18-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="bee18-136">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bee18-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="bee18-137">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bee18-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)

