---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524120"
---
# <span data-ttu-id="3d638-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d638-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3d638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d638-102">SYNOPSIS</span></span>
<span data-ttu-id="3d638-103">Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="3d638-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d638-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d638-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d638-105">DESCRIPTION</span></span>
<span data-ttu-id="3d638-106">**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="3d638-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3d638-107">EXAMPLES</span></span>

### <span data-ttu-id="3d638-108">예제 1: 모든 권한이 있는 테이블에서 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="3d638-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="3d638-109">이 명령은 MyTable 이라는 저장소 테이블에 대 한 Policy08 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="3d638-110">변수</span><span class="sxs-lookup"><span data-stu-id="3d638-110">PARAMETERS</span></span>

### <span data-ttu-id="3d638-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3d638-111">-Context</span></span>
<span data-ttu-id="3d638-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3d638-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3d638-114">-ExpiryTime</span></span>
<span data-ttu-id="3d638-115">저장 된 액세스 정책이 만료 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3d638-116">-NoExpiryTime</span></span>
<span data-ttu-id="3d638-117">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="3d638-118">-NoStartTime</span></span>
<span data-ttu-id="3d638-119">시작 시간이 $Null 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-119">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-120">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="3d638-120">-Permission</span></span>
<span data-ttu-id="3d638-121">이 저장소 테이블에 대 한 공용 액세스 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-121">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-122">-정책</span><span class="sxs-lookup"><span data-stu-id="3d638-122">-Policy</span></span>
<span data-ttu-id="3d638-123">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3d638-124">-StartTime</span></span>
<span data-ttu-id="3d638-125">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-126">-테이블</span><span class="sxs-lookup"><span data-stu-id="3d638-126">-Table</span></span>
<span data-ttu-id="3d638-127">Azure 저장소 테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d638-128">-확인</span><span class="sxs-lookup"><span data-stu-id="3d638-128">-Confirm</span></span>
<span data-ttu-id="3d638-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d638-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d638-130">-WhatIf</span></span>
<span data-ttu-id="3d638-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d638-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d638-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d638-133">CommonParameters</span></span>
<span data-ttu-id="3d638-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d638-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d638-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d638-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d638-136">입력</span><span class="sxs-lookup"><span data-stu-id="3d638-136">INPUTS</span></span>

## <span data-ttu-id="3d638-137">출력</span><span class="sxs-lookup"><span data-stu-id="3d638-137">OUTPUTS</span></span>

## <span data-ttu-id="3d638-138">상속자</span><span class="sxs-lookup"><span data-stu-id="3d638-138">NOTES</span></span>

## <span data-ttu-id="3d638-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d638-139">RELATED LINKS</span></span>

[<span data-ttu-id="3d638-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d638-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3d638-141">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d638-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3d638-142">새로운 AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d638-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3d638-143">제거-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d638-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)