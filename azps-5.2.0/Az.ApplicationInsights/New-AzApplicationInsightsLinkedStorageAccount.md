---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353498"
---
# <span data-ttu-id="d9c38-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9c38-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d9c38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9c38-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c38-103">Application Insights 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="d9c38-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="d9c38-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9c38-104">SYNTAX</span></span>

### <span data-ttu-id="d9c38-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d9c38-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c38-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9c38-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c38-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9c38-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9c38-108">설명</span><span class="sxs-lookup"><span data-stu-id="d9c38-108">DESCRIPTION</span></span>
<span data-ttu-id="d9c38-109">Application Insights 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="d9c38-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="d9c38-110">예제</span><span class="sxs-lookup"><span data-stu-id="d9c38-110">EXAMPLES</span></span>

### <span data-ttu-id="d9c38-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d9c38-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="d9c38-112">구성 요소 "componentName$account 아래에서 연결된 저장소 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="d9c38-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="d9c38-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9c38-113">PARAMETERS</span></span>

### <span data-ttu-id="d9c38-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d9c38-114">-ComponentName</span></span>
<span data-ttu-id="d9c38-115">구성 요소 이름</span><span class="sxs-lookup"><span data-stu-id="d9c38-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9c38-116">-DefaultProfile</span></span>
<span data-ttu-id="d9c38-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9c38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9c38-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9c38-118">-InputObject</span></span>
<span data-ttu-id="d9c38-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d9c38-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c38-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c38-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="d9c38-121">Storage 계정 ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c38-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="d9c38-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9c38-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9c38-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d9c38-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c38-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c38-124">-ResourceId</span></span>
<span data-ttu-id="d9c38-125">구성 요소 ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9c38-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c38-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9c38-126">-Confirm</span></span>
<span data-ttu-id="d9c38-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9c38-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9c38-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9c38-128">-WhatIf</span></span>
<span data-ttu-id="d9c38-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9c38-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9c38-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9c38-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9c38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c38-131">CommonParameters</span></span>
<span data-ttu-id="d9c38-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9c38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c38-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9c38-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c38-134">입력</span><span class="sxs-lookup"><span data-stu-id="d9c38-134">INPUTS</span></span>

### <span data-ttu-id="d9c38-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d9c38-135">System.String</span></span>

### <span data-ttu-id="d9c38-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d9c38-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="d9c38-137">출력</span><span class="sxs-lookup"><span data-stu-id="d9c38-137">OUTPUTS</span></span>

### <span data-ttu-id="d9c38-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d9c38-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="d9c38-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9c38-139">NOTES</span></span>

## <span data-ttu-id="d9c38-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9c38-140">RELATED LINKS</span></span>