---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041660"
---
# <span data-ttu-id="e2f35-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="e2f35-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="e2f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f35-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f35-103">새 지원 티켓 통신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="e2f35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2f35-104">SYNTAX</span></span>

### <span data-ttu-id="e2f35-105">CreateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2f35-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f35-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2f35-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2f35-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2f35-107">DESCRIPTION</span></span>
<span data-ttu-id="e2f35-108">Azure 지원 티켓에 새 고객 통신을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="e2f35-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e2f35-109">EXAMPLES</span></span>

### <span data-ttu-id="e2f35-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2f35-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="e2f35-111">변수</span><span class="sxs-lookup"><span data-stu-id="e2f35-111">PARAMETERS</span></span>

### <span data-ttu-id="e2f35-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2f35-112">-AsJob</span></span>
<span data-ttu-id="e2f35-113">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e2f35-114">-본문</span><span class="sxs-lookup"><span data-stu-id="e2f35-114">-Body</span></span>
<span data-ttu-id="e2f35-115">통신의 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-115">Body of the communication.</span></span>

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

### <span data-ttu-id="e2f35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f35-116">-DefaultProfile</span></span>
<span data-ttu-id="e2f35-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f35-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e2f35-118">-Name</span></span>
<span data-ttu-id="e2f35-119">통신 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="e2f35-120">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="e2f35-120">-Sender</span></span>
<span data-ttu-id="e2f35-121">보낸 사람의 전자 메일 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="e2f35-122">-주제</span><span class="sxs-lookup"><span data-stu-id="e2f35-122">-Subject</span></span>
<span data-ttu-id="e2f35-123">통신의 주제.</span><span class="sxs-lookup"><span data-stu-id="e2f35-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="e2f35-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="e2f35-124">-SupportTicketName</span></span>
<span data-ttu-id="e2f35-125">티켓 이름을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f35-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="e2f35-126">-SupportTicketObject</span></span>
<span data-ttu-id="e2f35-127">티켓 개체를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f35-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e2f35-128">-Confirm</span></span>
<span data-ttu-id="e2f35-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f35-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f35-130">-WhatIf</span></span>
<span data-ttu-id="e2f35-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f35-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f35-133">CommonParameters</span></span>
<span data-ttu-id="e2f35-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f35-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2f35-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f35-136">입력</span><span class="sxs-lookup"><span data-stu-id="e2f35-136">INPUTS</span></span>

### <span data-ttu-id="e2f35-137">Microsoft. PSSupportTicket을 통해 지원 되는 모델</span><span class="sxs-lookup"><span data-stu-id="e2f35-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="e2f35-138">출력</span><span class="sxs-lookup"><span data-stu-id="e2f35-138">OUTPUTS</span></span>

### <span data-ttu-id="e2f35-139">PSSupportTicketCommunication를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f35-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="e2f35-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e2f35-140">NOTES</span></span>

## <span data-ttu-id="e2f35-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2f35-141">RELATED LINKS</span></span>