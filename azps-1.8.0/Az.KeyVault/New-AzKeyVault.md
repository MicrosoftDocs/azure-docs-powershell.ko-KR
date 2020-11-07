---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 08f3b7ebaa7b1bc07bdac10b5b7cc16cb4405534
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867962"
---
# <span data-ttu-id="30f53-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="30f53-101">New-AzKeyVault</span></span>

## <span data-ttu-id="30f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f53-102">SYNOPSIS</span></span>
<span data-ttu-id="30f53-103">키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-103">Creates a key vault.</span></span>

## <span data-ttu-id="30f53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30f53-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30f53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30f53-105">DESCRIPTION</span></span>
<span data-ttu-id="30f53-106">**AzKeyVault** cmdlet은 지정 된 리소스 그룹에 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="30f53-107">또한이 cmdlet은 현재 로그온 한 사용자에 게 키 자격 증명 모음에서 키와 비밀을 추가, 제거 또는 나열할 수 있는 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="30f53-108">참고: 새 키 자격 증명 모음을 만들려고 할 때 **구독이 ' microsoft. KeyVault '을 사용 하도록 등록 되어 있지 않은** 경우 **AzResourceProvider-Providernamespace "Microsoft. keyvault"** 을 실행 한 다음 **새-AzKeyVault** 명령을 다시 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="30f53-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="30f53-109">자세한 내용은 Register-AzResourceProvider를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="30f53-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="30f53-110">예제의</span><span class="sxs-lookup"><span data-stu-id="30f53-110">EXAMPLES</span></span>

### <span data-ttu-id="30f53-111">예제 1: 표준 키 보관소 만들기</span><span class="sxs-lookup"><span data-stu-id="30f53-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="30f53-112">이 명령은 Azure 지역 동부 US에 Contoso03Vault 이라는 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="30f53-113">이 명령은 Group14 이라는 리소스 그룹에 키 보관소를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="30f53-114">명령이 *SKU* 매개 변수에 대 한 값을 지정 하지 않기 때문에 표준 키 자격 증명 모음이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="30f53-115">예제 2: Premium 키 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="30f53-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="30f53-116">이 명령은 이전 예제와 마찬가지로 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="30f53-117">그러나, Premium 키 자격 증명 모음을 만들기 위해 *SKU* 매개 변수에 premium 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="30f53-118">변수</span><span class="sxs-lookup"><span data-stu-id="30f53-118">PARAMETERS</span></span>

### <span data-ttu-id="30f53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f53-119">-DefaultProfile</span></span>
<span data-ttu-id="30f53-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="30f53-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30f53-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="30f53-121">-EnabledForDeployment</span></span>
<span data-ttu-id="30f53-122">이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="30f53-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="30f53-124">Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="30f53-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="30f53-126">이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="30f53-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="30f53-128">지정 된 경우 즉시 삭제에 대 한 보호가이 자격 증명 모음에 대해 사용 하도록 설정 됩니다. 또한 소프트 삭제를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="30f53-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="30f53-129">-EnableSoftDelete</span></span>
<span data-ttu-id="30f53-130">이 키 보관소에 대해 소프트 삭제 기능을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="30f53-131">일시 삭제를 사용 하는 경우 유예 기간 동안이 키 보관소 및 해당 내용이 삭제 된 후 해당 콘텐츠를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="30f53-132">이 기능에 대 한 자세한 내용은 [Azure 키 보관소 소프트-삭제 개요](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="30f53-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="30f53-133">방법 지침은 [PowerShell에서 키 보관소 소프트 삭제를 사용 하는 방법을](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="30f53-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="30f53-134">-위치</span><span class="sxs-lookup"><span data-stu-id="30f53-134">-Location</span></span>
<span data-ttu-id="30f53-135">키 자격 증명 모음을 만들 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="30f53-136">[AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) 명령을 사용 하 여 선택 항목을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-137">-이름</span><span class="sxs-lookup"><span data-stu-id="30f53-137">-Name</span></span>
<span data-ttu-id="30f53-138">만들려는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="30f53-139">이름은 문자, 숫자 또는 하이픈을 임의로 조합 하 여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="30f53-140">이름은 문자 또는 숫자로 시작 하 고 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="30f53-141">이름은 범용으로 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-141">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f53-142">-ResourceGroupName</span></span>
<span data-ttu-id="30f53-143">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-144">-Sku</span><span class="sxs-lookup"><span data-stu-id="30f53-144">-Sku</span></span>
<span data-ttu-id="30f53-145">키 보관소 인스턴스의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="30f53-146">각 SKU에 대해 사용할 수 있는 기능에 대 한 자세한 내용은 Azure 키 보관소 가격 웹 사이트 ()를 참조 하세요 https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="30f53-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f53-147">태그</span><span class="sxs-lookup"><span data-stu-id="30f53-147">-Tag</span></span>
<span data-ttu-id="30f53-148">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30f53-149">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="30f53-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="30f53-150">-확인</span><span class="sxs-lookup"><span data-stu-id="30f53-150">-Confirm</span></span>
<span data-ttu-id="30f53-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f53-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f53-152">-WhatIf</span></span>
<span data-ttu-id="30f53-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f53-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f53-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f53-155">CommonParameters</span></span>
<span data-ttu-id="30f53-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30f53-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f53-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f53-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f53-158">입력</span><span class="sxs-lookup"><span data-stu-id="30f53-158">INPUTS</span></span>

### <span data-ttu-id="30f53-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30f53-159">System.String</span></span>

### <span data-ttu-id="30f53-160">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="30f53-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="30f53-161">Microsoft Azure. KeyVault. 모델.</span><span class="sxs-lookup"><span data-stu-id="30f53-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="30f53-162">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="30f53-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="30f53-163">출력</span><span class="sxs-lookup"><span data-stu-id="30f53-163">OUTPUTS</span></span>

### <span data-ttu-id="30f53-164">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="30f53-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="30f53-165">상속자</span><span class="sxs-lookup"><span data-stu-id="30f53-165">NOTES</span></span>

## <span data-ttu-id="30f53-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30f53-166">RELATED LINKS</span></span>

[<span data-ttu-id="30f53-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="30f53-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="30f53-168">제거-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="30f53-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)