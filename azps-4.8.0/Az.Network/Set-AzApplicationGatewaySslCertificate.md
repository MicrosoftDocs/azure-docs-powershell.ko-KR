---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0fa72c48693335dd3df6ab3c1cf8040c5343cc84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048843"
---
# <span data-ttu-id="e6427-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e6427-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e6427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6427-102">SYNOPSIS</span></span>
<span data-ttu-id="e6427-103">Application gateway에 대 한 SSL 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-103">Updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="e6427-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6427-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6427-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e6427-105">DESCRIPTION</span></span>
<span data-ttu-id="e6427-106">**AzApplicationGatewaySslCertificate** cmdlet은 응용 프로그램 게이트웨이에 대 한 SSL 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet updates an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="e6427-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e6427-107">EXAMPLES</span></span>

### <span data-ttu-id="e6427-108">예제 1: 응용 프로그램 게이트웨이에서 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="e6427-108">Example 1: Update an existing SSL certificate on Application Gateway</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e6427-109">ApplicationGateway01 라는 응용 프로그램 게이트웨이에 대 한 기존 SSL 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-109">Update an existing SSL certificate for the application gateway named ApplicationGateway01.</span></span>

### <span data-ttu-id="e6427-110">예제 2: 응용 프로그램 게이트웨이에서 KeyVault 비밀 (버전-less secretId)을 사용 하 여 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="e6427-110">Example 2: Update an existing SSL certificate using KeyVault Secret (version-less secretId) on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e6427-111">를 사용 하 여 기존 SSL 인증서를 업데이트 하 고 암호를 가져옵니다 `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="e6427-111">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>

### <span data-ttu-id="e6427-112">예제 3: 응용 프로그램 게이트웨이에서 KeyVault 비밀을 사용 하 여 기존 SSL 인증서 업데이트</span><span class="sxs-lookup"><span data-stu-id="e6427-112">Example 3: Update an existing SSL certificate using KeyVault Secret on Application Gateway</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="e6427-113">를 사용 하 여 기존 SSL 인증서를 업데이트 하 고 암호를 가져옵니다 `Set-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="e6427-113">Get the secret and update an existing SSL Certificate using `Set-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="e6427-114">참고: Application Gateway가 KeyVault와 인증서를 동기화 해야 하는 경우에는 버전을 더 적게 secretId을 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="e6427-114">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="e6427-115">변수</span><span class="sxs-lookup"><span data-stu-id="e6427-115">PARAMETERS</span></span>

### <span data-ttu-id="e6427-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6427-116">-ApplicationGateway</span></span>
<span data-ttu-id="e6427-117">SSL (Secure Socket Layer) 인증서가 연결 되는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-117">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6427-118">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e6427-118">-CertificateFile</span></span>
<span data-ttu-id="e6427-119">SSL 인증서의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-119">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="e6427-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6427-120">-DefaultProfile</span></span>
<span data-ttu-id="e6427-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6427-122">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="e6427-122">-KeyVaultSecretId</span></span>
<span data-ttu-id="e6427-123">KeyVault 비밀에 대 한 SecretId (uri)입니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-123">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="e6427-124">특정 버전의 비밀을 사용 해야 하는 경우이 옵션을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-124">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="e6427-125">-이름</span><span class="sxs-lookup"><span data-stu-id="e6427-125">-Name</span></span>
<span data-ttu-id="e6427-126">SSL 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-126">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="e6427-127">-암호</span><span class="sxs-lookup"><span data-stu-id="e6427-127">-Password</span></span>
<span data-ttu-id="e6427-128">SSL 인증서의 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-128">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6427-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6427-129">CommonParameters</span></span>
<span data-ttu-id="e6427-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6427-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6427-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6427-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6427-132">입력</span><span class="sxs-lookup"><span data-stu-id="e6427-132">INPUTS</span></span>

### <span data-ttu-id="e6427-133">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6427-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6427-134">출력</span><span class="sxs-lookup"><span data-stu-id="e6427-134">OUTPUTS</span></span>

### <span data-ttu-id="e6427-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6427-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6427-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e6427-136">NOTES</span></span>

## <span data-ttu-id="e6427-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6427-137">RELATED LINKS</span></span>

[<span data-ttu-id="e6427-138">추가-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e6427-138">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e6427-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e6427-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e6427-140">새로운 AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e6427-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e6427-141">제거-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e6427-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

