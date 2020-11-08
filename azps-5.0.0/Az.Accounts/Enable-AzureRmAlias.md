---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218264"
---
# <span data-ttu-id="2d9b8-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2d9b8-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="2d9b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9b8-103">Az 모듈에 대 한 AzureRm 접두사 별칭을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="2d9b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d9b8-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d9b8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d9b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9b8-106">Az 모듈에 대 한 AzureRm 접두사 별칭을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="2d9b8-107">-Module을 지정 하면 나열 된 모듈만 별칭을 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="2d9b8-108">그렇지 않으면 모든 AzureRm 별칭을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="2d9b8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2d9b8-109">EXAMPLES</span></span>

### <span data-ttu-id="2d9b8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d9b8-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="2d9b8-111">현재 PowerShell 세션에 대해 모든 AzureRm 접두사를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="2d9b8-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2d9b8-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="2d9b8-113">현재 프로세스와 현재 사용자 둘 다에 대 한 Az 모듈에 대해 AzureRm 별칭을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="2d9b8-114">변수</span><span class="sxs-lookup"><span data-stu-id="2d9b8-114">PARAMETERS</span></span>

### <span data-ttu-id="2d9b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9b8-115">-DefaultProfile</span></span>
<span data-ttu-id="2d9b8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d9b8-117">-모듈</span><span class="sxs-lookup"><span data-stu-id="2d9b8-117">-Module</span></span>
<span data-ttu-id="2d9b8-118">별칭을 사용할 모듈을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="2d9b8-119">아무것도 지정 하지 않으면 모든 모듈이 기본적으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="2d9b8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d9b8-120">-PassThru</span></span>
<span data-ttu-id="2d9b8-121">지정 하는 경우 cmdlet은 모든 별칭을 반환 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="2d9b8-122">-범위</span><span class="sxs-lookup"><span data-stu-id="2d9b8-122">-Scope</span></span>
<span data-ttu-id="2d9b8-123">사용할 수 있는 범위 별칭을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="2d9b8-124">기본값은 ' Local '입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9b8-125">-확인</span><span class="sxs-lookup"><span data-stu-id="2d9b8-125">-Confirm</span></span>
<span data-ttu-id="2d9b8-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d9b8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d9b8-127">-WhatIf</span></span>
<span data-ttu-id="2d9b8-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d9b8-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d9b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9b8-130">CommonParameters</span></span>
<span data-ttu-id="2d9b8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9b8-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9b8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9b8-133">입력</span><span class="sxs-lookup"><span data-stu-id="2d9b8-133">INPUTS</span></span>

### <span data-ttu-id="2d9b8-134">않아야</span><span class="sxs-lookup"><span data-stu-id="2d9b8-134">None</span></span>

## <span data-ttu-id="2d9b8-135">출력</span><span class="sxs-lookup"><span data-stu-id="2d9b8-135">OUTPUTS</span></span>

### <span data-ttu-id="2d9b8-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d9b8-136">System.String</span></span>

## <span data-ttu-id="2d9b8-137">상속자</span><span class="sxs-lookup"><span data-stu-id="2d9b8-137">NOTES</span></span>

## <span data-ttu-id="2d9b8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d9b8-138">RELATED LINKS</span></span>