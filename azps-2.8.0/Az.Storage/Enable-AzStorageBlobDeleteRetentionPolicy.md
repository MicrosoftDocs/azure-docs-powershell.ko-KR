---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: fdac081aa6edc5ac43c98800ad2d857cb8f62b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873785"
---
# <span data-ttu-id="32264-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="32264-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="32264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32264-102">SYNOPSIS</span></span>
<span data-ttu-id="32264-103">Azure 저장소 Blob 서비스에 대 한 삭제 보존 정책을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32264-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="32264-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32264-104">SYNTAX</span></span>

### <span data-ttu-id="32264-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="32264-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32264-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="32264-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32264-107">Blobservice속성 Resourceid</span><span class="sxs-lookup"><span data-stu-id="32264-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32264-108">설명은</span><span class="sxs-lookup"><span data-stu-id="32264-108">DESCRIPTION</span></span>
<span data-ttu-id="32264-109">AzStorageBlobDeleteRetentionPolicy cmdlet을 **사용** 하면 Azure 저장소 Blob 서비스에 대 한 삭제 보존 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32264-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="32264-110">예제의</span><span class="sxs-lookup"><span data-stu-id="32264-110">EXAMPLES</span></span>

### <span data-ttu-id="32264-111">예제 1: Blob 서비스에 대 한 삭제 보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="32264-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="32264-112">이 명령은 Blob 서비스에 대 한 삭제 보존 정책을 활성화 하 고 삭제 된 blob 보존 일을 4로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32264-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="32264-113">변수</span><span class="sxs-lookup"><span data-stu-id="32264-113">PARAMETERS</span></span>

### <span data-ttu-id="32264-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32264-114">-DefaultProfile</span></span>
<span data-ttu-id="32264-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32264-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32264-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32264-116">-PassThru</span></span>
<span data-ttu-id="32264-117">ServiceProperties 표시</span><span class="sxs-lookup"><span data-stu-id="32264-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="32264-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32264-118">-ResourceGroupName</span></span>
<span data-ttu-id="32264-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32264-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32264-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32264-120">-ResourceId</span></span>
<span data-ttu-id="32264-121">저장소 계정 리소스 Id 또는 Blob 서비스 속성 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="32264-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32264-122">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="32264-122">-RetentionDays</span></span>
<span data-ttu-id="32264-123">DeleteRetentionPolicy 보존 일 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32264-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32264-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="32264-124">-StorageAccount</span></span>
<span data-ttu-id="32264-125">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="32264-125">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32264-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="32264-126">-StorageAccountName</span></span>
<span data-ttu-id="32264-127">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32264-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32264-128">-확인</span><span class="sxs-lookup"><span data-stu-id="32264-128">-Confirm</span></span>
<span data-ttu-id="32264-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32264-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32264-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32264-130">-WhatIf</span></span>
<span data-ttu-id="32264-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32264-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32264-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32264-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32264-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32264-133">CommonParameters</span></span>
<span data-ttu-id="32264-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32264-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32264-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32264-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32264-136">입력</span><span class="sxs-lookup"><span data-stu-id="32264-136">INPUTS</span></span>

### <span data-ttu-id="32264-137">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="32264-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="32264-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32264-138">System.String</span></span>

## <span data-ttu-id="32264-139">출력</span><span class="sxs-lookup"><span data-stu-id="32264-139">OUTPUTS</span></span>

### <span data-ttu-id="32264-140">Microsoft. a. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="32264-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="32264-141">상속자</span><span class="sxs-lookup"><span data-stu-id="32264-141">NOTES</span></span>

## <span data-ttu-id="32264-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32264-142">RELATED LINKS</span></span>