---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 485f244caa78bffda71d6129990c76daa8b173c4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875743"
---
# <span data-ttu-id="ebc1c-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ebc1c-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="ebc1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc1c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc1c-103">Azns 작업 그룹 유형의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="ebc1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebc1c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebc1c-105">DESCRIPTION</span></span>
<span data-ttu-id="ebc1c-106">Azns Action Group 유형의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="ebc1c-107">이 개체는 로그 경고 규칙을 만드는 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="ebc1c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ebc1c-108">EXAMPLES</span></span>

### <span data-ttu-id="ebc1c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ebc1c-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="ebc1c-110">변수</span><span class="sxs-lookup"><span data-stu-id="ebc1c-110">PARAMETERS</span></span>

### <span data-ttu-id="ebc1c-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="ebc1c-111">-ActionGroup</span></span>
<span data-ttu-id="ebc1c-112">알림을 보낼 작업 그룹 목록</span><span class="sxs-lookup"><span data-stu-id="ebc1c-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="ebc1c-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="ebc1c-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="ebc1c-114">사용자 지정 된 webhook 페이로드</span><span class="sxs-lookup"><span data-stu-id="ebc1c-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="ebc1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc1c-115">-DefaultProfile</span></span>
<span data-ttu-id="ebc1c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc1c-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="ebc1c-117">-EmailSubject</span></span>
<span data-ttu-id="ebc1c-118">알림 메시지의 전자 메일 제목</span><span class="sxs-lookup"><span data-stu-id="ebc1c-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="ebc1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc1c-119">CommonParameters</span></span>
<span data-ttu-id="ebc1c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc1c-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc1c-122">입력</span><span class="sxs-lookup"><span data-stu-id="ebc1c-122">INPUTS</span></span>

### <span data-ttu-id="ebc1c-123">않아야</span><span class="sxs-lookup"><span data-stu-id="ebc1c-123">None</span></span>

## <span data-ttu-id="ebc1c-124">출력</span><span class="sxs-lookup"><span data-stu-id="ebc1c-124">OUTPUTS</span></span>

### <span data-ttu-id="ebc1c-125">PSScheduledQueryRuleAznsAction를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebc1c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="ebc1c-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ebc1c-126">NOTES</span></span>

## <span data-ttu-id="ebc1c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebc1c-127">RELATED LINKS</span></span>