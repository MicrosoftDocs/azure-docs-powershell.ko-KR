---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 5F856280-C561-47B5-AA96-27E34C86D604
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 1504d4f18c8ab3baee000c2cf8d873df1dd9a177
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044884"
---
# <span data-ttu-id="23e2d-101">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23e2d-101">Get-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="23e2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="23e2d-103">키 자격 증명 모음에 대 한 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-103">Gets a certificate issuer for a key vault.</span></span>

## <span data-ttu-id="23e2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23e2d-104">SYNTAX</span></span>

### <span data-ttu-id="23e2d-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="23e2d-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificateIssuer [-VaultName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23e2d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23e2d-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVault> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23e2d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23e2d-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateIssuer [-ResourceId] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23e2d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="23e2d-109">**AzKeyVaultCertificateIssuer** cmdlet은 지정 된 인증서 발급자 또는 Azure key vault의 키 자격 증명에 대 한 모든 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-109">The **Get-AzKeyVaultCertificateIssuer** cmdlet gets a specified certificate issuer or all certificate issuers for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="23e2d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="23e2d-110">EXAMPLES</span></span>

### <span data-ttu-id="23e2d-111">예제 1: 인증서 발급자 가져오기</span><span class="sxs-lookup"><span data-stu-id="23e2d-111">Example 1: Get a certificate issuer</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="23e2d-112">이 명령은 TestIssuer01 이라는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-112">This command gets the certificate issuer named TestIssuer01.</span></span>

### <span data-ttu-id="23e2d-113">예제 2: 필터링을 사용 하 여 인증서 발급자 나열</span><span class="sxs-lookup"><span data-stu-id="23e2d-113">Example 2: List certificate issuers using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "test*"

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer02
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="23e2d-114">이 명령은 "test"로 시작 하는 인증서 발급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-114">This command gets the certificate issuers that start with "test".</span></span>

## <span data-ttu-id="23e2d-115">변수</span><span class="sxs-lookup"><span data-stu-id="23e2d-115">PARAMETERS</span></span>

### <span data-ttu-id="23e2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e2d-116">-DefaultProfile</span></span>
<span data-ttu-id="23e2d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="23e2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23e2d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23e2d-118">-InputObject</span></span>
<span data-ttu-id="23e2d-119">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="23e2d-119">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23e2d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="23e2d-120">-Name</span></span>
<span data-ttu-id="23e2d-121">가져올 인증서 발급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-121">Specifies the name of the certificate issuer to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e2d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e2d-122">-ResourceId</span></span>
<span data-ttu-id="23e2d-123">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-123">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23e2d-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="23e2d-124">-VaultName</span></span>
<span data-ttu-id="23e2d-125">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e2d-126">CommonParameters</span></span>
<span data-ttu-id="23e2d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23e2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e2d-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23e2d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e2d-129">입력</span><span class="sxs-lookup"><span data-stu-id="23e2d-129">INPUTS</span></span>

### <span data-ttu-id="23e2d-130">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="23e2d-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="23e2d-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23e2d-131">System.String</span></span>

## <span data-ttu-id="23e2d-132">출력</span><span class="sxs-lookup"><span data-stu-id="23e2d-132">OUTPUTS</span></span>

### <span data-ttu-id="23e2d-133">Microsoft. KeyVault. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="23e2d-133">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

### <span data-ttu-id="23e2d-134">Microsoft. KeyVault. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23e2d-134">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="23e2d-135">상속자</span><span class="sxs-lookup"><span data-stu-id="23e2d-135">NOTES</span></span>

## <span data-ttu-id="23e2d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23e2d-136">RELATED LINKS</span></span>

[<span data-ttu-id="23e2d-137">제거-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23e2d-137">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="23e2d-138">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="23e2d-138">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)

