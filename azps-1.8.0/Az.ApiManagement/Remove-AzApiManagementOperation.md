---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 6c44ff9fe0c96dc3b87540493f11864b2441d340
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869418"
---
# <span data-ttu-id="962a4-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="962a4-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="962a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="962a4-102">SYNOPSIS</span></span>
<span data-ttu-id="962a4-103">기존 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-103">Removes an existing operation.</span></span>

## <span data-ttu-id="962a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="962a4-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="962a4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="962a4-105">DESCRIPTION</span></span>
<span data-ttu-id="962a4-106">**AzApiManagementOperation** cmdlet에서는 기존 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="962a4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="962a4-107">EXAMPLES</span></span>

### <span data-ttu-id="962a4-108">예제 1: 기존 API 연산 제거</span><span class="sxs-lookup"><span data-stu-id="962a4-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="962a4-109">이 명령은 기존 API 연산을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="962a4-110">변수</span><span class="sxs-lookup"><span data-stu-id="962a4-110">PARAMETERS</span></span>

### <span data-ttu-id="962a4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="962a4-111">-ApiId</span></span>
<span data-ttu-id="962a4-112">API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="962a4-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="962a4-113">-ApiRevision</span></span>
<span data-ttu-id="962a4-114">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-114">Identifier of API Revision.</span></span> <span data-ttu-id="962a4-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-115">This parameter is optional.</span></span> <span data-ttu-id="962a4-116">지정 하지 않으면 현재 활성 상태인 api 개정판에서 작업이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="962a4-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="962a4-117">-Context</span></span>
<span data-ttu-id="962a4-118">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-118">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962a4-119">-DefaultProfile</span></span>
<span data-ttu-id="962a4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962a4-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="962a4-121">-OperationId</span></span>
<span data-ttu-id="962a4-122">API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="962a4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="962a4-123">-PassThru</span></span>
<span data-ttu-id="962a4-124">이 cmdlet이 성공할 경우 $True 값을 반환 하거나, $False 값이 없는 경우, 그렇지 않은 경우이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962a4-125">-확인</span><span class="sxs-lookup"><span data-stu-id="962a4-125">-Confirm</span></span>
<span data-ttu-id="962a4-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962a4-127">-WhatIf</span></span>
<span data-ttu-id="962a4-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="962a4-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962a4-130">CommonParameters</span></span>
<span data-ttu-id="962a4-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="962a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962a4-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962a4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962a4-133">입력</span><span class="sxs-lookup"><span data-stu-id="962a4-133">INPUTS</span></span>

### <span data-ttu-id="962a4-134">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="962a4-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="962a4-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="962a4-135">System.String</span></span>

### <span data-ttu-id="962a4-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="962a4-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="962a4-137">출력</span><span class="sxs-lookup"><span data-stu-id="962a4-137">OUTPUTS</span></span>

### <span data-ttu-id="962a4-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="962a4-138">System.Boolean</span></span>

## <span data-ttu-id="962a4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="962a4-139">NOTES</span></span>

## <span data-ttu-id="962a4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="962a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="962a4-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="962a4-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="962a4-142">새로운 AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="962a4-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="962a4-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="962a4-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)

