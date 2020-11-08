---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226056"
---
# <span data-ttu-id="c5448-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c5448-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="c5448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5448-102">SYNOPSIS</span></span>
<span data-ttu-id="c5448-103">잠기지 않은 정책으로 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="c5448-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5448-104">SYNTAX</span></span>

### <span data-ttu-id="c5448-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5448-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5448-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c5448-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5448-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="c5448-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5448-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c5448-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5448-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c5448-109">DESCRIPTION</span></span>
<span data-ttu-id="c5448-110">**AzRmStorageContainerImmutabilityPolicy** cmdlet은 잠기지 않은 정책으로 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="c5448-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c5448-111">EXAMPLES</span></span>

### <span data-ttu-id="c5448-112">예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 잠금 해제 된 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="c5448-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="c5448-113">이 명령은 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 잠금 해제 된 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c5448-114">예제 2: 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 잠기지 않은 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="c5448-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="c5448-115">이 명령은 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 잠금 해제 된 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="c5448-116">예제 3: 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 잠기지 않은 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="c5448-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="c5448-117">이 명령은 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 잠금 해제 된 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="c5448-118">예제 4: ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 잠기지 않은 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="c5448-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="c5448-119">이 명령은 ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 잠금 해제 된 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="c5448-120">변수</span><span class="sxs-lookup"><span data-stu-id="c5448-120">PARAMETERS</span></span>

### <span data-ttu-id="c5448-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="c5448-121">-Container</span></span>
<span data-ttu-id="c5448-122">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="c5448-122">Storage container object</span></span>

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

### <span data-ttu-id="c5448-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c5448-123">-ContainerName</span></span>
<span data-ttu-id="c5448-124">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="c5448-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5448-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5448-125">-DefaultProfile</span></span>
<span data-ttu-id="c5448-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5448-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="c5448-127">-Etag</span></span>
<span data-ttu-id="c5448-128">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="c5448-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5448-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5448-129">-InputObject</span></span>
<span data-ttu-id="c5448-130">제거할 잠금 해제 된 ImmutabilityPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="c5448-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5448-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5448-131">-ResourceGroupName</span></span>
<span data-ttu-id="c5448-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5448-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5448-133">-StorageAccount</span></span>
<span data-ttu-id="c5448-134">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c5448-134">Storage account object</span></span>

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

### <span data-ttu-id="c5448-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c5448-135">-StorageAccountName</span></span>
<span data-ttu-id="c5448-136">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="c5448-137">-확인</span><span class="sxs-lookup"><span data-stu-id="c5448-137">-Confirm</span></span>
<span data-ttu-id="c5448-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5448-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5448-139">-WhatIf</span></span>
<span data-ttu-id="c5448-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5448-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5448-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5448-142">CommonParameters</span></span>
<span data-ttu-id="c5448-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5448-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5448-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5448-145">입력</span><span class="sxs-lookup"><span data-stu-id="c5448-145">INPUTS</span></span>

### <span data-ttu-id="c5448-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5448-146">System.String</span></span>

### <span data-ttu-id="c5448-147">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c5448-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c5448-148">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="c5448-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="c5448-149">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="c5448-150">출력</span><span class="sxs-lookup"><span data-stu-id="c5448-150">OUTPUTS</span></span>

### <span data-ttu-id="c5448-151">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5448-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="c5448-152">상속자</span><span class="sxs-lookup"><span data-stu-id="c5448-152">NOTES</span></span>

## <span data-ttu-id="c5448-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5448-153">RELATED LINKS</span></span>