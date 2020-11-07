---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 51b8af420ee619b3b07dfab8d03532c076312dc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873575"
---
# <span data-ttu-id="57bfd-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57bfd-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="57bfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="57bfd-103">SQL 관리 인스턴스에서 키 보관소 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="57bfd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57bfd-104">SYNTAX</span></span>

### <span data-ttu-id="57bfd-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="57bfd-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57bfd-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57bfd-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57bfd-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57bfd-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57bfd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="57bfd-108">DESCRIPTION</span></span>
<span data-ttu-id="57bfd-109">Remove-AzSqlInstanceKeyVaultKey cmdlet은 지정 된 관리 되는 인스턴스에서 키 자격 증명 모음 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="57bfd-110">키 보관소에 대 한 SQL 관리 인스턴스의 권한은 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="57bfd-111">사용 권한을 변경 하려면 Set-AzKeyVaultAccessPolicy를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="57bfd-112">이 cmdlet은 키 자격 증명을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="57bfd-113">키 자격 증명 모음에서 키를 제거 하려면 AzureKeyVaultKey를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="57bfd-114">예제의</span><span class="sxs-lookup"><span data-stu-id="57bfd-114">EXAMPLES</span></span>

### <span data-ttu-id="57bfd-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="57bfd-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="57bfd-116">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지정 된 관리 되는 인스턴스에서 Id가 ' ' 인 키 보관소 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="57bfd-117">예제 2: 관리 되는 인스턴스 개체 사용</span><span class="sxs-lookup"><span data-stu-id="57bfd-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="57bfd-118">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지정 된 관리 되는 인스턴스에서 Id가 ' ' 인 키 보관소 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="57bfd-119">예제 3: 관리 되는 인스턴스 리소스 id 사용</span><span class="sxs-lookup"><span data-stu-id="57bfd-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="57bfd-120">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지정 된 관리 되는 인스턴스에서 Id가 ' ' 인 키 보관소 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="57bfd-121">예제 4: 배관 사용</span><span class="sxs-lookup"><span data-stu-id="57bfd-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="57bfd-122">이 명령은 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지정 된 관리 되는 인스턴스에서 Id가 ' ' 인 키 보관소 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="57bfd-123">변수</span><span class="sxs-lookup"><span data-stu-id="57bfd-123">PARAMETERS</span></span>

### <span data-ttu-id="57bfd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bfd-124">-DefaultProfile</span></span>
<span data-ttu-id="57bfd-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57bfd-126">-인스턴스</span><span class="sxs-lookup"><span data-stu-id="57bfd-126">-Instance</span></span>
<span data-ttu-id="57bfd-127">인스턴스 입력 개체</span><span class="sxs-lookup"><span data-stu-id="57bfd-127">The instance input object</span></span>

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

### <span data-ttu-id="57bfd-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="57bfd-128">-InstanceName</span></span>
<span data-ttu-id="57bfd-129">인스턴스 이름</span><span class="sxs-lookup"><span data-stu-id="57bfd-129">The instance name</span></span>

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

### <span data-ttu-id="57bfd-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="57bfd-130">-InstanceResourceId</span></span>
<span data-ttu-id="57bfd-131">인스턴스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="57bfd-131">The instance resource id</span></span>

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

### <span data-ttu-id="57bfd-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="57bfd-132">-KeyId</span></span>
<span data-ttu-id="57bfd-133">AzureKeyVault 키 id</span><span class="sxs-lookup"><span data-stu-id="57bfd-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="57bfd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57bfd-134">-ResourceGroupName</span></span>
<span data-ttu-id="57bfd-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="57bfd-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="57bfd-136">-확인</span><span class="sxs-lookup"><span data-stu-id="57bfd-136">-Confirm</span></span>
<span data-ttu-id="57bfd-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57bfd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57bfd-138">-WhatIf</span></span>
<span data-ttu-id="57bfd-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57bfd-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57bfd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bfd-141">CommonParameters</span></span>
<span data-ttu-id="57bfd-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57bfd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bfd-143">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57bfd-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bfd-144">입력</span><span class="sxs-lookup"><span data-stu-id="57bfd-144">INPUTS</span></span>

### <span data-ttu-id="57bfd-145">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="57bfd-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="57bfd-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57bfd-146">System.String</span></span>

## <span data-ttu-id="57bfd-147">출력</span><span class="sxs-lookup"><span data-stu-id="57bfd-147">OUTPUTS</span></span>

### <span data-ttu-id="57bfd-148">TransparentDataEncryption. AzureRmSqlManagedInstanceKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="57bfd-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="57bfd-149">상속자</span><span class="sxs-lookup"><span data-stu-id="57bfd-149">NOTES</span></span>

## <span data-ttu-id="57bfd-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57bfd-150">RELATED LINKS</span></span>