---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 183618058d6400798dc2af74975fd45a0a397b16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867830"
---
# <span data-ttu-id="2c980-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c980-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2c980-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c980-102">SYNOPSIS</span></span>
<span data-ttu-id="2c980-103">키 자격 증명 모음 관리 Azure 저장소 계정의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2c980-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c980-104">SYNTAX</span></span>

### <span data-ttu-id="2c980-105">ByDefinitionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c980-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c980-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c980-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c980-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2c980-107">DESCRIPTION</span></span>
<span data-ttu-id="2c980-108">키 보관소 관리 Azure Storage 계정의 편집 가능한 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2c980-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2c980-109">EXAMPLES</span></span>

### <span data-ttu-id="2c980-110">예제 1: 키 보관소 관리 Azure 저장소 계정에서 활성 키를 ' key2 '로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="2c980-111">키 자격 증명 모음에서 Azure Storage 계정 활성 키를 ' a m m '으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="2c980-112">이 업데이트 후에 ' key2 '가 SAS 토큰을 생성 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="2c980-113">변수</span><span class="sxs-lookup"><span data-stu-id="2c980-113">PARAMETERS</span></span>

### <span data-ttu-id="2c980-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c980-114">-AccountName</span></span>
<span data-ttu-id="2c980-115">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="2c980-116">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c980-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="2c980-117">-ActiveKeyName</span></span>
<span data-ttu-id="2c980-118">활성 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-118">Active key name.</span></span>
<span data-ttu-id="2c980-119">지정 하지 않으면 관리 저장소 계정의 활성 키 이름에 대 한 기존 값이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="2c980-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2c980-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="2c980-121">자동으로 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-121">Auto regenerate key.</span></span>
<span data-ttu-id="2c980-122">지정 하지 않으면 관리 되는 저장소 계정의 기존 자동 재생성 키 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="2c980-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c980-123">-DefaultProfile</span></span>
<span data-ttu-id="2c980-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2c980-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c980-125">-사용</span><span class="sxs-lookup"><span data-stu-id="2c980-125">-Enable</span></span>
<span data-ttu-id="2c980-126">있으면 value가 true 인 경우 sas 토큰 생성에 대해 관리 되는 저장소 계정 키를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="2c980-127">값이 false 인 경우 sas 토큰 생성에 대해 관리 되는 저장소 계정 키를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="2c980-128">지정 하지 않으면 저장소 계정의 사용/사용 안 함 상태에 대 한 기존 값이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="2c980-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c980-129">-InputObject</span></span>
<span data-ttu-id="2c980-130">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-130">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c980-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c980-131">-PassThru</span></span>
<span data-ttu-id="2c980-132">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="2c980-133">이 스위치가 지정 된 경우 관리 되는 저장소 계정 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="2c980-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="2c980-134">-RegenerationPeriod</span></span>
<span data-ttu-id="2c980-135">재생성 기간.</span><span class="sxs-lookup"><span data-stu-id="2c980-135">Regeneration period.</span></span> <span data-ttu-id="2c980-136">자동 다시 생성 키를 사용 하는 경우이 값은 관리 저장소 계정의 비활성 keygets 재생성 되 고 활성 키가 되는 timespan을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="2c980-137">지정 하지 않은 경우 관리 되는 저장소 계정의 기존 다시 생성 기간 값은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c980-138">태그</span><span class="sxs-lookup"><span data-stu-id="2c980-138">-Tag</span></span>
<span data-ttu-id="2c980-139">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2c980-140">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2c980-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2c980-141">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2c980-141">-VaultName</span></span>
<span data-ttu-id="2c980-142">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="2c980-142">Vault name.</span></span>
<span data-ttu-id="2c980-143">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c980-144">-확인</span><span class="sxs-lookup"><span data-stu-id="2c980-144">-Confirm</span></span>
<span data-ttu-id="2c980-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c980-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c980-146">-WhatIf</span></span>
<span data-ttu-id="2c980-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c980-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c980-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c980-149">CommonParameters</span></span>
<span data-ttu-id="2c980-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c980-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c980-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c980-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c980-152">입력</span><span class="sxs-lookup"><span data-stu-id="2c980-152">INPUTS</span></span>

### <span data-ttu-id="2c980-153">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2c980-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="2c980-154">출력</span><span class="sxs-lookup"><span data-stu-id="2c980-154">OUTPUTS</span></span>

### <span data-ttu-id="2c980-155">Microsoft. KeyVault. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c980-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2c980-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2c980-156">NOTES</span></span>

## <span data-ttu-id="2c980-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c980-157">RELATED LINKS</span></span>

[<span data-ttu-id="2c980-158">Az의 KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c980-158">Az.KeyVault</span></span>](/powershell/module/az.keyvault)