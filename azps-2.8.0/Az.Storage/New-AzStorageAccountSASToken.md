---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 83480321e58d4dbd21d0a13dd6139c2f2d905c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874220"
---
# <span data-ttu-id="fc308-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="fc308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc308-102">SYNOPSIS</span></span>
<span data-ttu-id="fc308-103">계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="fc308-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc308-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc308-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc308-105">DESCRIPTION</span></span>
<span data-ttu-id="fc308-106">**AzStorageSASToken** Cmdlet은 Azure 저장소 계정에 대 한 sa (계정 수준 공유 액세스 서명) 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="fc308-107">SAS 토큰을 사용 하 여 여러 서비스에 대 한 사용 권한을 위임 하거나 개체 수준 SAS 토큰과 함께 사용할 수 없는 서비스에 대 한 사용 권한을 위임할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="fc308-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fc308-108">EXAMPLES</span></span>

### <span data-ttu-id="fc308-109">예제 1: 모든 권한이 있는 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="fc308-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="fc308-110">이 명령은 모든 권한이 있는 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="fc308-111">예제 2: IP 주소 범위에 대 한 계정 수준 SAS 토큰 만들기</span><span class="sxs-lookup"><span data-stu-id="fc308-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="fc308-112">이 명령은 지정 된 IP 주소 범위의 HTTPS 전용 요청에 대 한 계정 수준 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="fc308-113">변수</span><span class="sxs-lookup"><span data-stu-id="fc308-113">PARAMETERS</span></span>

### <span data-ttu-id="fc308-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fc308-114">-Context</span></span>
<span data-ttu-id="fc308-115">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="fc308-116">New-AzStorageContext cmdlet을 사용 하 여 **Azurestoragecontext** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="fc308-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc308-117">-DefaultProfile</span></span>
<span data-ttu-id="fc308-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc308-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fc308-119">-ExpiryTime</span></span>
<span data-ttu-id="fc308-120">공유 액세스 서명이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="fc308-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="fc308-121">-IPAddressOrRange</span></span>
<span data-ttu-id="fc308-122">168.1.5.65 또는 168.1.5.60-168.1.5.70와 같이 요청을 허용 하는 ip 주소 또는 ip 주소의 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="fc308-123">범위는 포함입니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="fc308-124">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="fc308-124">-Permission</span></span>
<span data-ttu-id="fc308-125">저장소 계정에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="fc308-126">사용 권한은 지정 된 리소스 종류와 일치 하는 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="fc308-127">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="fc308-128">허용 되는 사용 권한 값에 대 한 자세한 내용은 계정 SA 만들기를 참조 하세요. https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="fc308-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="fc308-129">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="fc308-129">-Protocol</span></span>
<span data-ttu-id="fc308-130">계정 SA로 작성 된 요청에 허용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="fc308-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc308-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="fc308-132">HttpsOnly</span></span>
- <span data-ttu-id="fc308-133">HttpsOrHttp의 기본값은 HttpsOrHttp입니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc308-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fc308-134">-ResourceType</span></span>
<span data-ttu-id="fc308-135">SAS 토큰과 함께 사용할 수 있는 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="fc308-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc308-137">않아야</span><span class="sxs-lookup"><span data-stu-id="fc308-137">None</span></span>
- <span data-ttu-id="fc308-138">Services</span><span class="sxs-lookup"><span data-stu-id="fc308-138">Service</span></span>
- <span data-ttu-id="fc308-139">컨트롤러</span><span class="sxs-lookup"><span data-stu-id="fc308-139">Container</span></span>
- <span data-ttu-id="fc308-140">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="fc308-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc308-141">-서비스</span><span class="sxs-lookup"><span data-stu-id="fc308-141">-Service</span></span>
<span data-ttu-id="fc308-142">서비스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-142">Specifies the service.</span></span>
<span data-ttu-id="fc308-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc308-144">않아야</span><span class="sxs-lookup"><span data-stu-id="fc308-144">None</span></span>
- <span data-ttu-id="fc308-145">블</span><span class="sxs-lookup"><span data-stu-id="fc308-145">Blob</span></span>
- <span data-ttu-id="fc308-146">파일</span><span class="sxs-lookup"><span data-stu-id="fc308-146">File</span></span>
- <span data-ttu-id="fc308-147">전담팀</span><span class="sxs-lookup"><span data-stu-id="fc308-147">Queue</span></span>
- <span data-ttu-id="fc308-148">테이블로</span><span class="sxs-lookup"><span data-stu-id="fc308-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc308-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fc308-149">-StartTime</span></span>
<span data-ttu-id="fc308-150">SA가 유효 하 게 되는 **DateTime** 개체로 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="fc308-151">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="fc308-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc308-152">CommonParameters</span></span>
<span data-ttu-id="fc308-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc308-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc308-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc308-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc308-155">입력</span><span class="sxs-lookup"><span data-stu-id="fc308-155">INPUTS</span></span>

### <span data-ttu-id="fc308-156">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc308-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fc308-157">출력</span><span class="sxs-lookup"><span data-stu-id="fc308-157">OUTPUTS</span></span>

### <span data-ttu-id="fc308-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc308-158">System.String</span></span>

## <span data-ttu-id="fc308-159">상속자</span><span class="sxs-lookup"><span data-stu-id="fc308-159">NOTES</span></span>

## <span data-ttu-id="fc308-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc308-160">RELATED LINKS</span></span>

[<span data-ttu-id="fc308-161">새로운 AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="fc308-162">새로운 AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="fc308-163">새로운 AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="fc308-164">새로운 AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="fc308-165">새로운 AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="fc308-166">새로운 AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="fc308-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)

