---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204342"
---
# <span data-ttu-id="ffa04-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="ffa04-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="ffa04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa04-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa04-103">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="ffa04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffa04-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa04-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffa04-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa04-106">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="ffa04-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ffa04-107">EXAMPLES</span></span>

### <span data-ttu-id="ffa04-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffa04-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="ffa04-109">구독에 대 한 보안 연락처를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="ffa04-110">변수</span><span class="sxs-lookup"><span data-stu-id="ffa04-110">PARAMETERS</span></span>

### <span data-ttu-id="ffa04-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="ffa04-111">-AlertAdmin</span></span>
<span data-ttu-id="ffa04-112">관리자에 게 알림이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="ffa04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa04-113">-DefaultProfile</span></span>
<span data-ttu-id="ffa04-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa04-115">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="ffa04-115">-Email</span></span>
<span data-ttu-id="ffa04-116">이메일.</span><span class="sxs-lookup"><span data-stu-id="ffa04-116">E-Mail.</span></span>

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

### <span data-ttu-id="ffa04-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ffa04-117">-Name</span></span>
<span data-ttu-id="ffa04-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-118">Resource name.</span></span>

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

### <span data-ttu-id="ffa04-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="ffa04-119">-NotifyOnAlert</span></span>
<span data-ttu-id="ffa04-120">알림을 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="ffa04-121">-전화</span><span class="sxs-lookup"><span data-stu-id="ffa04-121">-Phone</span></span>
<span data-ttu-id="ffa04-122">전화.</span><span class="sxs-lookup"><span data-stu-id="ffa04-122">Phone.</span></span>

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

### <span data-ttu-id="ffa04-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ffa04-123">-Confirm</span></span>
<span data-ttu-id="ffa04-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa04-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa04-125">-WhatIf</span></span>
<span data-ttu-id="ffa04-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffa04-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa04-128">CommonParameters</span></span>
<span data-ttu-id="ffa04-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffa04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa04-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ffa04-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa04-131">입력</span><span class="sxs-lookup"><span data-stu-id="ffa04-131">INPUTS</span></span>

### <span data-ttu-id="ffa04-132">않아야</span><span class="sxs-lookup"><span data-stu-id="ffa04-132">None</span></span>

## <span data-ttu-id="ffa04-133">출력</span><span class="sxs-lookup"><span data-stu-id="ffa04-133">OUTPUTS</span></span>

### <span data-ttu-id="ffa04-134">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="ffa04-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="ffa04-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ffa04-135">NOTES</span></span>

## <span data-ttu-id="ffa04-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffa04-136">RELATED LINKS</span></span>