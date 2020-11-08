---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048186"
---
# <span data-ttu-id="93886-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="93886-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="93886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93886-102">SYNOPSIS</span></span>
<span data-ttu-id="93886-103">메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93886-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="93886-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93886-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93886-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93886-105">DESCRIPTION</span></span>
<span data-ttu-id="93886-106">**AzActivityLogAlertCondition** cmdlet은 메모리에 새 활동 로그 알림 상태 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93886-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="93886-107">예제의</span><span class="sxs-lookup"><span data-stu-id="93886-107">EXAMPLES</span></span>

### <span data-ttu-id="93886-108">예제 1: 메모리에 새 활동 로그 경고 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93886-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="93886-109">이 명령은 메모리에 새 활동 로그 알림 조건 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93886-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="93886-110">**참고** :이 cmdlet을 Set-AzActivityLogAlert에 사용 하는 경우 매개 변수로 전달 되는 이러한 개체 중 하나 이상에는 해당 필드가 "Category"와 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93886-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="93886-111">그렇지 않으면 백 엔드가 400 (BadRequest)로 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="93886-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="93886-112">변수</span><span class="sxs-lookup"><span data-stu-id="93886-112">PARAMETERS</span></span>

### <span data-ttu-id="93886-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93886-113">-DefaultProfile</span></span>
<span data-ttu-id="93886-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="93886-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93886-115">-같음</span><span class="sxs-lookup"><span data-stu-id="93886-115">-Equal</span></span>
<span data-ttu-id="93886-116">리프 조건에 대 한 equals 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93886-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="93886-117">-필드</span><span class="sxs-lookup"><span data-stu-id="93886-117">-Field</span></span>
<span data-ttu-id="93886-118">조건에 대 한 필드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93886-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="93886-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93886-119">CommonParameters</span></span>
<span data-ttu-id="93886-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93886-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93886-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93886-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93886-122">입력</span><span class="sxs-lookup"><span data-stu-id="93886-122">INPUTS</span></span>

### <span data-ttu-id="93886-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="93886-123">System.String</span></span>

## <span data-ttu-id="93886-124">출력</span><span class="sxs-lookup"><span data-stu-id="93886-124">OUTPUTS</span></span>

### <span data-ttu-id="93886-125">ActivityLogAlertLeafCondition를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="93886-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="93886-126">상속자</span><span class="sxs-lookup"><span data-stu-id="93886-126">NOTES</span></span>

## <span data-ttu-id="93886-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93886-127">RELATED LINKS</span></span>

[<span data-ttu-id="93886-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="93886-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="93886-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="93886-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="93886-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="93886-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="93886-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="93886-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="93886-132">제거-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="93886-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="93886-133">새로운 AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="93886-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)