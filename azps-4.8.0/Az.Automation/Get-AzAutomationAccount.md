---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049222"
---
# <span data-ttu-id="7a604-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7a604-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="7a604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a604-102">SYNOPSIS</span></span>
<span data-ttu-id="7a604-103">리소스 그룹의 자동화 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="7a604-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a604-104">SYNTAX</span></span>

### <span data-ttu-id="7a604-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="7a604-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a604-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a604-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a604-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7a604-107">DESCRIPTION</span></span>
<span data-ttu-id="7a604-108">**Get-AzAutomationAccount** cmdlet은 리소스 그룹의 Azure Automation 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="7a604-109">자동화 계정에 대 한 자세한 내용은 New-AzAutomationAccount cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a604-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="7a604-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7a604-110">EXAMPLES</span></span>

### <span data-ttu-id="7a604-111">예제 1: 모든 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="7a604-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="7a604-112">이 명령은 ResourceGroup03 이라는 리소스 그룹의 모든 자동화 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="7a604-113">예제 2: 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="7a604-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="7a604-114">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 ContosoAutomationAccount 라는 Automation 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="7a604-115">변수</span><span class="sxs-lookup"><span data-stu-id="7a604-115">PARAMETERS</span></span>

### <span data-ttu-id="7a604-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a604-116">-DefaultProfile</span></span>
<span data-ttu-id="7a604-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7a604-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a604-118">-이름</span><span class="sxs-lookup"><span data-stu-id="7a604-118">-Name</span></span>
<span data-ttu-id="7a604-119">이 cmdlet이 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a604-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a604-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a604-121">이 cmdlet에서 자동화 계정을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a604-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a604-122">CommonParameters</span></span>
<span data-ttu-id="7a604-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a604-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a604-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a604-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a604-125">입력</span><span class="sxs-lookup"><span data-stu-id="7a604-125">INPUTS</span></span>

### <span data-ttu-id="7a604-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a604-126">System.String</span></span>

## <span data-ttu-id="7a604-127">출력</span><span class="sxs-lookup"><span data-stu-id="7a604-127">OUTPUTS</span></span>

### <span data-ttu-id="7a604-128">Microsoft Azure. \*.</span><span class="sxs-lookup"><span data-stu-id="7a604-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="7a604-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7a604-129">NOTES</span></span>

## <span data-ttu-id="7a604-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a604-130">RELATED LINKS</span></span>

[<span data-ttu-id="7a604-131">새로운 AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7a604-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="7a604-132">제거-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7a604-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="7a604-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="7a604-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)

