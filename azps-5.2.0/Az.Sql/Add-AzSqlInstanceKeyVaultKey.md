---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332421"
---
# <span data-ttu-id="84b73-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="84b73-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="84b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84b73-102">SYNOPSIS</span></span>
<span data-ttu-id="84b73-103">제공된 Managed Instance에 키 자격 증명 모음 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="84b73-104">구문</span><span class="sxs-lookup"><span data-stu-id="84b73-104">SYNTAX</span></span>

### <span data-ttu-id="84b73-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="84b73-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b73-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84b73-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84b73-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84b73-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b73-108">설명</span><span class="sxs-lookup"><span data-stu-id="84b73-108">DESCRIPTION</span></span>
<span data-ttu-id="84b73-109">Add-AzSqlInstanceKeyVaultKey cmdlet은 제공된 Managed Instance에 키 자격 증명 모음 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="84b73-110">관리되는 인스턴스에는 자격 증명 모음에 대한 'get, wrapKey, unwrapKey' 권한이 있어야 합니다. 다음 스크립트를 사용하여 관리되는 인스턴스에 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="84b73-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="84b73-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="84b73-112">예제</span><span class="sxs-lookup"><span data-stu-id="84b73-112">EXAMPLES</span></span>

### <span data-ttu-id="84b73-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="84b73-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="84b73-114">이 명령은 리소스 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 그룹 'ContosoResourceGroup'에서 'ContosoManagedInstanceName'이라는 SQL 관리되는 인스턴스에 Id '가 있는 Key Vault 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="84b73-115">예제 2: 관리되는 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="84b73-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="84b73-116">이 명령은 리소스 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 그룹 'ContosoResourceGroup'에서 'ContosoManagedInstanceName'이라는 SQL 관리되는 인스턴스에 Id '가 있는 Key Vault 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="84b73-117">예제 3: 관리되는 인스턴스 리소스 ID 사용</span><span class="sxs-lookup"><span data-stu-id="84b73-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="84b73-118">이 명령은 리소스 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 그룹 'ContosoResourceGroup'에서 'ContosoManagedInstanceName'이라는 SQL 관리되는 인스턴스에 Id '가 있는 Key Vault 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="84b73-119">예제 4: 파이핑 사용</span><span class="sxs-lookup"><span data-stu-id="84b73-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="84b73-120">이 명령은 리소스 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 그룹 'ContosoResourceGroup'에서 'ContosoManagedInstanceName'이라는 SQL 관리되는 인스턴스에 Id '가 있는 Key Vault 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="84b73-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84b73-121">PARAMETERS</span></span>

### <span data-ttu-id="84b73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b73-122">-DefaultProfile</span></span>
<span data-ttu-id="84b73-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84b73-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="84b73-124">-Instance</span></span>
<span data-ttu-id="84b73-125">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="84b73-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b73-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="84b73-126">-InstanceName</span></span>
<span data-ttu-id="84b73-127">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="84b73-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b73-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="84b73-128">-InstanceResourceId</span></span>
<span data-ttu-id="84b73-129">인스턴스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="84b73-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b73-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="84b73-130">-KeyId</span></span>
<span data-ttu-id="84b73-131">AzureKeyVault 키 ID</span><span class="sxs-lookup"><span data-stu-id="84b73-131">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b73-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b73-132">-ResourceGroupName</span></span>
<span data-ttu-id="84b73-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="84b73-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b73-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84b73-134">-Confirm</span></span>
<span data-ttu-id="84b73-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b73-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b73-136">-WhatIf</span></span>
<span data-ttu-id="84b73-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="84b73-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b73-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b73-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b73-139">CommonParameters</span></span>
<span data-ttu-id="84b73-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84b73-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b73-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84b73-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b73-142">입력</span><span class="sxs-lookup"><span data-stu-id="84b73-142">INPUTS</span></span>

### <span data-ttu-id="84b73-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="84b73-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="84b73-144">System.String</span><span class="sxs-lookup"><span data-stu-id="84b73-144">System.String</span></span>

## <span data-ttu-id="84b73-145">출력</span><span class="sxs-lookup"><span data-stu-id="84b73-145">OUTPUTS</span></span>

### <span data-ttu-id="84b73-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="84b73-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="84b73-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84b73-147">NOTES</span></span>

## <span data-ttu-id="84b73-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84b73-148">RELATED LINKS</span></span>