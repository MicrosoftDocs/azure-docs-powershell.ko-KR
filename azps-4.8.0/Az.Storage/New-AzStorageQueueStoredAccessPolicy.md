---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047516"
---
# <span data-ttu-id="5feee-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5feee-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="5feee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5feee-102">SYNOPSIS</span></span>
<span data-ttu-id="5feee-103">Azure 저장소 큐에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="5feee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5feee-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5feee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5feee-105">DESCRIPTION</span></span>
<span data-ttu-id="5feee-106">**AzStorageQueueStoredAccessPolicy** Cmdlet은 Azure 저장소 큐에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="5feee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5feee-107">EXAMPLES</span></span>

### <span data-ttu-id="5feee-108">예제 1: 저장소 큐에 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="5feee-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="5feee-109">이 명령은 MyQueue 이라는 저장소 큐에 Policy01 라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="5feee-110">변수</span><span class="sxs-lookup"><span data-stu-id="5feee-110">PARAMETERS</span></span>

### <span data-ttu-id="5feee-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="5feee-111">-Context</span></span>
<span data-ttu-id="5feee-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5feee-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5feee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5feee-114">-DefaultProfile</span></span>
<span data-ttu-id="5feee-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5feee-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5feee-116">-ExpiryTime</span></span>
<span data-ttu-id="5feee-117">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5feee-118">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="5feee-118">-Permission</span></span>
<span data-ttu-id="5feee-119">저장 된 액세스 정책에서 저장소 큐에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="5feee-120">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="5feee-121">-정책</span><span class="sxs-lookup"><span data-stu-id="5feee-121">-Policy</span></span>
<span data-ttu-id="5feee-122">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5feee-123">-큐</span><span class="sxs-lookup"><span data-stu-id="5feee-123">-Queue</span></span>
<span data-ttu-id="5feee-124">Azure 저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-124">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5feee-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5feee-125">-StartTime</span></span>
<span data-ttu-id="5feee-126">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-126">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5feee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5feee-127">CommonParameters</span></span>
<span data-ttu-id="5feee-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5feee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5feee-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5feee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5feee-130">입력</span><span class="sxs-lookup"><span data-stu-id="5feee-130">INPUTS</span></span>

### <span data-ttu-id="5feee-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5feee-131">System.String</span></span>

### <span data-ttu-id="5feee-132">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5feee-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5feee-133">출력</span><span class="sxs-lookup"><span data-stu-id="5feee-133">OUTPUTS</span></span>

### <span data-ttu-id="5feee-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5feee-134">System.String</span></span>

## <span data-ttu-id="5feee-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5feee-135">NOTES</span></span>

## <span data-ttu-id="5feee-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5feee-136">RELATED LINKS</span></span>

[<span data-ttu-id="5feee-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5feee-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5feee-138">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5feee-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5feee-139">제거-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5feee-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5feee-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5feee-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

