---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212043"
---
# <span data-ttu-id="a1700-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a1700-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="a1700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1700-102">SYNOPSIS</span></span>
<span data-ttu-id="a1700-103">저장소 blob 컨테이너 수정</span><span class="sxs-lookup"><span data-stu-id="a1700-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="a1700-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1700-104">SYNTAX</span></span>

### <span data-ttu-id="a1700-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1700-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1700-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a1700-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1700-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a1700-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1700-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a1700-108">DESCRIPTION</span></span>
<span data-ttu-id="a1700-109">**업데이트 AzRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="a1700-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a1700-110">EXAMPLES</span></span>

### <span data-ttu-id="a1700-111">예제 1: 저장소 blob 컨테이너의 메타 데이터 및 저장소 계정 이름과 컨테이너 이름을 사용 하 여 공용 액세스 수정</span><span class="sxs-lookup"><span data-stu-id="a1700-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="a1700-112">이 명령은 저장소 blob 컨테이너의 메타 데이터 및 저장소 계정 이름과 컨테이너 이름을 사용 하 여 공용 액세스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="a1700-113">예제 2: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 공용 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a1700-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="a1700-114">이 명령은 저장소 계정 개체와 컨테이너 이름을 가진 저장소 blob 컨테이너에서 공용 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="a1700-115">예제 3: 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너에 대 한 Blob로 공용 액세스 설정</span><span class="sxs-lookup"><span data-stu-id="a1700-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="a1700-116">이 명령은 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너에 대해 공용 액세스를 Blob로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="a1700-117">변수</span><span class="sxs-lookup"><span data-stu-id="a1700-117">PARAMETERS</span></span>

### <span data-ttu-id="a1700-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1700-118">-DefaultProfile</span></span>
<span data-ttu-id="a1700-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1700-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1700-120">-InputObject</span></span>
<span data-ttu-id="a1700-121">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="a1700-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1700-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a1700-122">-Metadata</span></span>
<span data-ttu-id="a1700-123">컨테이너 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="a1700-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1700-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a1700-124">-Name</span></span>
<span data-ttu-id="a1700-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="a1700-125">Container Name</span></span>

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

### <span data-ttu-id="a1700-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="a1700-126">-PublicAccess</span></span>
<span data-ttu-id="a1700-127">컨테이너 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="a1700-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1700-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1700-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1700-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1700-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1700-130">-StorageAccount</span></span>
<span data-ttu-id="a1700-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="a1700-131">Storage account object</span></span>

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

### <span data-ttu-id="a1700-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a1700-132">-StorageAccountName</span></span>
<span data-ttu-id="a1700-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="a1700-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a1700-134">-Confirm</span></span>
<span data-ttu-id="a1700-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1700-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1700-136">-WhatIf</span></span>
<span data-ttu-id="a1700-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1700-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1700-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1700-139">CommonParameters</span></span>
<span data-ttu-id="a1700-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1700-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1700-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1700-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1700-142">입력</span><span class="sxs-lookup"><span data-stu-id="a1700-142">INPUTS</span></span>

### <span data-ttu-id="a1700-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1700-143">System.String</span></span>

### <span data-ttu-id="a1700-144">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1700-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a1700-145">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a1700-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a1700-146">출력</span><span class="sxs-lookup"><span data-stu-id="a1700-146">OUTPUTS</span></span>

### <span data-ttu-id="a1700-147">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a1700-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a1700-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a1700-148">NOTES</span></span>

## <span data-ttu-id="a1700-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1700-149">RELATED LINKS</span></span>