---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: 92c4ea23f54025fdf32821742896459587f605f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530960"
---
# <span data-ttu-id="223a2-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="223a2-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="223a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="223a2-102">SYNOPSIS</span></span>
<span data-ttu-id="223a2-103">로그 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="223a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="223a2-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="223a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="223a2-105">DESCRIPTION</span></span>
<span data-ttu-id="223a2-106">**AzureRmLogProfile** cmdlet은 로그 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="223a2-107">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="223a2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="223a2-108">EXAMPLES</span></span>

## <span data-ttu-id="223a2-109">변수</span><span class="sxs-lookup"><span data-stu-id="223a2-109">PARAMETERS</span></span>

### <span data-ttu-id="223a2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223a2-110">-DefaultProfile</span></span>
<span data-ttu-id="223a2-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="223a2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223a2-112">-이름</span><span class="sxs-lookup"><span data-stu-id="223a2-112">-Name</span></span>
<span data-ttu-id="223a2-113">제거할 로그 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="223a2-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="223a2-114">-PassThru</span></span>
<span data-ttu-id="223a2-115">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="223a2-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="223a2-116">-확인</span><span class="sxs-lookup"><span data-stu-id="223a2-116">-Confirm</span></span>
<span data-ttu-id="223a2-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="223a2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="223a2-118">-WhatIf</span></span>
<span data-ttu-id="223a2-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="223a2-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="223a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223a2-121">CommonParameters</span></span>
<span data-ttu-id="223a2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="223a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223a2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="223a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223a2-124">입력</span><span class="sxs-lookup"><span data-stu-id="223a2-124">INPUTS</span></span>

### <span data-ttu-id="223a2-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="223a2-125">System.String</span></span>

## <span data-ttu-id="223a2-126">출력</span><span class="sxs-lookup"><span data-stu-id="223a2-126">OUTPUTS</span></span>

### <span data-ttu-id="223a2-127">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="223a2-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="223a2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="223a2-128">NOTES</span></span>

## <span data-ttu-id="223a2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="223a2-129">RELATED LINKS</span></span>

[<span data-ttu-id="223a2-130">추가-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="223a2-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="223a2-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="223a2-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

