---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4ef0ffba83fdf24d9808880cda5a7942c1705c8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056731"
---
# <span data-ttu-id="72978-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="72978-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="72978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72978-102">SYNOPSIS</span></span>
<span data-ttu-id="72978-103">디스크 업데이트 개체에서 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="72978-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72978-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72978-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72978-105">DESCRIPTION</span></span>
<span data-ttu-id="72978-106">**Set-AzDiskUpdateDiskEncryptionKey** cmdlet은 디스크 업데이트 개체에서 디스크 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="72978-107">예제의</span><span class="sxs-lookup"><span data-stu-id="72978-107">EXAMPLES</span></span>

### <span data-ttu-id="72978-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="72978-108">Example 1</span></span>
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

<span data-ttu-id="72978-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72978-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="72978-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="72978-111">두 번째 및 세 번째 명령은 디스크 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="72978-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="72978-113">변수</span><span class="sxs-lookup"><span data-stu-id="72978-113">PARAMETERS</span></span>

### <span data-ttu-id="72978-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72978-114">-DefaultProfile</span></span>
<span data-ttu-id="72978-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72978-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72978-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="72978-116">-DiskUpdate</span></span>
<span data-ttu-id="72978-117">로컬 디스크 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72978-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="72978-118">-SecretUrl</span></span>
<span data-ttu-id="72978-119">비밀 Url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-119">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72978-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="72978-120">-SourceVaultId</span></span>
<span data-ttu-id="72978-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72978-122">-확인</span><span class="sxs-lookup"><span data-stu-id="72978-122">-Confirm</span></span>
<span data-ttu-id="72978-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72978-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72978-124">-WhatIf</span></span>
<span data-ttu-id="72978-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72978-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72978-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72978-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72978-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72978-127">CommonParameters</span></span>
<span data-ttu-id="72978-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72978-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72978-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="72978-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72978-130">입력</span><span class="sxs-lookup"><span data-stu-id="72978-130">INPUTS</span></span>

### <span data-ttu-id="72978-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="72978-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="72978-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72978-132">System.String</span></span>

## <span data-ttu-id="72978-133">출력</span><span class="sxs-lookup"><span data-stu-id="72978-133">OUTPUTS</span></span>

### <span data-ttu-id="72978-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="72978-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="72978-135">상속자</span><span class="sxs-lookup"><span data-stu-id="72978-135">NOTES</span></span>

## <span data-ttu-id="72978-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72978-136">RELATED LINKS</span></span>