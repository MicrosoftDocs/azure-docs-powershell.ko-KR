---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215165"
---
# <span data-ttu-id="e50b5-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="e50b5-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="e50b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e50b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e50b5-103">지원 연락처 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="e50b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e50b5-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50b5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e50b5-105">DESCRIPTION</span></span>
<span data-ttu-id="e50b5-106">지원 티켓을 만들거나 업데이트할 때 지원 연락처 프로필 개체를 만드는 데 사용할 수 있는 도우미 cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="e50b5-107">지원 티켓을 만드는 데 필수적인 다음 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="e50b5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e50b5-108">EXAMPLES</span></span>

### <span data-ttu-id="e50b5-109">예제 1: 연락처 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="e50b5-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="e50b5-110">변수</span><span class="sxs-lookup"><span data-stu-id="e50b5-110">PARAMETERS</span></span>

### <span data-ttu-id="e50b5-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e50b5-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="e50b5-112">여기에 나열 된 전자 메일 주소는 지원 티켓에 대 한 모든 서신에 복사 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50b5-113">-국가</span><span class="sxs-lookup"><span data-stu-id="e50b5-113">-Country</span></span>
<span data-ttu-id="e50b5-114">고객 국가.</span><span class="sxs-lookup"><span data-stu-id="e50b5-114">Customer country.</span></span>
<span data-ttu-id="e50b5-115">유효한 ISO Alpha-3 국가 코드 (ISO 3166) 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="e50b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50b5-116">-DefaultProfile</span></span>
<span data-ttu-id="e50b5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e50b5-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e50b5-118">-FirstName</span></span>
<span data-ttu-id="e50b5-119">고객 성.</span><span class="sxs-lookup"><span data-stu-id="e50b5-119">Customer first name.</span></span>

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

### <span data-ttu-id="e50b5-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="e50b5-120">-LastName</span></span>
<span data-ttu-id="e50b5-121">고객 성.</span><span class="sxs-lookup"><span data-stu-id="e50b5-121">Customer last name.</span></span>

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

### <span data-ttu-id="e50b5-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e50b5-122">-PhoneNumber</span></span>
<span data-ttu-id="e50b5-123">고객 전화 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-123">Customer phone number.</span></span>
<span data-ttu-id="e50b5-124">이는 기본 연락 방법이 휴대폰 인 경우 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="e50b5-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="e50b5-125">-PreferredContactMethod</span></span>
<span data-ttu-id="e50b5-126">선호 연락 방법.</span><span class="sxs-lookup"><span data-stu-id="e50b5-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50b5-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="e50b5-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="e50b5-128">고객 선호 지원 언어.</span><span class="sxs-lookup"><span data-stu-id="e50b5-128">Customer preferred support language.</span></span>
<span data-ttu-id="e50b5-129">여기에 나열 된 지원 언어 중 하나에 대 한 올바른 언어 contry 코드 여야 합니다 https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="e50b5-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="e50b5-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="e50b5-130">-PreferredTimeZone</span></span>
<span data-ttu-id="e50b5-131">고객 기본 설정 표준 시간대</span><span class="sxs-lookup"><span data-stu-id="e50b5-131">Customer preferred time zone.</span></span>
<span data-ttu-id="e50b5-132">유효한 System.TimeZoneInfo.Id 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="e50b5-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e50b5-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="e50b5-134">고객 기본 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="e50b5-135">-확인</span><span class="sxs-lookup"><span data-stu-id="e50b5-135">-Confirm</span></span>
<span data-ttu-id="e50b5-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e50b5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50b5-137">-WhatIf</span></span>
<span data-ttu-id="e50b5-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e50b5-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e50b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50b5-140">CommonParameters</span></span>
<span data-ttu-id="e50b5-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50b5-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e50b5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50b5-143">입력</span><span class="sxs-lookup"><span data-stu-id="e50b5-143">INPUTS</span></span>

### <span data-ttu-id="e50b5-144">않아야</span><span class="sxs-lookup"><span data-stu-id="e50b5-144">None</span></span>

## <span data-ttu-id="e50b5-145">출력</span><span class="sxs-lookup"><span data-stu-id="e50b5-145">OUTPUTS</span></span>

### <span data-ttu-id="e50b5-146">Microsoft. Azure. Ps연락처 프로필</span><span class="sxs-lookup"><span data-stu-id="e50b5-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="e50b5-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e50b5-147">NOTES</span></span>

## <span data-ttu-id="e50b5-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e50b5-148">RELATED LINKS</span></span>