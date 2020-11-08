---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203840"
---
# <span data-ttu-id="34068-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="34068-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="34068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34068-102">SYNOPSIS</span></span>
<span data-ttu-id="34068-103">작업 영역에 대 한 서비스 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="34068-103">Unlink service for workspace</span></span>

## <span data-ttu-id="34068-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34068-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34068-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34068-105">DESCRIPTION</span></span>
<span data-ttu-id="34068-106">작업 영역에 대 한 서비스 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="34068-106">Unlink service for workspace</span></span>

## <span data-ttu-id="34068-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34068-107">EXAMPLES</span></span>

### <span data-ttu-id="34068-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="34068-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="34068-109">작업 영역에 대 한 연결 된 서비스 연결 해제</span><span class="sxs-lookup"><span data-stu-id="34068-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="34068-110">변수</span><span class="sxs-lookup"><span data-stu-id="34068-110">PARAMETERS</span></span>

### <span data-ttu-id="34068-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34068-111">-AsJob</span></span>
<span data-ttu-id="34068-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="34068-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34068-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34068-113">-DefaultProfile</span></span>
<span data-ttu-id="34068-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34068-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34068-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="34068-115">-LinkedServiceName</span></span>
<span data-ttu-id="34068-116">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34068-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34068-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34068-117">-ResourceGroupName</span></span>
<span data-ttu-id="34068-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34068-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34068-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="34068-119">-WorkspaceName</span></span>
<span data-ttu-id="34068-120">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34068-120">The Workspace name.</span></span>

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

### <span data-ttu-id="34068-121">-확인</span><span class="sxs-lookup"><span data-stu-id="34068-121">-Confirm</span></span>
<span data-ttu-id="34068-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34068-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34068-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34068-123">-WhatIf</span></span>
<span data-ttu-id="34068-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34068-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34068-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34068-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34068-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34068-126">CommonParameters</span></span>
<span data-ttu-id="34068-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34068-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34068-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34068-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34068-129">입력</span><span class="sxs-lookup"><span data-stu-id="34068-129">INPUTS</span></span>

### <span data-ttu-id="34068-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34068-130">System.String</span></span>

## <span data-ttu-id="34068-131">출력</span><span class="sxs-lookup"><span data-stu-id="34068-131">OUTPUTS</span></span>

### <span data-ttu-id="34068-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="34068-132">System.Boolean</span></span>

## <span data-ttu-id="34068-133">상속자</span><span class="sxs-lookup"><span data-stu-id="34068-133">NOTES</span></span>

## <span data-ttu-id="34068-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34068-134">RELATED LINKS</span></span>