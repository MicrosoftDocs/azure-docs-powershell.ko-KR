---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 4361d025026e3ff9c9a72a092a99a72b8b63c850
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875705"
---
# <span data-ttu-id="a7965-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7965-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="a7965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7965-102">SYNOPSIS</span></span>
<span data-ttu-id="a7965-103">응용 프로그램 게이트웨이에 백 엔드 HTTP 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="a7965-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7965-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7965-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7965-105">DESCRIPTION</span></span>
<span data-ttu-id="a7965-106">Add-AzApplicationGatewayBackendHttpSetting cmdlet은 응용 프로그램 게이트웨이에 백 엔드 HTTP 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="a7965-107">백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="a7965-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a7965-108">EXAMPLES</span></span>

### <span data-ttu-id="a7965-109">예제 1: 응용 프로그램 게이트웨이에 백 엔드 HTTP 설정 추가</span><span class="sxs-lookup"><span data-stu-id="a7965-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="a7965-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정을 추가 하 고, 포트를 88로 설정 하 고, 프로토콜을 HTTP로 설정한 다음, 설정의 이름을 Setting02.</span><span class="sxs-lookup"><span data-stu-id="a7965-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="a7965-111">변수</span><span class="sxs-lookup"><span data-stu-id="a7965-111">PARAMETERS</span></span>

### <span data-ttu-id="a7965-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="a7965-112">-AffinityCookieName</span></span>
<span data-ttu-id="a7965-113">선호도 쿠키에 사용할 쿠키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-113">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7965-114">-ApplicationGateway</span></span>
<span data-ttu-id="a7965-115">이 cmdlet이 설정을 추가 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="a7965-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="a7965-117">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a7965-118">-ConnectionDraining</span></span>
<span data-ttu-id="a7965-119">백 엔드 http 설정 리소스의 연결 드레이닝</span><span class="sxs-lookup"><span data-stu-id="a7965-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="a7965-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="a7965-121">백 엔드 서버 풀에 대해 쿠키 기반 선호도를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="a7965-122">이 매개 변수에 허용 되는 값은 Disabled, Enabled입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7965-123">-DefaultProfile</span></span>
<span data-ttu-id="a7965-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="a7965-125">-HostName</span></span>
<span data-ttu-id="a7965-126">백 엔드 서버로 보낼 호스트 헤더를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-126">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-127">-이름</span><span class="sxs-lookup"><span data-stu-id="a7965-127">-Name</span></span>
<span data-ttu-id="a7965-128">이 cmdlet이 추가 하는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-129">-Path</span><span class="sxs-lookup"><span data-stu-id="a7965-129">-Path</span></span>
<span data-ttu-id="a7965-130">모든 HTTP 요청에 대 한 접두사로 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="a7965-131">이 매개 변수에 대 한 값을 제공 하지 않으면 경로에 접두사를 붙일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="a7965-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="a7965-133">백 엔드 서버의 호스트 이름에서 호스트 헤더를 선택 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="a7965-134">-포트</span><span class="sxs-lookup"><span data-stu-id="a7965-134">-Port</span></span>
<span data-ttu-id="a7965-135">백 엔드 서버 풀의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-136">-프로브</span><span class="sxs-lookup"><span data-stu-id="a7965-136">-Probe</span></span>
<span data-ttu-id="a7965-137">백 엔드 서버와 연결 되는 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="a7965-138">-ProbeEnabled</span></span>
<span data-ttu-id="a7965-139">프로브를 사용 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-139">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="a7965-140">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a7965-140">-ProbeId</span></span>
<span data-ttu-id="a7965-141">백 엔드 서버와 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-142">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="a7965-142">-Protocol</span></span>
<span data-ttu-id="a7965-143">응용 프로그램 게이트웨이 및 백 엔드 서버 간 통신을 위한 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="a7965-144">이 매개 변수에 허용 되는 값은 Http 및 Https입니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-144">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="a7965-145">-RequestTimeout</span></span>
<span data-ttu-id="a7965-146">요청 시간 초과 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-146">Specifies the request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7965-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7965-147">CommonParameters</span></span>
<span data-ttu-id="a7965-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7965-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7965-149">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7965-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7965-150">입력</span><span class="sxs-lookup"><span data-stu-id="a7965-150">INPUTS</span></span>

### <span data-ttu-id="a7965-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7965-151">System.String</span></span>

## <span data-ttu-id="a7965-152">출력</span><span class="sxs-lookup"><span data-stu-id="a7965-152">OUTPUTS</span></span>

### <span data-ttu-id="a7965-153">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7965-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7965-154">상속자</span><span class="sxs-lookup"><span data-stu-id="a7965-154">NOTES</span></span>

## <span data-ttu-id="a7965-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7965-155">RELATED LINKS</span></span>

[<span data-ttu-id="a7965-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7965-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="a7965-157">새로운 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7965-157">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="a7965-158">제거-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7965-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="a7965-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a7965-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()
