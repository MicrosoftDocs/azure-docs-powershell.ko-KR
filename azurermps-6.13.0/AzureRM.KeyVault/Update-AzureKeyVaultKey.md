---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
ms.openlocfilehash: e9e2401ab96da63c3fe6b5978916b96f98db9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530253"
---
# <span data-ttu-id="1d491-101">Update-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d491-101">Update-AzureKeyVaultKey</span></span>

## <span data-ttu-id="1d491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d491-102">SYNOPSIS</span></span>
<span data-ttu-id="1d491-103">키 자격 증명 모음에서 키의 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d491-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d491-104">SYNTAX</span></span>

### <span data-ttu-id="1d491-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1d491-105">Default (Default)</span></span>
```
Update-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d491-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1d491-106">InputObject</span></span>
```
Update-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d491-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1d491-107">DESCRIPTION</span></span>
<span data-ttu-id="1d491-108">**AzureKeyVaultKey** cmdlet은 키 자격 증명 모음에서 키의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-108">The **Update-AzureKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="1d491-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1d491-109">EXAMPLES</span></span>

### <span data-ttu-id="1d491-110">예제 1: 키를 수정 하 여 사용 하도록 설정 하 고 만료 날짜와 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="1d491-111">첫 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1d491-112">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="1d491-113">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="1d491-114">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="1d491-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1d491-115">두 번째 명령은 높은 심각도와 계정의 태그 값을 저장 하는 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="1d491-116">마지막 명령은 ITSoftware 라는 키를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="1d491-117">이 명령은 키를 설정 하 고 만료 시간을 $Expires에 저장 된 시간으로 설정 하 고 $Tags에 저장 된 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="1d491-118">예제 2: 모든 태그를 삭제 하는 키 수정</span><span class="sxs-lookup"><span data-stu-id="1d491-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1d491-119">이 명령은 ITSoftware 라는 특정 버전의 키에 대 한 태그를 모두 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="1d491-120">변수</span><span class="sxs-lookup"><span data-stu-id="1d491-120">PARAMETERS</span></span>

### <span data-ttu-id="1d491-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d491-121">-DefaultProfile</span></span>
<span data-ttu-id="1d491-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d491-123">-사용</span><span class="sxs-lookup"><span data-stu-id="1d491-123">-Enable</span></span>
<span data-ttu-id="1d491-124">True 값을 사용 하면 키와 false disabless 값이 키에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="1d491-125">지정 하지 않으면 기존의 enabled/disabled 상태가 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="1d491-126">-만료</span><span class="sxs-lookup"><span data-stu-id="1d491-126">-Expires</span></span>
<span data-ttu-id="1d491-127">UTC 시간 키의 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="1d491-128">지정 하지 않은 경우 키의 기존 만료 시간은 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="1d491-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d491-129">-InputObject</span></span>
<span data-ttu-id="1d491-130">Key 개체</span><span class="sxs-lookup"><span data-stu-id="1d491-130">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d491-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="1d491-131">-KeyOps</span></span>
<span data-ttu-id="1d491-132">키를 사용 하 여 수행할 수 있는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="1d491-133">지정 하지 않으면 키의 기존 키 작업이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="1d491-134">-이름</span><span class="sxs-lookup"><span data-stu-id="1d491-134">-Name</span></span>
<span data-ttu-id="1d491-135">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-135">Key name.</span></span>
<span data-ttu-id="1d491-136">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d491-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1d491-137">-NotBefore</span></span>
<span data-ttu-id="1d491-138">키를 사용할 수 없는 UTC 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="1d491-139">지정 하지 않으면 키의 기존 NotBefore 특성이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="1d491-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d491-140">-PassThru</span></span>
<span data-ttu-id="1d491-141">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1d491-142">이 스위치가 지정 된 경우 업데이트 된 키 번들 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="1d491-143">태그</span><span class="sxs-lookup"><span data-stu-id="1d491-143">-Tag</span></span>
<span data-ttu-id="1d491-144">Hashtable는 키 태그를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="1d491-145">지정 하지 않으면 키의 existings 태그가 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="1d491-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1d491-146">-VaultName</span></span>
<span data-ttu-id="1d491-147">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="1d491-147">Vault name.</span></span>
<span data-ttu-id="1d491-148">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d491-149">-버전</span><span class="sxs-lookup"><span data-stu-id="1d491-149">-Version</span></span>
<span data-ttu-id="1d491-150">키 버전.</span><span class="sxs-lookup"><span data-stu-id="1d491-150">Key version.</span></span>
<span data-ttu-id="1d491-151">Cmdlet은 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전의 키에 대 한 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d491-152">-확인</span><span class="sxs-lookup"><span data-stu-id="1d491-152">-Confirm</span></span>
<span data-ttu-id="1d491-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d491-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d491-154">-WhatIf</span></span>
<span data-ttu-id="1d491-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d491-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d491-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d491-157">CommonParameters</span></span>
<span data-ttu-id="1d491-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d491-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d491-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d491-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d491-160">입력</span><span class="sxs-lookup"><span data-stu-id="1d491-160">INPUTS</span></span>

### <span data-ttu-id="1d491-161">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1d491-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="1d491-162">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d491-162">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1d491-163">출력</span><span class="sxs-lookup"><span data-stu-id="1d491-163">OUTPUTS</span></span>

### <span data-ttu-id="1d491-164">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1d491-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1d491-165">상속자</span><span class="sxs-lookup"><span data-stu-id="1d491-165">NOTES</span></span>

## <span data-ttu-id="1d491-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d491-166">RELATED LINKS</span></span>