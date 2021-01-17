---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356763"
---
# <span data-ttu-id="52a51-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="52a51-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="52a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a51-102">SYNOPSIS</span></span>
<span data-ttu-id="52a51-103">마이그레이션 프로젝트에 도구를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="52a51-104">구문</span><span class="sxs-lookup"><span data-stu-id="52a51-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52a51-105">설명</span><span class="sxs-lookup"><span data-stu-id="52a51-105">DESCRIPTION</span></span>
<span data-ttu-id="52a51-106">마이그레이션 프로젝트에 도구를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="52a51-107">예제</span><span class="sxs-lookup"><span data-stu-id="52a51-107">EXAMPLES</span></span>

### <span data-ttu-id="52a51-108">예제 1: REgister 도구.</span><span class="sxs-lookup"><span data-stu-id="52a51-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="52a51-109">마이그레이션 프로젝트에 도구를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="52a51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52a51-110">PARAMETERS</span></span>

### <span data-ttu-id="52a51-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="52a51-111">-AcceptLanguage</span></span>
<span data-ttu-id="52a51-112">표준 요청 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-112">Standard request header.</span></span>
<span data-ttu-id="52a51-113">서비스에서 적절한 언어로 클라이언트에 응답하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="52a51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a51-114">-DefaultProfile</span></span>
<span data-ttu-id="52a51-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a51-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="52a51-116">-MigrateProjectName</span></span>
<span data-ttu-id="52a51-117">Azure Migrate 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="52a51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a51-118">-ResourceGroupName</span></span>
<span data-ttu-id="52a51-119">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름은 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="52a51-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52a51-120">-SubscriptionId</span></span>
<span data-ttu-id="52a51-121">마이그레이션 프로젝트를 만든 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a51-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="52a51-122">-Tool</span></span>
<span data-ttu-id="52a51-123">등록할 도구를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="52a51-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52a51-124">-Confirm</span></span>
<span data-ttu-id="52a51-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a51-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a51-126">-WhatIf</span></span>
<span data-ttu-id="52a51-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="52a51-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a51-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a51-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a51-129">CommonParameters</span></span>
<span data-ttu-id="52a51-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52a51-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a51-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52a51-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a51-132">입력</span><span class="sxs-lookup"><span data-stu-id="52a51-132">INPUTS</span></span>

## <span data-ttu-id="52a51-133">출력</span><span class="sxs-lookup"><span data-stu-id="52a51-133">OUTPUTS</span></span>

### <span data-ttu-id="52a51-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52a51-134">System.Boolean</span></span>

## <span data-ttu-id="52a51-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52a51-135">NOTES</span></span>

<span data-ttu-id="52a51-136">별칭</span><span class="sxs-lookup"><span data-stu-id="52a51-136">ALIASES</span></span>

## <span data-ttu-id="52a51-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52a51-137">RELATED LINKS</span></span>
