---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 3696b33b18314d58e950fa9786e1febac5c3d22c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876613"
---
# <span data-ttu-id="1f90f-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1f90f-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="1f90f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f90f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f90f-103">Application gateway에 대 한 백 엔드 HTTP 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="1f90f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f90f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f90f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f90f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f90f-106">Set-AzApplicationGatewayBackendHttpSetting cmdlet은 Azure application gateway의 백 엔드 HTTP (하이퍼텍스트 전송 프로토콜) 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="1f90f-107">백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="1f90f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1f90f-108">EXAMPLES</span></span>

### <span data-ttu-id="1f90f-109">예제 1: 응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="1f90f-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="1f90f-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1f90f-111">두 번째 명령은 포트 88, HTTP 프로토콜을 사용 하도록 $AppGw 변수에 있는 응용 프로그램 게이트웨이의 HTTP 설정을 업데이트 하 고 쿠키 기반 선호도를 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="1f90f-112">변수</span><span class="sxs-lookup"><span data-stu-id="1f90f-112">PARAMETERS</span></span>

### <span data-ttu-id="1f90f-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="1f90f-113">-AffinityCookieName</span></span>
<span data-ttu-id="1f90f-114">선호도 쿠키에 사용할 쿠키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="1f90f-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f90f-115">-ApplicationGateway</span></span>
<span data-ttu-id="1f90f-116">이 cmdlet이 백 엔드 HTTP 설정을 연결 하는 데 사용 되는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="1f90f-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="1f90f-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="1f90f-118">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="1f90f-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1f90f-119">-ConnectionDraining</span></span>
<span data-ttu-id="1f90f-120">백 엔드 http 설정 리소스의 연결 드레이닝</span><span class="sxs-lookup"><span data-stu-id="1f90f-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="1f90f-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="1f90f-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="1f90f-122">백 엔드 서버 풀에 대해 쿠키 기반 선호도를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="1f90f-123">이 매개 변수에 허용 되는 값은 사용 되지 않거나 사용 하도록 설정 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="1f90f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f90f-124">-DefaultProfile</span></span>
<span data-ttu-id="1f90f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f90f-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="1f90f-126">-HostName</span></span>
<span data-ttu-id="1f90f-127">백 엔드 서버로 보낼 호스트 헤더를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="1f90f-128">-이름</span><span class="sxs-lookup"><span data-stu-id="1f90f-128">-Name</span></span>
<span data-ttu-id="1f90f-129">백 엔드 HTTP 설정 개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="1f90f-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1f90f-130">-Path</span></span>
<span data-ttu-id="1f90f-131">모든 HTTP 요청에 대 한 접두사로 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="1f90f-132">이 매개 변수에 대 한 값을 제공 하지 않으면 경로에 접두사를 붙일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="1f90f-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="1f90f-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="1f90f-134">백 엔드 서버의 호스트 이름에서 호스트 헤더를 선택 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="1f90f-135">-포트</span><span class="sxs-lookup"><span data-stu-id="1f90f-135">-Port</span></span>
<span data-ttu-id="1f90f-136">백 엔드 서버 풀의 각 서버에 사용할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="1f90f-137">-프로브</span><span class="sxs-lookup"><span data-stu-id="1f90f-137">-Probe</span></span>
<span data-ttu-id="1f90f-138">백 엔드 HTTP 설정과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="1f90f-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="1f90f-139">-ProbeEnabled</span></span>
<span data-ttu-id="1f90f-140">프로브를 사용 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="1f90f-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="1f90f-141">-ProbeId</span></span>
<span data-ttu-id="1f90f-142">백 엔드 HTTP 설정과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="1f90f-143">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="1f90f-143">-Protocol</span></span>
<span data-ttu-id="1f90f-144">응용 프로그램 게이트웨이 및 백 엔드 서버 간 통신에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="1f90f-145">이 매개 변수에 허용 되는 값은 Http 및 Https입니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="1f90f-146">이 매개 변수는 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="1f90f-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="1f90f-147">-RequestTimeout</span></span>
<span data-ttu-id="1f90f-148">요청 시간 초과 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="1f90f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f90f-149">CommonParameters</span></span>
<span data-ttu-id="1f90f-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f90f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f90f-151">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f90f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f90f-152">입력</span><span class="sxs-lookup"><span data-stu-id="1f90f-152">INPUTS</span></span>

### <span data-ttu-id="1f90f-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f90f-153">System.String</span></span>

## <span data-ttu-id="1f90f-154">출력</span><span class="sxs-lookup"><span data-stu-id="1f90f-154">OUTPUTS</span></span>

### <span data-ttu-id="1f90f-155">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f90f-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f90f-156">상속자</span><span class="sxs-lookup"><span data-stu-id="1f90f-156">NOTES</span></span>

## <span data-ttu-id="1f90f-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f90f-157">RELATED LINKS</span></span>

[<span data-ttu-id="1f90f-158">추가-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1f90f-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="1f90f-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1f90f-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="1f90f-160">새로운 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1f90f-160">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="1f90f-161">제거-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1f90f-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()
