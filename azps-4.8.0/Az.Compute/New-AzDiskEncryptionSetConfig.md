---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049140"
---
# <span data-ttu-id="115e7-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="115e7-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="115e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="115e7-102">SYNOPSIS</span></span>
<span data-ttu-id="115e7-103">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="115e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="115e7-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="115e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="115e7-105">DESCRIPTION</span></span>
<span data-ttu-id="115e7-106">구성 가능한 디스크 암호화 집합 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="115e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="115e7-107">EXAMPLES</span></span>

### <span data-ttu-id="115e7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="115e7-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="115e7-109">키 자격 증명 모음에서 지정 된 활성 키를 사용 하 여 디스크 암호화 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="115e7-110">변수</span><span class="sxs-lookup"><span data-stu-id="115e7-110">PARAMETERS</span></span>

### <span data-ttu-id="115e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115e7-111">-DefaultProfile</span></span>
<span data-ttu-id="115e7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="115e7-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="115e7-113">-EncryptionType</span></span>
<span data-ttu-id="115e7-114">이를 사용 하 여 디스크 암호화 집합의 암호화 유형을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="115e7-115">사용 가능한 값은 ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '입니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

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

### <span data-ttu-id="115e7-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="115e7-116">-IdentityType</span></span>
<span data-ttu-id="115e7-117">Diska Set에 사용 되는 관리 되는 Id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="115e7-118">할당 된 시스템만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="115e7-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="115e7-119">-KeyUrl</span></span>
<span data-ttu-id="115e7-120">KeyVault의 활성 키를 가리키는 Url</span><span class="sxs-lookup"><span data-stu-id="115e7-120">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="115e7-121">-위치</span><span class="sxs-lookup"><span data-stu-id="115e7-121">-Location</span></span>
<span data-ttu-id="115e7-122">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-122">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115e7-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="115e7-123">-SourceVaultId</span></span>
<span data-ttu-id="115e7-124">활성 키를 포함 하는 KeyVault의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115e7-125">태그</span><span class="sxs-lookup"><span data-stu-id="115e7-125">-Tag</span></span>
<span data-ttu-id="115e7-126">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="115e7-127">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="115e7-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="115e7-128">-확인</span><span class="sxs-lookup"><span data-stu-id="115e7-128">-Confirm</span></span>
<span data-ttu-id="115e7-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="115e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="115e7-130">-WhatIf</span></span>
<span data-ttu-id="115e7-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="115e7-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="115e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115e7-133">CommonParameters</span></span>
<span data-ttu-id="115e7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="115e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115e7-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="115e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115e7-136">입력</span><span class="sxs-lookup"><span data-stu-id="115e7-136">INPUTS</span></span>

### <span data-ttu-id="115e7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="115e7-137">System.String</span></span>

### <span data-ttu-id="115e7-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="115e7-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="115e7-139">출력</span><span class="sxs-lookup"><span data-stu-id="115e7-139">OUTPUTS</span></span>

### <span data-ttu-id="115e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="115e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="115e7-141">상속자</span><span class="sxs-lookup"><span data-stu-id="115e7-141">NOTES</span></span>

## <span data-ttu-id="115e7-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="115e7-142">RELATED LINKS</span></span>