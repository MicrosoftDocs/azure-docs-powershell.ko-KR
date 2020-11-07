---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: de2bb7d4dab052c0dff53a8f259ade3ba4da29ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867717"
---
# <span data-ttu-id="0edf1-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0edf1-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="0edf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0edf1-102">SYNOPSIS</span></span>
<span data-ttu-id="0edf1-103">논리 앱 트리거 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="0edf1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0edf1-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0edf1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0edf1-105">DESCRIPTION</span></span>
<span data-ttu-id="0edf1-106">**Get-AzLogicAppTriggerCallbackUrl** cmdlet은 리소스 그룹에서 논리 앱 트리거 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="0edf1-107">이 cmdlet은 콜백 URL을 나타내는 **Workflowtriggercallbackurl** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="0edf1-108">리소스 그룹 이름, 논리 앱 이름 및 트리거 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="0edf1-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0edf1-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0edf1-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0edf1-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0edf1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0edf1-113">EXAMPLES</span></span>

### <span data-ttu-id="0edf1-114">예제 1: 논리 앱 트리거 콜백 URL 가져오기</span><span class="sxs-lookup"><span data-stu-id="0edf1-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="0edf1-115">이 명령은 논리 앱 트리거 콜백 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="0edf1-116">변수</span><span class="sxs-lookup"><span data-stu-id="0edf1-116">PARAMETERS</span></span>

### <span data-ttu-id="0edf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0edf1-117">-DefaultProfile</span></span>
<span data-ttu-id="0edf1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0edf1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0edf1-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0edf1-119">-Name</span></span>
<span data-ttu-id="0edf1-120">논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0edf1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0edf1-121">-ResourceGroupName</span></span>
<span data-ttu-id="0edf1-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0edf1-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0edf1-123">-TriggerName</span></span>
<span data-ttu-id="0edf1-124">트리거의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-124">Specifies the name of a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0edf1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0edf1-125">CommonParameters</span></span>
<span data-ttu-id="0edf1-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0edf1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0edf1-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0edf1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0edf1-128">입력</span><span class="sxs-lookup"><span data-stu-id="0edf1-128">INPUTS</span></span>

### <span data-ttu-id="0edf1-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0edf1-129">System.String</span></span>

## <span data-ttu-id="0edf1-130">출력</span><span class="sxs-lookup"><span data-stu-id="0edf1-130">OUTPUTS</span></span>

### <span data-ttu-id="0edf1-131">Microsoft. Azure. 관리. i m l. 모델. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0edf1-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="0edf1-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0edf1-132">NOTES</span></span>

## <span data-ttu-id="0edf1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0edf1-133">RELATED LINKS</span></span>

[<span data-ttu-id="0edf1-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="0edf1-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

