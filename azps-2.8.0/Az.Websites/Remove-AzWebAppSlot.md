---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 38b11543140a0f789674e4109db8cc73c7843f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874120"
---
# <span data-ttu-id="e32da-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="e32da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e32da-102">SYNOPSIS</span></span>

## <span data-ttu-id="e32da-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e32da-103">SYNTAX</span></span>

### <span data-ttu-id="e32da-104">S1</span><span class="sxs-lookup"><span data-stu-id="e32da-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e32da-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="e32da-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32da-106">설명은</span><span class="sxs-lookup"><span data-stu-id="e32da-106">DESCRIPTION</span></span>
<span data-ttu-id="e32da-107">**AzWebAppSlot** cmdlet은 리소스 그룹과 웹 앱 이름을 제공 하는 Azure Web app 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="e32da-108">이 cmdlet은 기본적으로 모든 슬롯과 메트릭스도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="e32da-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e32da-109">EXAMPLES</span></span>

### <span data-ttu-id="e32da-110">예제 1: 웹 앱 슬롯 제거</span><span class="sxs-lookup"><span data-stu-id="e32da-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="e32da-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 웹 앱 ContosoSite와 연결 된 Slot001 이라는 슬롯을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e32da-112">변수</span><span class="sxs-lookup"><span data-stu-id="e32da-112">PARAMETERS</span></span>

### <span data-ttu-id="e32da-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e32da-113">-AsJob</span></span>
<span data-ttu-id="e32da-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e32da-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e32da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32da-115">-DefaultProfile</span></span>
<span data-ttu-id="e32da-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e32da-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e32da-117">-Force</span></span>
<span data-ttu-id="e32da-118">강제로 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="e32da-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="e32da-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e32da-119">-Name</span></span>
<span data-ttu-id="e32da-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="e32da-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32da-121">-ResourceGroupName</span></span>
<span data-ttu-id="e32da-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e32da-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-123">-슬롯</span><span class="sxs-lookup"><span data-stu-id="e32da-123">-Slot</span></span>
<span data-ttu-id="e32da-124">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="e32da-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="e32da-125">-WebApp</span></span>
<span data-ttu-id="e32da-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="e32da-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-127">-확인</span><span class="sxs-lookup"><span data-stu-id="e32da-127">-Confirm</span></span>
<span data-ttu-id="e32da-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e32da-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32da-129">-WhatIf</span></span>
<span data-ttu-id="e32da-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e32da-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e32da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32da-132">CommonParameters</span></span>
<span data-ttu-id="e32da-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32da-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32da-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32da-135">입력</span><span class="sxs-lookup"><span data-stu-id="e32da-135">INPUTS</span></span>

### <span data-ttu-id="e32da-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e32da-136">System.String</span></span>

### <span data-ttu-id="e32da-137">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="e32da-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e32da-138">출력</span><span class="sxs-lookup"><span data-stu-id="e32da-138">OUTPUTS</span></span>

### <span data-ttu-id="e32da-139">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e32da-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="e32da-140">상속자</span><span class="sxs-lookup"><span data-stu-id="e32da-140">NOTES</span></span>

## <span data-ttu-id="e32da-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e32da-141">RELATED LINKS</span></span>

[<span data-ttu-id="e32da-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e32da-143">새로운 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="e32da-144">다시 시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="e32da-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="e32da-146">시작-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="e32da-147">중지-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e32da-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="e32da-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e32da-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)