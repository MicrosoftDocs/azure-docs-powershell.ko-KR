---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219135"
---
# <span data-ttu-id="b3e24-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="b3e24-101">Update-AzAlertState</span></span>

## <span data-ttu-id="b3e24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e24-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e24-103">알림 상태 업데이트</span><span class="sxs-lookup"><span data-stu-id="b3e24-103">Updates alert state</span></span>

## <span data-ttu-id="b3e24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3e24-104">SYNTAX</span></span>

### <span data-ttu-id="b3e24-105">ByAlertId (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3e24-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e24-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3e24-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e24-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b3e24-107">DESCRIPTION</span></span>
<span data-ttu-id="b3e24-108">**업데이트-AzAlertState** cmdlet 업데이트 알림 상태</span><span class="sxs-lookup"><span data-stu-id="b3e24-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="b3e24-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b3e24-109">EXAMPLES</span></span>

### <span data-ttu-id="b3e24-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3e24-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="b3e24-111">이 cmdlet은 경고 상태를 닫힘으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="b3e24-112">변수</span><span class="sxs-lookup"><span data-stu-id="b3e24-112">PARAMETERS</span></span>

### <span data-ttu-id="b3e24-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="b3e24-113">-AlertId</span></span>
<span data-ttu-id="b3e24-114">알림의 알림/ResourceId에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e24-115">-DefaultProfile</span></span>
<span data-ttu-id="b3e24-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3e24-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3e24-117">-InputObject</span></span>
<span data-ttu-id="b3e24-118">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e24-119">-상태</span><span class="sxs-lookup"><span data-stu-id="b3e24-119">-State</span></span>
<span data-ttu-id="b3e24-120">업데이트 된 알림 상태</span><span class="sxs-lookup"><span data-stu-id="b3e24-120">Updated Alert State</span></span>

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

### <span data-ttu-id="b3e24-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b3e24-121">-Confirm</span></span>
<span data-ttu-id="b3e24-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e24-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e24-123">-WhatIf</span></span>
<span data-ttu-id="b3e24-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e24-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e24-126">CommonParameters</span></span>
<span data-ttu-id="b3e24-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3e24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e24-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3e24-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e24-129">입력</span><span class="sxs-lookup"><span data-stu-id="b3e24-129">INPUTS</span></span>

### <span data-ttu-id="b3e24-130">않아야</span><span class="sxs-lookup"><span data-stu-id="b3e24-130">None</span></span>

## <span data-ttu-id="b3e24-131">출력</span><span class="sxs-lookup"><span data-stu-id="b3e24-131">OUTPUTS</span></span>

### <span data-ttu-id="b3e24-132">AlertsManagement 모델을 생성 합니다. PSAlert</span><span class="sxs-lookup"><span data-stu-id="b3e24-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="b3e24-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b3e24-133">NOTES</span></span>

## <span data-ttu-id="b3e24-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3e24-134">RELATED LINKS</span></span>