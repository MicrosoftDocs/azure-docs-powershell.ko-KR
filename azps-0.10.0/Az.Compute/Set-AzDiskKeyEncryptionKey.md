---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 09757005b8865652ef4c922c558dbf86e8c68cdc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876910"
---
# <span data-ttu-id="d060a-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d060a-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="d060a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d060a-102">SYNOPSIS</span></span>
<span data-ttu-id="d060a-103">디스크 개체에 대 한 키 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="d060a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d060a-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d060a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d060a-105">DESCRIPTION</span></span>
<span data-ttu-id="d060a-106">**Set-AzDiskKeyEncryptionKey** cmdlet은 disk 개체의 키 암호화 키 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="d060a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d060a-107">EXAMPLES</span></span>

### <span data-ttu-id="d060a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d060a-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="d060a-109">첫 번째 명령은 Standard_LRS 저장소 계정 유형의 크기가 5GB 인 로컬 빈 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d060a-110">또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d060a-111">두 번째 및 세 번째 명령은 disk 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="d060a-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d060a-113">변수</span><span class="sxs-lookup"><span data-stu-id="d060a-113">PARAMETERS</span></span>

### <span data-ttu-id="d060a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d060a-114">-DefaultProfile</span></span>
<span data-ttu-id="d060a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d060a-116">-디스크</span><span class="sxs-lookup"><span data-stu-id="d060a-116">-Disk</span></span>
<span data-ttu-id="d060a-117">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d060a-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d060a-118">-KeyUrl</span></span>
<span data-ttu-id="d060a-119">키 Url을 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-119">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d060a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d060a-120">-SourceVaultId</span></span>
<span data-ttu-id="d060a-121">원본 자격 증명 모음 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d060a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="d060a-122">-Confirm</span></span>
<span data-ttu-id="d060a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d060a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d060a-124">-WhatIf</span></span>
<span data-ttu-id="d060a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d060a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d060a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d060a-127">CommonParameters</span></span>
<span data-ttu-id="d060a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d060a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d060a-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d060a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d060a-130">입력</span><span class="sxs-lookup"><span data-stu-id="d060a-130">INPUTS</span></span>

### <span data-ttu-id="d060a-131">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="d060a-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="d060a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d060a-132">System.String</span></span>

## <span data-ttu-id="d060a-133">출력</span><span class="sxs-lookup"><span data-stu-id="d060a-133">OUTPUTS</span></span>

### <span data-ttu-id="d060a-134">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="d060a-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d060a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d060a-135">NOTES</span></span>

## <span data-ttu-id="d060a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d060a-136">RELATED LINKS</span></span>
