---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 515a238aa7e6bb49117dd38954dbb67f840abd9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218661"
---
# <span data-ttu-id="4d59c-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d59c-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="4d59c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d59c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d59c-103">키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="4d59c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d59c-104">SYNTAX</span></span>

### <span data-ttu-id="4d59c-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d59c-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="4d59c-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="4d59c-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="4d59c-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="4d59c-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="4d59c-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="4d59c-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="4d59c-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d59c-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="4d59c-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d59c-114">설명은</span><span class="sxs-lookup"><span data-stu-id="4d59c-114">DESCRIPTION</span></span>
<span data-ttu-id="4d59c-115">**AzKeyVaultKey** Cmdlet은 Azure 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="4d59c-116">이 cmdlet은 특정 **Microsoft Azure.** e. e. e. e. e. e. e. e a **KeyBundle** e.</span><span class="sxs-lookup"><span data-stu-id="4d59c-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="4d59c-117">예제의</span><span class="sxs-lookup"><span data-stu-id="4d59c-117">EXAMPLES</span></span>

### <span data-ttu-id="4d59c-118">예제 1: 키 보관소에 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d59c-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="4d59c-119">이 명령은 Contoso 라는 키 보관소의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="4d59c-120">예제 2: 현재 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d59c-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="4d59c-121">이 명령은 Contoso 라는 키 보관소에 있는 test1 이라는 키의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="4d59c-122">예제 3: 모든 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d59c-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="4d59c-123">이 명령은 Contoso 라는 키 보관소에 ITPfx 라는 모든 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-123">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="4d59c-124">예제 4: 특정 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d59c-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="4d59c-125">이 명령은 Contoso 라는 키 보관소에 있는 test1 이라는 특정 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="4d59c-126">이 명령을 실행 한 후에는 $Key 개체를 탐색 하 여 키의 다양 한 속성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="4d59c-127">예제 5: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d59c-127">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="4d59c-128">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="4d59c-129">예제 6: 삭제 되었지만이 키 보관소에는 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="4d59c-130">이 명령은 Contoso 라는 키 자격 증명 모음에서 이전에 삭제 되었지만 제거 되지 않은 키 test3를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="4d59c-131">이 명령은 삭제 날짜 등의 메타 데이터와이 지운 편지함의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="4d59c-132">예제 7: 필터링을 사용 하 여 키 보관소에 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="4d59c-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="4d59c-133">이 명령은 "test"로 시작 하는 Contoso 라는 키 보관소의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="4d59c-134">예제 8: 공개 키를 pem 파일로 다운로드</span><span class="sxs-lookup"><span data-stu-id="4d59c-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="4d59c-135">매개 변수를 지정 하 여 RSA 키의 공개 키를 다운로드할 수 있습니다 `-OutFile` .</span><span class="sxs-lookup"><span data-stu-id="4d59c-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="4d59c-136">이 단계는 HSM에서 보호 하는 키를 Azure 키 자격 증명 모음으로 가져오는 한 가지 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="4d59c-137">보기 https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="4d59c-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="4d59c-138">변수</span><span class="sxs-lookup"><span data-stu-id="4d59c-138">PARAMETERS</span></span>

### <span data-ttu-id="4d59c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d59c-139">-DefaultProfile</span></span>
<span data-ttu-id="4d59c-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4d59c-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d59c-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="4d59c-141">-IncludeVersions</span></span>
<span data-ttu-id="4d59c-142">이 cmdlet가 모든 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="4d59c-143">키의 현재 버전은 목록의 첫 번째 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="4d59c-144">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="4d59c-145">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d59c-146">-InputObject</span></span>
<span data-ttu-id="4d59c-147">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="4d59c-147">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4d59c-148">-InRemovedState</span></span>
<span data-ttu-id="4d59c-149">출력에 이전에 삭제 된 키를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-149">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-150">-이름</span><span class="sxs-lookup"><span data-stu-id="4d59c-150">-Name</span></span>
<span data-ttu-id="4d59c-151">가져올 키 번들의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-152">출력</span><span class="sxs-lookup"><span data-stu-id="4d59c-152">-OutFile</span></span>
<span data-ttu-id="4d59c-153">이 cmdlet이 키를 저장할 출력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="4d59c-154">공개 키는 기본적으로 PEM 형식으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="4d59c-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d59c-155">-ResourceId</span></span>
<span data-ttu-id="4d59c-156">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-156">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4d59c-157">-VaultName</span></span>
<span data-ttu-id="4d59c-158">이 cmdlet에서 키를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="4d59c-159">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 선택한 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-160">-버전</span><span class="sxs-lookup"><span data-stu-id="4d59c-160">-Version</span></span>
<span data-ttu-id="4d59c-161">키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-161">Specifies the key version.</span></span>
<span data-ttu-id="4d59c-162">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d59c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d59c-163">CommonParameters</span></span>
<span data-ttu-id="4d59c-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d59c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d59c-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d59c-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d59c-166">입력</span><span class="sxs-lookup"><span data-stu-id="4d59c-166">INPUTS</span></span>

### <span data-ttu-id="4d59c-167">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4d59c-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4d59c-168">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4d59c-168">System.String</span></span>

## <span data-ttu-id="4d59c-169">출력</span><span class="sxs-lookup"><span data-stu-id="4d59c-169">OUTPUTS</span></span>

### <span data-ttu-id="4d59c-170">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4d59c-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="4d59c-171">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d59c-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="4d59c-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4d59c-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="4d59c-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d59c-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="4d59c-174">상속자</span><span class="sxs-lookup"><span data-stu-id="4d59c-174">NOTES</span></span>

## <span data-ttu-id="4d59c-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d59c-175">RELATED LINKS</span></span>

[<span data-ttu-id="4d59c-176">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d59c-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="4d59c-177">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4d59c-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="4d59c-178">실행 취소-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="4d59c-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="4d59c-179">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="4d59c-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
