---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/register-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Register-AzWvdApplicationGroup.md
ms.openlocfilehash: 874cc587bff418bf0d6846fe39bdf7d10c42d7dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215011"
---
# <span data-ttu-id="b9458-101">Register-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="b9458-101">Register-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="b9458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9458-102">SYNOPSIS</span></span>
<span data-ttu-id="b9458-103">Windows 가상 데스크톱 응용 프로그램 그룹을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-103">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="b9458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9458-104">SYNTAX</span></span>

```
Register-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b9458-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9458-105">DESCRIPTION</span></span>
<span data-ttu-id="b9458-106">Windows 가상 데스크톱 응용 프로그램 그룹을 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-106">Register a Windows virtual desktop application group.</span></span>

## <span data-ttu-id="b9458-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b9458-107">EXAMPLES</span></span>

### <span data-ttu-id="b9458-108">예제 1: Windows 가상 데스크톱 응용 프로그램 그룹 등록</span><span class="sxs-lookup"><span data-stu-id="b9458-108">Example 1: Register a Windows Virtual Desktop Application Group</span></span>
```powershell
PS C:\> Register-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="b9458-109">이 명령은 Windows 가상 데스크톱 응용 프로그램 그룹을 작업 영역에 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-109">This command registers a Windows Virtual Desktop Application Group to a Workspace.</span></span>

## <span data-ttu-id="b9458-110">변수</span><span class="sxs-lookup"><span data-stu-id="b9458-110">PARAMETERS</span></span>

### <span data-ttu-id="b9458-111">-ApplicationGroupPath</span><span class="sxs-lookup"><span data-stu-id="b9458-111">-ApplicationGroupPath</span></span>
<span data-ttu-id="b9458-112">ApplicationGroupPath 경로</span><span class="sxs-lookup"><span data-stu-id="b9458-112">ApplicationGroupPath Path</span></span>

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

### <span data-ttu-id="b9458-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9458-113">-DefaultProfile</span></span>
<span data-ttu-id="b9458-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9458-115">-ResourceGroupName</span></span>
<span data-ttu-id="b9458-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b9458-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b9458-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9458-117">-SubscriptionId</span></span>
<span data-ttu-id="b9458-118">구독 Id</span><span class="sxs-lookup"><span data-stu-id="b9458-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9458-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9458-119">-WorkspaceName</span></span>
<span data-ttu-id="b9458-120">작업 영역 이름</span><span class="sxs-lookup"><span data-stu-id="b9458-120">Workspace Name</span></span>

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

### <span data-ttu-id="b9458-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b9458-121">-Confirm</span></span>
<span data-ttu-id="b9458-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9458-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9458-123">-WhatIf</span></span>
<span data-ttu-id="b9458-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9458-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9458-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9458-126">CommonParameters</span></span>
<span data-ttu-id="b9458-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9458-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9458-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9458-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9458-129">입력</span><span class="sxs-lookup"><span data-stu-id="b9458-129">INPUTS</span></span>

## <span data-ttu-id="b9458-130">출력</span><span class="sxs-lookup"><span data-stu-id="b9458-130">OUTPUTS</span></span>

### <span data-ttu-id="b9458-131">Api20191210Preview. i i m. .exe 작업 영역</span><span class="sxs-lookup"><span data-stu-id="b9458-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="b9458-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b9458-132">NOTES</span></span>

<span data-ttu-id="b9458-133">별칭과</span><span class="sxs-lookup"><span data-stu-id="b9458-133">ALIASES</span></span>

## <span data-ttu-id="b9458-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9458-134">RELATED LINKS</span></span>
