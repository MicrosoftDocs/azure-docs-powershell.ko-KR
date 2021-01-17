---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372793"
---
# <span data-ttu-id="e5f43-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5f43-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e5f43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f43-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f43-103">KeyVault 관리 저장소 계정을 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="e5f43-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5f43-104">SYNTAX</span></span>

### <span data-ttu-id="e5f43-105">ByStorageAccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5f43-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5f43-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5f43-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f43-107">설명</span><span class="sxs-lookup"><span data-stu-id="e5f43-107">DESCRIPTION</span></span>
<span data-ttu-id="e5f43-108">**Backup-AzKeyVaultManagedStorageAccount** cmdlet은 키 자격 증명 모음에 지정된 관리 저장소 계정을 다운로드하고 파일에 저장하여 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="e5f43-109">다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="e5f43-110">자격 증명 모음이 동일한 Azure 지리에 있는 한 백업된 저장소 계정을 백업된 구독의 키 자격 증명 모음으로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="e5f43-111">이 cmdlet을 사용하는 일반적인 이유는</span><span class="sxs-lookup"><span data-stu-id="e5f43-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="e5f43-112">자격 증명 모음에서 원본을 실수로 삭제하는 경우 저장소 계정의 오프라인 복사본을 유지하려는 경우</span><span class="sxs-lookup"><span data-stu-id="e5f43-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="e5f43-113">Key Vault를 사용하여 관리되는 저장소 계정을 만들었다가 이제 개체를 다른 Azure 지역에 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있도록 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="e5f43-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="e5f43-114">**Backup-AzKeyVaultManagedStorageAccount** cmdlet을 사용하여 암호화된 형식으로 관리되는 저장소 계정을 검색한 다음 **Restore-AzKeyVaultManagedStorageAccount** cmdlet을 사용하여 두 번째 지역에서 키 자격 증명 모음을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="e5f43-115">예제</span><span class="sxs-lookup"><span data-stu-id="e5f43-115">EXAMPLES</span></span>

### <span data-ttu-id="e5f43-116">예제 1: 자동으로 생성된 파일 이름으로 관리되는 저장소 계정 백업</span><span class="sxs-lookup"><span data-stu-id="e5f43-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="e5f43-117">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyMSAK라는 관리 저장소 계정을 검색하고 해당 관리 저장소 계정의 백업을 자동으로 명명된 파일에 저장하고 파일 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="e5f43-118">예제 2: 지정된 파일 이름에 관리되는 저장소 계정 백업</span><span class="sxs-lookup"><span data-stu-id="e5f43-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="e5f43-119">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyMSAK라는 관리 저장소 계정을 검색하고 해당 관리 저장소 계정의 백업을 Backup.blob이라는 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="e5f43-120">예제 3: 이전에 검색한 관리되는 저장소 계정을 지정된 파일 이름에 백업하여 메시지를 표시하지 않고 대상 파일을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="e5f43-121">이 명령은 관리되는 저장소 계정의 백업을 $msak. 자격 증명 모음의 이름입니다$msak. VaultName을 Backup.blob이라는 파일에 저장하고, 파일이 이미 있는 경우 파일을 자동으로 덮어써야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="e5f43-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5f43-122">PARAMETERS</span></span>

### <span data-ttu-id="e5f43-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f43-123">-DefaultProfile</span></span>
<span data-ttu-id="e5f43-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5f43-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e5f43-125">-Force</span></span>
<span data-ttu-id="e5f43-126">주어진 파일이 있는 경우 덮어 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="e5f43-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="e5f43-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5f43-127">-InputObject</span></span>
<span data-ttu-id="e5f43-128">백업할 저장소 계정 번들입니다. 검색 호출의 출력에서 파이프라인됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f43-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e5f43-129">-Name</span></span>
<span data-ttu-id="e5f43-130">비밀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-130">Secret name.</span></span>
<span data-ttu-id="e5f43-131">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 비밀 이름에서 비밀의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f43-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e5f43-132">-OutputFile</span></span>
<span data-ttu-id="e5f43-133">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-133">Output file.</span></span>
<span data-ttu-id="e5f43-134">저장소 계정 백업을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="e5f43-135">지정하지 않으면 기본 파일 이름도 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f43-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e5f43-136">-VaultName</span></span>
<span data-ttu-id="e5f43-137">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-137">Vault name.</span></span>
<span data-ttu-id="e5f43-138">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f43-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5f43-139">-Confirm</span></span>
<span data-ttu-id="e5f43-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f43-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f43-141">-WhatIf</span></span>
<span data-ttu-id="e5f43-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e5f43-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f43-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f43-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f43-144">CommonParameters</span></span>
<span data-ttu-id="e5f43-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f43-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f43-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5f43-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f43-147">입력</span><span class="sxs-lookup"><span data-stu-id="e5f43-147">INPUTS</span></span>

### <span data-ttu-id="e5f43-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e5f43-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e5f43-149">출력</span><span class="sxs-lookup"><span data-stu-id="e5f43-149">OUTPUTS</span></span>

### <span data-ttu-id="e5f43-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e5f43-150">System.String</span></span>

## <span data-ttu-id="e5f43-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5f43-151">NOTES</span></span>

## <span data-ttu-id="e5f43-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5f43-152">RELATED LINKS</span></span>