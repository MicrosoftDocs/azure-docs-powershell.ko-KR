---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056318"
---
# <span data-ttu-id="0e8d0-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="0e8d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8d0-103">키 자격 증명 모음에 키를 만들거나 키를 키 보관소로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="0e8d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e8d0-104">SYNTAX</span></span>

### <span data-ttu-id="0e8d0-105">InteractiveCreate (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e8d0-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8d0-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="0e8d0-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8d0-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="0e8d0-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8d0-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="0e8d0-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8d0-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="0e8d0-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e8d0-110">Resourcei//포트</span><span class="sxs-lookup"><span data-stu-id="0e8d0-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8d0-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0e8d0-111">DESCRIPTION</span></span>
<span data-ttu-id="0e8d0-112">**AzKeyVaultKey** Cmdlet은 Azure key vault의 키 보관소에 키를 만들거나 키를 키 모음으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="0e8d0-113">이 cmdlet을 사용 하 여 다음 방법 중 하나를 사용 하 여 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="0e8d0-114">키 보관소 서비스의 HSM (하드웨어 보안 모듈)에서 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="0e8d0-115">키 보관소 서비스의 소프트웨어에서 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="0e8d0-116">키 보관소 서비스의 HSM (하드웨어 보안 모듈)에서 Hsm으로 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="0e8d0-117">컴퓨터의 .pfx 파일에서 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="0e8d0-118">컴퓨터에 있는 .pfx 파일의 키를 키 보관소 서비스의 Hsm (하드웨어 보안 모듈)로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="0e8d0-119">이러한 작업의 경우 키 특성을 제공 하거나 기본 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="0e8d0-120">키 자격 증명 모음의 기존 키와 같은 이름을 가진 키를 만들거나 가져오면 새 키에 대해 지정 하는 값으로 원래 키가 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="0e8d0-121">해당 버전의 키에 대 한 버전 관련 URI를 사용 하 여 이전 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="0e8d0-122">주요 버전 및 URI 구조에 대 한 자세한 내용은 키 볼트 REST API 설명서의 [키 및 비밀 정보](http://go.microsoft.com/fwlink/?linkid=518560) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="0e8d0-123">참고: 고유한 하드웨어 보안 모듈에서 키를 가져오려면 먼저 Azure Key Vault BYOK 도구 집합을 사용 하 여 BYOK 패키지 (이름 확장명을 가진 파일)를 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="0e8d0-124">자세한 내용은 [Azure 키 보관소에 대 한 HSM-Protected 키를 생성 하 고 전송 하는 방법을](http://go.microsoft.com/fwlink/?LinkId=522252)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="0e8d0-125">가장 좋은 방법은 키를 만들거나 업데이트 한 후 Backup-AzKeyVaultKey cmdlet을 사용 하 여 백업 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="0e8d0-126">삭제 취소 기능이 없기 때문에 실수로 키를 삭제 하거나 삭제 한 다음 생각이 바뀌면 다시 복원할 수 있는 백업을가지고 있지 않는 한 키를 복구 가능 하지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="0e8d0-127">예제의</span><span class="sxs-lookup"><span data-stu-id="0e8d0-127">EXAMPLES</span></span>

### <span data-ttu-id="0e8d0-128">예제 1: 키 만들기</span><span class="sxs-lookup"><span data-stu-id="0e8d0-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0e8d0-129">이 명령은 Contoso 라는 키 보관소에 ITSoftware 라는 소프트웨어 보호 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e8d0-130">예제 2: HSM으로 보호 된 키 만들기</span><span class="sxs-lookup"><span data-stu-id="0e8d0-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0e8d0-131">이 명령은 Contoso 라는 키 보관소에 HSM으로 보호 된 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="0e8d0-132">예제 3: 기본값이 아닌 값을 사용 하 여 키 만들기</span><span class="sxs-lookup"><span data-stu-id="0e8d0-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="0e8d0-133">첫 번째 명령은 $KeyOperations 변수의 암호를 해독 하 고 확인 하는 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="0e8d0-134">두 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 UTC로 정의 된 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0e8d0-135">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="0e8d0-136">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="0e8d0-137">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="0e8d0-138">세 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0e8d0-139">해당 개체는 현재 UTC 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-139">That object specifies current UTC time.</span></span> <span data-ttu-id="0e8d0-140">이 명령은 $NotBefore 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="0e8d0-141">마지막 명령은 HSM으로 보호 된 키 인 ITHsmNonDefault 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="0e8d0-142">명령은 $KeyOperations 저장 된 허용 키 작업에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="0e8d0-143">이 명령은 이전 명령에서 만든 *만료* 및 *NotBefore* 매개 변수에 대 한 시간을 지정 하 고 높은 심각도 및이에 대 한 태그를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="0e8d0-144">새 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-144">The new key is disabled.</span></span> <span data-ttu-id="0e8d0-145">**AzKeyVaultKey** cmdlet을 사용 하 여이 기능을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="0e8d0-146">예제 4: HSM으로 보호 된 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e8d0-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0e8d0-147">이 명령은 *Keyfilepath* 매개 변수에서 지정 하는 위치에서 ITByok 라는 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="0e8d0-148">가져온 키는 HSM으로 보호 된 키입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="0e8d0-149">고유한 하드웨어 보안 모듈에서 키를 가져오려면 먼저 Azure Key Vault BYOK 도구 집합을 사용 하 여 BYOK 패키지 (파일 이름 확장명이. a 1)를 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="0e8d0-150">자세한 내용은 [Azure 키 보관소에 대 한 HSM-Protected 키를 생성 하 고 전송 하는 방법을](http://go.microsoft.com/fwlink/?LinkId=522252)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="0e8d0-151">예제 5: 소프트웨어 보호 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="0e8d0-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="0e8d0-152">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="0e8d0-153">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="0e8d0-154">두 번째 명령은 Contoso 키 보관소에 소프트웨어 비밀 번호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="0e8d0-155">명령은 $Password에 저장 된 키와 암호의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="0e8d0-156">예제 6: 키 가져오기 및 특성 할당</span><span class="sxs-lookup"><span data-stu-id="0e8d0-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="0e8d0-157">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="0e8d0-158">두 번째 명령은 **가져오기-날짜** cmdlet을 사용 하 여 **DateTime** 개체를 만든 다음 해당 개체를 $Expires 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="0e8d0-159">세 번째 명령은 $tags 변수를 만들어 높은 심각도 및 그에 대 한 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="0e8d0-160">마지막 명령은 지정 된 위치에서 HSM 키로 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="0e8d0-161">명령은 $Password에 저장 된 $Expires 및 암호에 저장 된 만료 시간을 지정 하 고 $tags에 저장 된 태그를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="0e8d0-162">예제 7: "자체 키 가져오기" (KEK) 기능에 대 한 키 교환 키 ()를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="0e8d0-163">키를 생성 합니다 (키 교환 키 (KEK)).</span><span class="sxs-lookup"><span data-stu-id="0e8d0-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="0e8d0-164">KEK는 키 가져오기 작업만 있는 RSA-HSM 키 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="0e8d0-165">키 보관소 Premium SKU만 RSA-HSM 키를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="0e8d0-166">자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="0e8d0-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="0e8d0-167">변수</span><span class="sxs-lookup"><span data-stu-id="0e8d0-167">PARAMETERS</span></span>

### <span data-ttu-id="0e8d0-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8d0-168">-DefaultProfile</span></span>
<span data-ttu-id="0e8d0-169">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e8d0-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8d0-170">-대상</span><span class="sxs-lookup"><span data-stu-id="0e8d0-170">-Destination</span></span>
<span data-ttu-id="0e8d0-171">키 자격 증명 모음 서비스에서 키를 소프트웨어 보호 키 또는 HSM로 보호 된 키로 추가할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="0e8d0-172">유효한 값은 HSM 및 소프트웨어입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="0e8d0-173">참고: 대상으로 HSM을 사용 하려면 Hsm을 지 원하는 키 자격 증명 모음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="0e8d0-174">Azure 키 자격 증명 모음의 서비스 계층 및 기능에 대 한 자세한 내용은 [Azure 키 보관소 가격 웹 사이트](http://go.microsoft.com/fwlink/?linkid=512521)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="0e8d0-175">이 매개 변수는 새 키를 만들 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="0e8d0-176">*Keyfilepath* 매개 변수를 사용 하 여 키를 가져오는 경우이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="0e8d0-177">이 매개 변수를 지정 하지 않고이 cmdlet은 file 이름 확장명이 byok 인 키를 가져오면 해당 키를 HSM 보호 키로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="0e8d0-178">Cmdlet에서 해당 키를 소프트웨어 보호 키로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="0e8d0-179">이 매개 변수를 지정 하지 않고이 cmdlet이 .pfx 파일 이름 확장명을 가진 키를 가져오면 해당 키를 소프트웨어 보호 키로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-180">-Disable</span><span class="sxs-lookup"><span data-stu-id="0e8d0-180">-Disable</span></span>
<span data-ttu-id="0e8d0-181">추가 하는 키가 비활성의 초기 상태로 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="0e8d0-182">키를 사용 하려는 시도는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="0e8d0-183">나중에 사용 하려는 키를 미리 로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="0e8d0-184">-만료</span><span class="sxs-lookup"><span data-stu-id="0e8d0-184">-Expires</span></span>
<span data-ttu-id="0e8d0-185">이 cmdlet이 추가 하는 키에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="0e8d0-186">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0e8d0-187">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0e8d0-188">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="0e8d0-189">이 매개 변수를 지정 하지 않으면 키가 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-189">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e8d0-190">-InputObject</span></span>
<span data-ttu-id="0e8d0-191">자격 증명 모음 개체.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-191">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="0e8d0-192">-KeyFilePassword</span></span>
<span data-ttu-id="0e8d0-193">가져온 파일의 암호를 **SecureString** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="0e8d0-194">**Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="0e8d0-195">자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="0e8d0-196">파일 이름 확장명이 .pfx 인 파일을 가져오려면이 암호를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-197">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="0e8d0-197">-KeyFilePath</span></span>
<span data-ttu-id="0e8d0-198">이 cmdlet이 가져오는 키 자료가 포함 된 로컬 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="0e8d0-199">올바른 파일 이름 확장명은 byok 및 .pfx입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="0e8d0-200">파일을 byok 파일 인 경우 가져오기 후 키가 Hsm에 의해 자동으로 보호 되며이 기본값을 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="0e8d0-201">파일이 .pfx 파일이 면 가져오기 후 소프트웨어에 의해 키가 자동으로 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="0e8d0-202">이 기본값을 재정의 하려면 키가 HSM으로 보호 되도록 *대상* 매개 변수를 hsm으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="0e8d0-203">이 매개 변수를 지정 하는 경우 *대상* 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="0e8d0-204">-KeyOps</span></span>
<span data-ttu-id="0e8d0-205">이 cmdlet이 추가 하는 키를 사용 하 여 수행할 수 있는 작업 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="0e8d0-206">이 매개 변수를 지정 하지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="0e8d0-207">이 매개 변수에 허용 되는 값은 [JSON Web key (JWK) 사양](http://go.microsoft.com/fwlink/?LinkID=613300)에 정의 된 대로 쉼표로 구분 된 키 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="0e8d0-208">해독할</span><span class="sxs-lookup"><span data-stu-id="0e8d0-208">encrypt</span></span>
- <span data-ttu-id="0e8d0-209">해독은</span><span class="sxs-lookup"><span data-stu-id="0e8d0-209">decrypt</span></span>
- <span data-ttu-id="0e8d0-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-210">wrapKey</span></span>
- <span data-ttu-id="0e8d0-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-211">unwrapKey</span></span>
- <span data-ttu-id="0e8d0-212">등록할</span><span class="sxs-lookup"><span data-stu-id="0e8d0-212">sign</span></span>
- <span data-ttu-id="0e8d0-213">나타나는지</span><span class="sxs-lookup"><span data-stu-id="0e8d0-213">verify</span></span>
- <span data-ttu-id="0e8d0-214">가져오기 (KEK만 해당) (예제 7 참조)</span><span class="sxs-lookup"><span data-stu-id="0e8d0-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="0e8d0-215">-이름</span><span class="sxs-lookup"><span data-stu-id="0e8d0-215">-Name</span></span>
<span data-ttu-id="0e8d0-216">키 자격 증명 모음에 추가할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="0e8d0-217">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="0e8d0-218">Name은 0-9, a-z, a-z 및-(대시 기호)만 포함 하는 1 ~ 63 문자 문자열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0e8d0-219">-NotBefore</span></span>
<span data-ttu-id="0e8d0-220">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="0e8d0-221">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-221">This parameter uses UTC.</span></span> <span data-ttu-id="0e8d0-222">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0e8d0-223">이 매개 변수를 지정 하지 않으면 키를 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-223">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e8d0-224">-ResourceId</span></span>
<span data-ttu-id="0e8d0-225">자격 증명 모음 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-225">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-226">-크기</span><span class="sxs-lookup"><span data-stu-id="0e8d0-226">-Size</span></span>
<span data-ttu-id="0e8d0-227">RSA 키 크기 (비트 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-227">RSA key size, in bits.</span></span> <span data-ttu-id="0e8d0-228">지정 하지 않으면 서비스에서 안전한 기본값을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-228">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-229">태그</span><span class="sxs-lookup"><span data-stu-id="0e8d0-229">-Tag</span></span>
<span data-ttu-id="0e8d0-230">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e8d0-231">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0e8d0-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0e8d0-232">-VaultName</span></span>
<span data-ttu-id="0e8d0-233">이 cmdlet이 키를 추가 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="0e8d0-234">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-235">-확인</span><span class="sxs-lookup"><span data-stu-id="0e8d0-235">-Confirm</span></span>
<span data-ttu-id="0e8d0-236">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-236">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8d0-237">-WhatIf</span></span>
<span data-ttu-id="0e8d0-238">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8d0-239">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-239">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8d0-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8d0-240">CommonParameters</span></span>
<span data-ttu-id="0e8d0-241">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8d0-242">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8d0-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8d0-243">입력</span><span class="sxs-lookup"><span data-stu-id="0e8d0-243">INPUTS</span></span>

### <span data-ttu-id="0e8d0-244">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0e8d0-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0e8d0-245">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e8d0-245">System.String</span></span>

## <span data-ttu-id="0e8d0-246">출력</span><span class="sxs-lookup"><span data-stu-id="0e8d0-246">OUTPUTS</span></span>

### <span data-ttu-id="0e8d0-247">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="0e8d0-248">상속자</span><span class="sxs-lookup"><span data-stu-id="0e8d0-248">NOTES</span></span>

## <span data-ttu-id="0e8d0-249">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e8d0-249">RELATED LINKS</span></span>

[<span data-ttu-id="0e8d0-250">백업-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="0e8d0-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="0e8d0-252">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e8d0-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="0e8d0-253">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="0e8d0-253">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)