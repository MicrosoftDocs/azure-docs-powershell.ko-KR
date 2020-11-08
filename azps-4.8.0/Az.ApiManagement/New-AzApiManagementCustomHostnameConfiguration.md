---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047998"
---
# <span data-ttu-id="67d6e-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="67d6e-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="67d6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="67d6e-103">의 인스턴스를 만듭니다 `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="67d6e-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="67d6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67d6e-104">SYNTAX</span></span>

### <span data-ttu-id="67d6e-105">NoChangeCertificate (기본값)</span><span class="sxs-lookup"><span data-stu-id="67d6e-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d6e-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="67d6e-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d6e-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="67d6e-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d6e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="67d6e-108">DESCRIPTION</span></span>
<span data-ttu-id="67d6e-109">**AzApiManagementCustomHostnameConfiguration** Cmdlet은 **PsApiManagementCustomHostNameConfiguration** 의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="67d6e-110">이 명령은 New-AzApiManagement 및 Set-AzApiManagement cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="67d6e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="67d6e-111">EXAMPLES</span></span>

### <span data-ttu-id="67d6e-112">예제 1: 파일의 Ssl 인증서를 사용 하 여 PsApiManagementCustomHostNameConfiguration의 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="67d6e-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="67d6e-113">이 명령은 포털에 대 한 **PsApiManagementCustomHostNameConfiguration** 의 인스턴스를 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="67d6e-114">그런 다음 사용자 지정 호스트 이름 구성을 사용 하 여 새 ApiManagement 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="67d6e-115">예제 2: KeyVault 리소스의 비밀을 사용 하 여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="67d6e-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="67d6e-116">이 명령은 **PsApiManagementCustomHostNameConfiguration** 의 인스턴스를 만들고 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="67d6e-117">변수</span><span class="sxs-lookup"><span data-stu-id="67d6e-117">PARAMETERS</span></span>

### <span data-ttu-id="67d6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d6e-118">-DefaultProfile</span></span>
<span data-ttu-id="67d6e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d6e-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="67d6e-120">-DefaultSslBinding</span></span>
<span data-ttu-id="67d6e-121">값이 비밀이 고 암호화 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="67d6e-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-122">This parameter is optional.</span></span>
<span data-ttu-id="67d6e-123">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-123">Default Value is false.</span></span>

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

### <span data-ttu-id="67d6e-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="67d6e-124">-Hostname</span></span>
<span data-ttu-id="67d6e-125">사용자 지정 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="67d6e-125">Custom Hostname</span></span>

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

### <span data-ttu-id="67d6e-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="67d6e-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="67d6e-127">기존 인증서 구성.</span><span class="sxs-lookup"><span data-stu-id="67d6e-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d6e-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="67d6e-128">-HostnameType</span></span>
<span data-ttu-id="67d6e-129">호스트 이름 유형</span><span class="sxs-lookup"><span data-stu-id="67d6e-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d6e-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="67d6e-130">-KeyVaultId</span></span>
<span data-ttu-id="67d6e-131">사용자 지정 SSL 인증서를 저장 하는 비밀으로 KeyVaultId.</span><span class="sxs-lookup"><span data-stu-id="67d6e-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d6e-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="67d6e-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="67d6e-133">값이 비밀이 고 암호화 해야 하는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="67d6e-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-134">This parameter is optional.</span></span>
<span data-ttu-id="67d6e-135">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-135">Default Value is false.</span></span>

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

### <span data-ttu-id="67d6e-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="67d6e-136">-PfxPassword</span></span>
<span data-ttu-id="67d6e-137">.Pfx 인증서 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d6e-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="67d6e-138">-PfxPath</span></span>
<span data-ttu-id="67d6e-139">.Pfx 인증서 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d6e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d6e-140">CommonParameters</span></span>
<span data-ttu-id="67d6e-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d6e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d6e-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="67d6e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d6e-143">입력</span><span class="sxs-lookup"><span data-stu-id="67d6e-143">INPUTS</span></span>

### <span data-ttu-id="67d6e-144">ApiManagement. PsApiManagementCertificateInformation/.</span><span class="sxs-lookup"><span data-stu-id="67d6e-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="67d6e-145">출력</span><span class="sxs-lookup"><span data-stu-id="67d6e-145">OUTPUTS</span></span>

### <span data-ttu-id="67d6e-146">ApiManagement. PsApiManagementCustomHostNameConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="67d6e-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="67d6e-147">상속자</span><span class="sxs-lookup"><span data-stu-id="67d6e-147">NOTES</span></span>

## <span data-ttu-id="67d6e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67d6e-148">RELATED LINKS</span></span>

[<span data-ttu-id="67d6e-149">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="67d6e-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="67d6e-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="67d6e-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)