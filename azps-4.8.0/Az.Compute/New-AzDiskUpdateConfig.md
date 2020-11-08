---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: 9c267a01629922408f25669ab93aa9a20a01b02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049136"
---
# <span data-ttu-id="b4e3a-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b4e3a-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="b4e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e3a-103">구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="b4e3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4e3a-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e3a-106">**AzDiskUpdateConfig** cmdlet은 구성 가능한 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="b4e3a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b4e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e3a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4e3a-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="b4e3a-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="b4e3a-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="b4e3a-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="b4e3a-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b4e3a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b4e3a-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="b4e3a-114">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b4e3a-115">변수</span><span class="sxs-lookup"><span data-stu-id="b4e3a-115">PARAMETERS</span></span>

### <span data-ttu-id="b4e3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e3a-116">-DefaultProfile</span></span>
<span data-ttu-id="b4e3a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4e3a-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="b4e3a-118">-DiskAccessId</span></span>
<span data-ttu-id="b4e3a-119">{{Fill DiskAccessId Description}}</span><span class="sxs-lookup"><span data-stu-id="b4e3a-119">{{ Fill DiskAccessId Description }}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b4e3a-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="b4e3a-121">디스크의 디스크 암호화 키 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-121">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-122">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="b4e3a-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b4e3a-123">나머지 암호화를 사용 하는 데 사용할 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-124">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4e3a-124">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="b4e3a-125">이 디스크에 허용 되는 IOPS 수입니다. UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-125">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="b4e3a-126">1 개의 작업은 4k와 256k 바이트 간에 전송할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-127">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4e3a-127">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="b4e3a-128">이 디스크에 허용 되는 대역폭 UltraSSD 디스크에만 설정 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-128">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="b4e3a-129">MBps는 초당 수백만 바이트의 수를 의미 합니다. 여기서는 ISO 표기법을 10의 거듭제곱으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-129">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-130">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b4e3a-130">-DiskSizeGB</span></span>
<span data-ttu-id="b4e3a-131">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-131">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-132">-# Settingsenabled</span><span class="sxs-lookup"><span data-stu-id="b4e3a-132">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b4e3a-133">암호화 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-133">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-134">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="b4e3a-134">-EncryptionType</span></span>
<span data-ttu-id="b4e3a-135">디스크의 데이터를 암호화 하는 데 사용 되는 키 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-135">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="b4e3a-136">사용 가능한 값은 ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '입니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-136">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-137">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b4e3a-137">-KeyEncryptionKey</span></span>
<span data-ttu-id="b4e3a-138">디스크의 키 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-138">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-139">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b4e3a-139">-NetworkAccessPolicy</span></span>
<span data-ttu-id="b4e3a-140">{{NetworkAccessPolicy 채우기 설명}}</span><span class="sxs-lookup"><span data-stu-id="b4e3a-140">{{ Fill NetworkAccessPolicy Description }}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="b4e3a-141">-OsType</span></span>
<span data-ttu-id="b4e3a-142">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-142">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-143">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="b4e3a-143">-SkuName</span></span>
<span data-ttu-id="b4e3a-144">저장소 계정의 Sku 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-144">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="b4e3a-145">사용할 수 있는 값은 Standard_LRS, Premium_LRS, StandardSSD_LRS, UltraSSD_LRS입니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-145">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="b4e3a-146">UltraSSD_LRS는 CreateOption 매개 변수에 대해 빈 값 으로만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-146">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-147">태그</span><span class="sxs-lookup"><span data-stu-id="b4e3a-147">-Tag</span></span>
<span data-ttu-id="b4e3a-148">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b4e3a-149">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b4e3a-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e3a-150">-확인</span><span class="sxs-lookup"><span data-stu-id="b4e3a-150">-Confirm</span></span>
<span data-ttu-id="b4e3a-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e3a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e3a-152">-WhatIf</span></span>
<span data-ttu-id="b4e3a-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4e3a-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e3a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e3a-155">CommonParameters</span></span>
<span data-ttu-id="b4e3a-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e3a-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e3a-158">입력</span><span class="sxs-lookup"><span data-stu-id="b4e3a-158">INPUTS</span></span>

### <span data-ttu-id="b4e3a-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4e3a-159">System.String</span></span>

### <span data-ttu-id="b4e3a-160">시스템 Null 허용 ' 1 [[OperatingSystemTypes, Microsoft azure. 23.0.0.0, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b4e3a-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b4e3a-161">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-161">System.Int32</span></span>

### <span data-ttu-id="b4e3a-162">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="b4e3a-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b4e3a-163">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b4e3a-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b4e3a-164">KeyVaultAndSecretReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-164">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="b4e3a-165">KeyVaultAndKeyReference를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4e3a-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b4e3a-166">출력</span><span class="sxs-lookup"><span data-stu-id="b4e3a-166">OUTPUTS</span></span>

### <span data-ttu-id="b4e3a-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="b4e3a-167">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="b4e3a-168">상속자</span><span class="sxs-lookup"><span data-stu-id="b4e3a-168">NOTES</span></span>

## <span data-ttu-id="b4e3a-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4e3a-169">RELATED LINKS</span></span>