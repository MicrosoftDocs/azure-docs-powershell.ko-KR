---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1202ecbdaaf07b9ba5704a01449784172204bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527127"
---
# <span data-ttu-id="c9f87-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="c9f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9f87-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f87-103">Runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9f87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9f87-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9f87-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9f87-105">DESCRIPTION</span></span>
<span data-ttu-id="c9f87-106">**AzureRmAutomationRunbook** Cmdlet은 Azure Automation의 프로덕션 환경에서 사용할 runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="c9f87-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9f87-107">EXAMPLES</span></span>

### <span data-ttu-id="c9f87-108">예제 1: runbook 게시</span><span class="sxs-lookup"><span data-stu-id="c9f87-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c9f87-109">이 명령은 Contoso17 이라는 Azure Automation 계정에 Runbk01 라는 runbook을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c9f87-110">변수</span><span class="sxs-lookup"><span data-stu-id="c9f87-110">PARAMETERS</span></span>

### <span data-ttu-id="c9f87-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c9f87-111">-AutomationAccountName</span></span>
<span data-ttu-id="c9f87-112">이 cmdlet이 runbook을 게시 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f87-113">-DefaultProfile</span></span>
<span data-ttu-id="c9f87-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c9f87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f87-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c9f87-115">-Name</span></span>
<span data-ttu-id="c9f87-116">이 cmdlet이 게시 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f87-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9f87-118">이 cmdlet이 runbook을 게시할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f87-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f87-119">CommonParameters</span></span>
<span data-ttu-id="c9f87-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f87-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f87-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f87-122">입력</span><span class="sxs-lookup"><span data-stu-id="c9f87-122">INPUTS</span></span>

### <span data-ttu-id="c9f87-123">않아야</span><span class="sxs-lookup"><span data-stu-id="c9f87-123">None</span></span>
<span data-ttu-id="c9f87-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9f87-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9f87-125">출력</span><span class="sxs-lookup"><span data-stu-id="c9f87-125">OUTPUTS</span></span>

### <span data-ttu-id="c9f87-126">Microsoft. Azure. i a m. Runbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-126">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="c9f87-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c9f87-127">NOTES</span></span>

## <span data-ttu-id="c9f87-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9f87-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9f87-129">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-129">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-130">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-130">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-131">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-132">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-133">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-134">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-134">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-135">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-135">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c9f87-136">시작-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c9f87-136">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

