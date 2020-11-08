---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211685"
---
# <span data-ttu-id="a40aa-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a40aa-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="a40aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a40aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a40aa-103">논리 앱의 실행 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="a40aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a40aa-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a40aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a40aa-105">DESCRIPTION</span></span>
<span data-ttu-id="a40aa-106">**AzLogicAppRunHistory** cmdlet은 로직 앱의 실행 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="a40aa-107">이 cmdlet은 **Workflowrun** 개체의 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="a40aa-108">논리 앱 및 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="a40aa-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a40aa-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a40aa-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a40aa-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a40aa-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a40aa-113">EXAMPLES</span></span>

### <span data-ttu-id="a40aa-114">예제 1: 논리 앱의 실행 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="a40aa-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="a40aa-115">이 명령은 LogicApp03 이라는 논리 앱의 실행 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="a40aa-116">예제 2: 논리 앱 실행 가져오기</span><span class="sxs-lookup"><span data-stu-id="a40aa-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="a40aa-117">이 명령은 LogicApp03 이라는 논리 앱에 대해 실행 되는 특정 논리 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="a40aa-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="a40aa-118">Example 3</span></span>

<span data-ttu-id="a40aa-119">이 명령은 LogicApp03 이라는 논리 앱의 실행 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="a40aa-120">생성</span><span class="sxs-lookup"><span data-stu-id="a40aa-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="a40aa-121">변수</span><span class="sxs-lookup"><span data-stu-id="a40aa-121">PARAMETERS</span></span>

### <span data-ttu-id="a40aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40aa-122">-DefaultProfile</span></span>
<span data-ttu-id="a40aa-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a40aa-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a40aa-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a40aa-124">-Name</span></span>
<span data-ttu-id="a40aa-125">이 cmdlet이 실행 기록을 가져오는 논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="a40aa-127">논리 앱을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="a40aa-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="a40aa-128">-RunName</span></span>
<span data-ttu-id="a40aa-129">논리 앱의 실행 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="a40aa-130">이 cmdlet은이 cmdlet에서 지정 하는 워크플로 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40aa-131">CommonParameters</span></span>
<span data-ttu-id="a40aa-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a40aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40aa-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40aa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40aa-134">입력</span><span class="sxs-lookup"><span data-stu-id="a40aa-134">INPUTS</span></span>

### <span data-ttu-id="a40aa-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a40aa-135">System.String</span></span>

## <span data-ttu-id="a40aa-136">출력</span><span class="sxs-lookup"><span data-stu-id="a40aa-136">OUTPUTS</span></span>

### <span data-ttu-id="a40aa-137">Microsoft. Azure. i a m. 모델. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="a40aa-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="a40aa-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a40aa-138">NOTES</span></span>

## <span data-ttu-id="a40aa-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a40aa-139">RELATED LINKS</span></span>

[<span data-ttu-id="a40aa-140">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="a40aa-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="a40aa-141">시작-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="a40aa-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="a40aa-142">중지-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a40aa-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)

