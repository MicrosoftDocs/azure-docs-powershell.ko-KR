---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056806"
---
# <span data-ttu-id="e3996-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="e3996-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3996-102">SYNOPSIS</span></span>
<span data-ttu-id="e3996-103">Runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-103">Gets a runbook.</span></span>

## <span data-ttu-id="e3996-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3996-104">SYNTAX</span></span>

### <span data-ttu-id="e3996-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3996-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3996-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="e3996-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3996-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e3996-107">DESCRIPTION</span></span>
<span data-ttu-id="e3996-108">**AzAutomationRunbook** Cmdlet은 Azure Automation runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="e3996-109">특정 runbook을 가져오려면 해당 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="e3996-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3996-110">EXAMPLES</span></span>

### <span data-ttu-id="e3996-111">예제 1: 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="e3996-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e3996-112">이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e3996-113">변수</span><span class="sxs-lookup"><span data-stu-id="e3996-113">PARAMETERS</span></span>

### <span data-ttu-id="e3996-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3996-114">-AutomationAccountName</span></span>
<span data-ttu-id="e3996-115">이 cmdlet이 runbook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3996-116">-DefaultProfile</span></span>
<span data-ttu-id="e3996-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e3996-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3996-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e3996-118">-Name</span></span>
<span data-ttu-id="e3996-119">이 cmdlet이 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3996-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3996-121">이 cmdlet이 runbook을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3996-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3996-122">CommonParameters</span></span>
<span data-ttu-id="e3996-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3996-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3996-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3996-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3996-125">입력</span><span class="sxs-lookup"><span data-stu-id="e3996-125">INPUTS</span></span>

### <span data-ttu-id="e3996-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3996-126">System.String</span></span>

## <span data-ttu-id="e3996-127">출력</span><span class="sxs-lookup"><span data-stu-id="e3996-127">OUTPUTS</span></span>

### <span data-ttu-id="e3996-128">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="e3996-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e3996-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e3996-129">NOTES</span></span>

## <span data-ttu-id="e3996-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3996-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3996-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-132">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-133">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-134">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-135">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-136">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e3996-138">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e3996-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

