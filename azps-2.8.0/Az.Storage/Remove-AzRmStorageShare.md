---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageShare.md
ms.openlocfilehash: 3c4071d11e521476f02cadb7323267f84183510b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874248"
---
# <span data-ttu-id="8eb01-101">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="8eb01-101">Remove-AzRmStorageShare</span></span>

## <span data-ttu-id="8eb01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eb01-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb01-103">저장소 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-103">Removes a Storage file share.</span></span>

## <span data-ttu-id="8eb01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8eb01-104">SYNTAX</span></span>

### <span data-ttu-id="8eb01-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8eb01-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eb01-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8eb01-106">AccountObject</span></span>
```
Remove-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eb01-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="8eb01-107">ShareResourceId</span></span>
```
Remove-AzRmStorageShare [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eb01-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="8eb01-108">ShareObject</span></span>
```
Remove-AzRmStorageShare -InputObject <PSShare> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eb01-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8eb01-109">DESCRIPTION</span></span>
<span data-ttu-id="8eb01-110">**새 AzRmStorageShare** Cmdlet은 저장소 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-110">The **New-AzRmStorageShare** cmdlet removes a Storage file share.</span></span>

## <span data-ttu-id="8eb01-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8eb01-111">EXAMPLES</span></span>

### <span data-ttu-id="8eb01-112">예제 1: 저장소 계정 이름과 공유 이름을 사용 하 여 저장소 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="8eb01-112">Example 1: Remove a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Remove-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"
```

<span data-ttu-id="8eb01-113">이 명령은 저장소 계정 이름과 공유 이름으로 저장소 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-113">This command removes a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="8eb01-114">예제 2: 저장소 계정 개체 및 공유 이름을 사용 하 여 저장소 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="8eb01-114">Example 2: Remove a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageShare -StorageAccount $accountObject -Name "myshare"
```

<span data-ttu-id="8eb01-115">이 명령은 저장소 계정 개체 및 공유 이름으로 저장소 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-115">This command removes a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="8eb01-116">예제 3: 파이프라인을 사용 하 여 저장소 계정에서 모든 저장소 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="8eb01-116">Example 3: Remove all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Remove-AzRmStorageShare -Force
```

<span data-ttu-id="8eb01-117">이 명령은 파이프라인을 사용 하 여 저장소 계정에서 모든 저장소 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-117">This command removes all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8eb01-118">변수</span><span class="sxs-lookup"><span data-stu-id="8eb01-118">PARAMETERS</span></span>

### <span data-ttu-id="8eb01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb01-119">-DefaultProfile</span></span>
<span data-ttu-id="8eb01-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb01-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8eb01-121">-Force</span></span>
<span data-ttu-id="8eb01-122">공유 및 모든 콘텐츠를 강제로 제거</span><span class="sxs-lookup"><span data-stu-id="8eb01-122">Force to remove the Share and all content in it</span></span>

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

### <span data-ttu-id="8eb01-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eb01-123">-InputObject</span></span>
<span data-ttu-id="8eb01-124">저장소 공유 개체</span><span class="sxs-lookup"><span data-stu-id="8eb01-124">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb01-125">-이름</span><span class="sxs-lookup"><span data-stu-id="8eb01-125">-Name</span></span>
<span data-ttu-id="8eb01-126">공유 이름</span><span class="sxs-lookup"><span data-stu-id="8eb01-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb01-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8eb01-127">-PassThru</span></span>
<span data-ttu-id="8eb01-128">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-128">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8eb01-129">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-129">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8eb01-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb01-130">-ResourceGroupName</span></span>
<span data-ttu-id="8eb01-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="8eb01-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eb01-132">-ResourceId</span></span>
<span data-ttu-id="8eb01-133">파일 공유 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-133">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb01-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eb01-134">-StorageAccount</span></span>
<span data-ttu-id="8eb01-135">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="8eb01-135">Storage account object</span></span>

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

### <span data-ttu-id="8eb01-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8eb01-136">-StorageAccountName</span></span>
<span data-ttu-id="8eb01-137">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="8eb01-138">-확인</span><span class="sxs-lookup"><span data-stu-id="8eb01-138">-Confirm</span></span>
<span data-ttu-id="8eb01-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eb01-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb01-140">-WhatIf</span></span>
<span data-ttu-id="8eb01-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eb01-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eb01-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb01-143">CommonParameters</span></span>
<span data-ttu-id="8eb01-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb01-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb01-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb01-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb01-146">입력</span><span class="sxs-lookup"><span data-stu-id="8eb01-146">INPUTS</span></span>

### <span data-ttu-id="8eb01-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8eb01-147">System.String</span></span>

### <span data-ttu-id="8eb01-148">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8eb01-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8eb01-149">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="8eb01-149">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="8eb01-150">출력</span><span class="sxs-lookup"><span data-stu-id="8eb01-150">OUTPUTS</span></span>

### <span data-ttu-id="8eb01-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8eb01-151">System.Boolean</span></span>

## <span data-ttu-id="8eb01-152">상속자</span><span class="sxs-lookup"><span data-stu-id="8eb01-152">NOTES</span></span>

## <span data-ttu-id="8eb01-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8eb01-153">RELATED LINKS</span></span>