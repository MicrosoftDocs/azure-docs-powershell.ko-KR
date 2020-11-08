---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204716"
---
# <span data-ttu-id="c42d7-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c42d7-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="c42d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c42d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c42d7-103">저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="c42d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c42d7-104">SYNTAX</span></span>

### <span data-ttu-id="c42d7-105">StorageEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="c42d7-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c42d7-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c42d7-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c42d7-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="c42d7-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c42d7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c42d7-108">DESCRIPTION</span></span>
<span data-ttu-id="c42d7-109">**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="c42d7-110">이 cmdlet을 사용 하 여 계정 유형을 수정 하거나, 고객 도메인을 업데이트 하거나, 저장소 계정에서 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="c42d7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c42d7-111">EXAMPLES</span></span>

### <span data-ttu-id="c42d7-112">예제 1: 저장소 계정 유형 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="c42d7-113">이 명령은 저장소 계정 유형을 Standard_RAGRS 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="c42d7-114">예제 2: 저장소 계정의 사용자 지정 도메인 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="c42d7-115">이 명령은 저장소 계정에 대 한 사용자 지정 도메인을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="c42d7-116">예제 3: 액세스 계층 값 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="c42d7-117">명령에서 액세스 계층 값이 멋진 것으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="c42d7-118">예제 4: 사용자 지정 도메인 및 태그 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="c42d7-119">이 명령은 저장소 계정의 사용자 지정 도메인 및 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="c42d7-120">예제 5: 암호화 KeySource를 Keysource로 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="c42d7-121">이 명령은 새로 만든 Keysource를 사용 하 여 암호화 KeySource를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="c42d7-122">예제 6: 암호화 KeySource를 "Microsoft. 저장소"로 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="c42d7-123">이 명령은 암호화 KeySource를 "Microsoft. 저장소"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="c42d7-124">예제 7: JSON을 사용 하 여 저장소 계정의 NetworkRuleSet 규칙 집합 속성 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="c42d7-125">이 명령은 JSON으로 저장소 계정의 네트워크 규칙 집합 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="c42d7-126">예제 8: 저장소 계정에서 NetworkRuleSet 속성 가져오기 및 다른 저장소 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="c42d7-127">첫 번째 명령은 저장소 계정에서 NetworkRuleSet 집합 속성을 가져오며, 두 번째 명령은 다른 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="c42d7-128">예제 9: 유형 "저장소" 또는 "BlobStorage"를 "StorageV2" kind 저장소 계정으로 사용 하 여 저장소 계정 업그레이드</span><span class="sxs-lookup"><span data-stu-id="c42d7-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="c42d7-129">"저장소" 또는 "BlobStorage" 종류가 "StorageV2" kind 저장소 계정으로 저장 된 저장소 계정을 명령으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="c42d7-130">예제 10: Azure Files AAD DS 인증을 사용 하도록 설정 하 여 저장소 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="c42d7-131">명령에서 Azure Files AAD DS 인증을 사용 하 여 저장소 계정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="c42d7-132">예제 11: 파일 Active Directory 도메인 서비스 인증을 사용 하도록 설정 하 여 저장소 계정을 업데이트 한 다음 파일 Id 기반 인증 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="c42d7-133">명령이 Azure Files Active Directory 도메인 서비스 인증을 사용 하도록 설정 하 여 저장소 계정을 업데이트 한 다음 파일 Id 기반 인증 설정을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="c42d7-134">예제 12: 이상 버전 및 AllowBlobPublicAccess 설정</span><span class="sxs-lookup"><span data-stu-id="c42d7-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="c42d7-135">이 명령은 고가을 설정 합니다. \ 및 AllowBlobPublicAccess를 설정한 다음 계정의 2 가지 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="c42d7-136">변수</span><span class="sxs-lookup"><span data-stu-id="c42d7-136">PARAMETERS</span></span>

### <span data-ttu-id="c42d7-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c42d7-137">-AccessTier</span></span>
<span data-ttu-id="c42d7-138">이 cmdlet이 수정 하는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="c42d7-139">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="c42d7-140">액세스 계층을 변경 하면 추가 요금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="c42d7-141">자세한 내용은 [Azure Blob Storage: 핫 및 유용한 저장소 계층](http://go.microsoft.com/fwlink/?LinkId=786482)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c42d7-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="c42d7-142">저장소 계정의 종류가 StorageV2 또는 BlobStorage 인 경우 *AccessTier* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="c42d7-143">저장소 계정에 저장소 유형이 있는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="c42d7-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="c42d7-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="c42d7-145">Azure Storage에 대 한 SID (보안 식별자)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="c42d7-146">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="c42d7-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="c42d7-148">도메인 GUID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-148">Specifies the domain GUID.</span></span> <span data-ttu-id="c42d7-149">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="c42d7-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="c42d7-151">광고 DNS 서버에 대해 권한이 있는 기본 도메인을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="c42d7-152">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="c42d7-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="c42d7-154">SID (보안 식별자)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="c42d7-155">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="c42d7-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="c42d7-157">가져올 Active Directory 포리스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="c42d7-158">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="c42d7-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="c42d7-160">NetBIOS 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="c42d7-161">-EnableActiveDirectoryDomainServicesForFile가 true로 설정 된 경우이 매개 변수를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="c42d7-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="c42d7-163">저장소 계정의 모든 blob 또는 컨테이너에 대 한 공용 액세스를 허용 하거나 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c42d7-164">-AsJob</span></span>
<span data-ttu-id="c42d7-165">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c42d7-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c42d7-166">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="c42d7-166">-AssignIdentity</span></span>
<span data-ttu-id="c42d7-167">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c42d7-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c42d7-168">-CustomDomainName</span></span>
<span data-ttu-id="c42d7-169">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="c42d7-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42d7-170">-DefaultProfile</span></span>
<span data-ttu-id="c42d7-171">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42d7-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="c42d7-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="c42d7-173">Azure Files 저장소 계정에 대 한 Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="c42d7-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="c42d7-175">Azure Files 저장소 계정에 대 한 Active Directory 도메인 서비스 인증을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c42d7-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="c42d7-177">저장소 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="c42d7-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="c42d7-179">저장소 계정이 5 개 이상의 TiB 용량으로 큰 파일 공유를 지원할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="c42d7-180">계정을 사용 하도록 설정한 후에는 해당 기능을 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="c42d7-181">현재 LRS 및 ZRS 복제 유형에만 지원 되므로 지역 중복 계정으로 계정 변환을 수행할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="c42d7-182">자세한 정보 https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="c42d7-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="c42d7-183">-Force</span><span class="sxs-lookup"><span data-stu-id="c42d7-183">-Force</span></span>
<span data-ttu-id="c42d7-184">변경 내용이 저장소 계정에 기록 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="c42d7-185">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c42d7-185">-KeyName</span></span>
<span data-ttu-id="c42d7-186">-KeyvaultEncryption를 사용 하 여 키 자격 증명 모음으로 암호화를 사용 하는 경우이 옵션을 사용 하 여 Keyname 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c42d7-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="c42d7-188">저장소 서비스 암호화를 사용 하는 경우 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="c42d7-189">KeyName, KeyVersion, KeyVaultUri이 모두 설정 된 경우 Keyversion는이 매개 변수 설정 여부에 관계 없이 Microsoft. Keyversion에 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c42d7-190">-KeyVaultUri</span></span>
<span data-ttu-id="c42d7-191">-KeyvaultEncryption 매개 변수를 지정 하 여 키 보관소 암호화를 사용 하는 경우이 옵션을 사용 하 여 키 보관소에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-192">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c42d7-192">-KeyVersion</span></span>
<span data-ttu-id="c42d7-193">-KeyvaultEncryption 매개 변수를 지정 하 여 키 보관소 암호화를 사용 하는 경우이 옵션을 사용 하 여 키 버전에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-194">-없음 Tls 버전</span><span class="sxs-lookup"><span data-stu-id="c42d7-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="c42d7-195">저장소 요청에 허용 되는 최소 TLS 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-195">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-196">-이름</span><span class="sxs-lookup"><span data-stu-id="c42d7-196">-Name</span></span>
<span data-ttu-id="c42d7-197">수정할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-197">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-198">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="c42d7-198">-NetworkRuleSet</span></span>
<span data-ttu-id="c42d7-199">NetworkRuleSet는 방화벽과 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 규칙을 우회 하도록 허용 된 서비스 같은 네트워크 속성에 대 한 값을 설정 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42d7-200">-ResourceGroupName</span></span>
<span data-ttu-id="c42d7-201">저장소 계정을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-202">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="c42d7-202">-SkuName</span></span>
<span data-ttu-id="c42d7-203">저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="c42d7-204">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c42d7-205">Standard_LRS 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="c42d7-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="c42d7-206">Standard_ZRS 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="c42d7-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="c42d7-207">Standard_GRS 지역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="c42d7-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="c42d7-208">Standard_RAGRS-액세스 지리적 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="c42d7-209">Premium_LRS-Premium 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="c42d7-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="c42d7-210">Standard_GZRS 지역 중복 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="c42d7-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="c42d7-211">Standard_RAGZRS-액세스 지리적 중복 영역 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="c42d7-212">Standard_ZRS 및 Premium_LRS 형식을 다른 계정 형식으로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="c42d7-213">다른 계정 유형은 Standard_ZRS 하거나 Premium_LRS 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="c42d7-214">-StorageEncryption</span></span>
<span data-ttu-id="c42d7-215">Microsoft 관리 키를 사용 하도록 저장소 계정 암호화를 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-216">태그</span><span class="sxs-lookup"><span data-stu-id="c42d7-216">-Tag</span></span>
<span data-ttu-id="c42d7-217">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c42d7-218">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c42d7-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="c42d7-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="c42d7-220">저장소 또는 BlobStorage에서 저장소 계정 종류를 StorageV2로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="c42d7-221">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="c42d7-221">-UseSubDomain</span></span>
<span data-ttu-id="c42d7-222">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-222">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-223">-확인</span><span class="sxs-lookup"><span data-stu-id="c42d7-223">-Confirm</span></span>
<span data-ttu-id="c42d7-224">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42d7-225">-WhatIf</span></span>
<span data-ttu-id="c42d7-226">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c42d7-227">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d7-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42d7-228">CommonParameters</span></span>
<span data-ttu-id="c42d7-229">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c42d7-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42d7-230">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c42d7-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42d7-231">입력</span><span class="sxs-lookup"><span data-stu-id="c42d7-231">INPUTS</span></span>

### <span data-ttu-id="c42d7-232">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c42d7-232">System.String</span></span>

### <span data-ttu-id="c42d7-233">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="c42d7-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c42d7-234">출력</span><span class="sxs-lookup"><span data-stu-id="c42d7-234">OUTPUTS</span></span>

### <span data-ttu-id="c42d7-235">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c42d7-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c42d7-236">상속자</span><span class="sxs-lookup"><span data-stu-id="c42d7-236">NOTES</span></span>

## <span data-ttu-id="c42d7-237">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c42d7-237">RELATED LINKS</span></span>

[<span data-ttu-id="c42d7-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c42d7-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="c42d7-239">새로운 AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c42d7-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="c42d7-240">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c42d7-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)