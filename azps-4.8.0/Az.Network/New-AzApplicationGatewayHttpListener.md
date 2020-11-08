---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211593"
---
# <span data-ttu-id="ac577-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac577-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ac577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac577-102">SYNOPSIS</span></span>
<span data-ttu-id="ac577-103">응용 프로그램 게이트웨이에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="ac577-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac577-104">SYNTAX</span></span>

### <span data-ttu-id="ac577-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac577-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac577-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ac577-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac577-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ac577-107">DESCRIPTION</span></span>
<span data-ttu-id="ac577-108">**AzApplicationGatewayHttpListener** Cmdlet은 Azure application gateway에 대 한 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ac577-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ac577-109">EXAMPLES</span></span>

### <span data-ttu-id="ac577-110">예제 1: HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="ac577-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="ac577-111">이 명령은 Listener01 이라는 HTTP 수신기를 만들고 결과를 명명 된 변수 $Listener에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ac577-112">예제 2: SSL을 사용 하 여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="ac577-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ac577-113">이 명령은 SSL 오프 로드를 사용 하 고 $SSLCert 01 변수에 SSL 인증서를 제공 하는 HTTP 수신기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="ac577-114">이 명령은 $Listener 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ac577-115">예제 3: 방화벽 정책을 사용 하 여 HTTP 수신기 만들기</span><span class="sxs-lookup"><span data-stu-id="ac577-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="ac577-116">이 명령은 Listener01 이라는 HTTP 수신기를 만들고, FirewallPolicy로 $firewallPolicy 하 고, 결과를 $Listener 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ac577-117">예제 4: SSL 및 호스트 이름을 사용 하 여 HTTPS 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="ac577-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="ac577-118">이 명령은 SSL 오프 로드를 사용 하는 HTTP 수신기를 만들고 $SSLCert 01 변수에는 두 개의 호스트 이름과 SSL 인증서를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="ac577-119">이 명령은 $Listener 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="ac577-120">변수</span><span class="sxs-lookup"><span data-stu-id="ac577-120">PARAMETERS</span></span>

### <span data-ttu-id="ac577-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac577-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="ac577-122">Application gateway의 고객 오류</span><span class="sxs-lookup"><span data-stu-id="ac577-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac577-123">-DefaultProfile</span></span>
<span data-ttu-id="ac577-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac577-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ac577-125">-FirewallPolicy</span></span>
<span data-ttu-id="ac577-126">최상위 수준의 방화벽 정책에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="ac577-127">New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet을 사용 하 여 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="ac577-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" 위를 사용 하 여 만든 방화벽 정책은 경로 규칙 수준에서 참조 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="ac577-129">위의 명령으로 기본 정책 설정 및 관리 되는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="ac577-130">기본값 대신 사용자는 각각 New-AzApplicationGatewayFirewallPolicySettings 및 New-AzApplicationGatewayFirewallPolicyManagedRules을 사용 하 여 PolicySettings, ManagedRules를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ac577-131">-FirewallPolicyId</span></span>
<span data-ttu-id="ac577-132">기존 상위 수준 웹 응용 프로그램 방화벽 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="ac577-133">방화벽 정책 Id는 Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet을 사용 하 여 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="ac577-134">ID를 설정한 후에는 *FirewallPolicy* 매개 변수 대신 *FirewallPolicyId* 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="ac577-135">예를 들어-FirewallPolicyId/subscriptions/<구독 id>/Resourcegroup/<리소스 그룹-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="ac577-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac577-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ac577-137">HTTP 수신기에 대 한 프런트 엔드 IP 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ac577-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ac577-139">HTTP 수신기에 대 한 프런트 엔드 IP 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ac577-140">-FrontendPort</span></span>
<span data-ttu-id="ac577-141">HTTP 수신기에 대 한 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ac577-142">-FrontendPortId</span></span>
<span data-ttu-id="ac577-143">HTTP 수신기에 대 한 프런트 엔드 포트 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="ac577-144">-HostName</span></span>
<span data-ttu-id="ac577-145">Application gateway HTTP 수신기의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="ac577-146">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ac577-146">-HostNames</span></span>
<span data-ttu-id="ac577-147">호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ac577-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-148">-이름</span><span class="sxs-lookup"><span data-stu-id="ac577-148">-Name</span></span>
<span data-ttu-id="ac577-149">이 cmdlet이 만드는 HTTP 수신기의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ac577-150">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="ac577-150">-Protocol</span></span>
<span data-ttu-id="ac577-151">HTTP 수신기가 사용 하는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ac577-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ac577-153">-SslCertificate</span></span>
<span data-ttu-id="ac577-154">HTTP 수신기에 대 한 SSL 인증서 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ac577-155">-SslCertificateId</span></span>
<span data-ttu-id="ac577-156">HTTP 수신기에 대 한 SSL 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac577-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac577-157">CommonParameters</span></span>
<span data-ttu-id="ac577-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac577-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac577-159">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac577-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac577-160">입력</span><span class="sxs-lookup"><span data-stu-id="ac577-160">INPUTS</span></span>

### <span data-ttu-id="ac577-161">않아야</span><span class="sxs-lookup"><span data-stu-id="ac577-161">None</span></span>

## <span data-ttu-id="ac577-162">출력</span><span class="sxs-lookup"><span data-stu-id="ac577-162">OUTPUTS</span></span>

### <span data-ttu-id="ac577-163">PSApplicationGatewayHttpListener에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ac577-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ac577-164">상속자</span><span class="sxs-lookup"><span data-stu-id="ac577-164">NOTES</span></span>

## <span data-ttu-id="ac577-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac577-165">RELATED LINKS</span></span>

[<span data-ttu-id="ac577-166">추가-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac577-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac577-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac577-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac577-168">제거-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac577-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ac577-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ac577-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

