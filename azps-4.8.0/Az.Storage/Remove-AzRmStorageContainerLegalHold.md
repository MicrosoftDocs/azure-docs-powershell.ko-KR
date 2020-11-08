---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213183"
---
# <span data-ttu-id="a46e8-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a46e8-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="a46e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a46e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a46e8-103">저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="a46e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a46e8-104">SYNTAX</span></span>

### <span data-ttu-id="a46e8-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a46e8-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a46e8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a46e8-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a46e8-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a46e8-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a46e8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a46e8-108">DESCRIPTION</span></span>
<span data-ttu-id="a46e8-109">**AzRmStorageContainerLegalHold** Cmdlet은 저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="a46e8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a46e8-110">EXAMPLES</span></span>

### <span data-ttu-id="a46e8-111">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너에서 법률 보존 태그 제거</span><span class="sxs-lookup"><span data-stu-id="a46e8-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="a46e8-112">이 명령은 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a46e8-113">예제 2: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 법률 보존 태그 제거</span><span class="sxs-lookup"><span data-stu-id="a46e8-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="a46e8-114">이 명령은 저장소 계정 개체와 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="a46e8-115">예제 3: 파이프라인을 사용 하 여 저장소 계정의 모든 저장소 blob 컨테이너에서 올바른 보류 태그 제거</span><span class="sxs-lookup"><span data-stu-id="a46e8-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="a46e8-116">이 명령은 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너에서 유지 되는 legal 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="a46e8-117">변수</span><span class="sxs-lookup"><span data-stu-id="a46e8-117">PARAMETERS</span></span>

### <span data-ttu-id="a46e8-118">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="a46e8-118">-Container</span></span>
<span data-ttu-id="a46e8-119">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="a46e8-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a46e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46e8-120">-DefaultProfile</span></span>
<span data-ttu-id="a46e8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a46e8-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a46e8-122">-Name</span></span>
<span data-ttu-id="a46e8-123">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="a46e8-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a46e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="a46e8-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46e8-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a46e8-126">-StorageAccount</span></span>
<span data-ttu-id="a46e8-127">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="a46e8-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a46e8-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a46e8-128">-StorageAccountName</span></span>
<span data-ttu-id="a46e8-129">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46e8-130">태그</span><span class="sxs-lookup"><span data-stu-id="a46e8-130">-Tag</span></span>
<span data-ttu-id="a46e8-131">컨테이너 LegalHold 태그</span><span class="sxs-lookup"><span data-stu-id="a46e8-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46e8-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a46e8-132">-Confirm</span></span>
<span data-ttu-id="a46e8-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a46e8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a46e8-134">-WhatIf</span></span>
<span data-ttu-id="a46e8-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a46e8-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a46e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46e8-137">CommonParameters</span></span>
<span data-ttu-id="a46e8-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46e8-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46e8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46e8-140">입력</span><span class="sxs-lookup"><span data-stu-id="a46e8-140">INPUTS</span></span>

### <span data-ttu-id="a46e8-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a46e8-141">System.String</span></span>

### <span data-ttu-id="a46e8-142">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a46e8-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a46e8-143">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a46e8-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a46e8-144">출력</span><span class="sxs-lookup"><span data-stu-id="a46e8-144">OUTPUTS</span></span>

### <span data-ttu-id="a46e8-145">PSLegalHold를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46e8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="a46e8-146">상속자</span><span class="sxs-lookup"><span data-stu-id="a46e8-146">NOTES</span></span>

## <span data-ttu-id="a46e8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a46e8-147">RELATED LINKS</span></span>