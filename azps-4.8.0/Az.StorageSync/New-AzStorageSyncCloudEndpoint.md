---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048575"
---
# <span data-ttu-id="5b9a4-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b9a4-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="5b9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9a4-103">이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="5b9a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b9a4-104">SYNTAX</span></span>

### <span data-ttu-id="5b9a4-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5b9a4-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b9a4-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b9a4-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b9a4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b9a4-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b9a4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5b9a4-108">DESCRIPTION</span></span>
<span data-ttu-id="5b9a4-109">이 명령은 Azure 파일 동기화 클라우드 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="5b9a4-110">클라우드 끝점은 기존 Azure 파일 공유에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="5b9a4-111">이는 파일 공유를 나타내며 클라우드 끝점을 만든 동기화 그룹의 모든 파일 부분을 동기화 하는 참여를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="5b9a4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5b9a4-112">EXAMPLES</span></span>

### <span data-ttu-id="5b9a4-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b9a4-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="5b9a4-114">클라우드 끝점은 동기화 그룹의 정수 계열 구성원이 며,이는 "mySyncGroupName" 이라는 기존 동기화 그룹 내에 하나를 만드는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="5b9a4-115">변수</span><span class="sxs-lookup"><span data-stu-id="5b9a4-115">PARAMETERS</span></span>

### <span data-ttu-id="5b9a4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b9a4-116">-AsJob</span></span>
<span data-ttu-id="5b9a4-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5b9a4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b9a4-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="5b9a4-118">-AzureFileShareName</span></span>
<span data-ttu-id="5b9a4-119">저장소 계정 공유 이름 (Azure 파일 공유 이름)</span><span class="sxs-lookup"><span data-stu-id="5b9a4-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9a4-120">-DefaultProfile</span></span>
<span data-ttu-id="5b9a4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b9a4-122">-이름</span><span class="sxs-lookup"><span data-stu-id="5b9a4-122">-Name</span></span>
<span data-ttu-id="5b9a4-123">클라우드 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="5b9a4-124">Azure 포털을 통해 생성 되 면 이름이 참조 하는 Azure 파일 공유의 이름으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b9a4-125">-ParentObject</span></span>
<span data-ttu-id="5b9a4-126">일반적으로 매개 변수를 통해 전달 되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b9a4-127">-ParentResourceId</span></span>
<span data-ttu-id="5b9a4-128">SyncGroup 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5b9a4-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9a4-129">-ResourceGroupName</span></span>
<span data-ttu-id="5b9a4-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5b9a4-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="5b9a4-132">저장소 계정 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="5b9a4-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="5b9a4-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="5b9a4-134">저장소 계정 테 넌 트 Id (회사 디렉터리 Id)</span><span class="sxs-lookup"><span data-stu-id="5b9a4-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-135">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="5b9a4-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="5b9a4-136">Storages<c13> Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9a4-137">-SyncGroupName</span></span>
<span data-ttu-id="5b9a4-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9a4-139">-확인</span><span class="sxs-lookup"><span data-stu-id="5b9a4-139">-Confirm</span></span>
<span data-ttu-id="5b9a4-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b9a4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b9a4-141">-WhatIf</span></span>
<span data-ttu-id="5b9a4-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b9a4-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b9a4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9a4-144">CommonParameters</span></span>
<span data-ttu-id="5b9a4-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b9a4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9a4-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b9a4-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9a4-147">입력</span><span class="sxs-lookup"><span data-stu-id="5b9a4-147">INPUTS</span></span>

### <span data-ttu-id="5b9a4-148">StorageSync. a m m Syncgroup</span><span class="sxs-lookup"><span data-stu-id="5b9a4-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="5b9a4-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b9a4-149">System.String</span></span>

## <span data-ttu-id="5b9a4-150">출력</span><span class="sxs-lookup"><span data-stu-id="5b9a4-150">OUTPUTS</span></span>

### <span data-ttu-id="5b9a4-151">StorageSync. c c i. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b9a4-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="5b9a4-152">상속자</span><span class="sxs-lookup"><span data-stu-id="5b9a4-152">NOTES</span></span>

## <span data-ttu-id="5b9a4-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b9a4-153">RELATED LINKS</span></span>