---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: c7ce5872338b9fd3b7741f341d661d09c2eef16a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528505"
---
# <span data-ttu-id="28849-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28849-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="28849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28849-102">SYNOPSIS</span></span>
<span data-ttu-id="28849-103">응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28849-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28849-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28849-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28849-105">DESCRIPTION</span></span>
<span data-ttu-id="28849-106">**Remove-AzureRmApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="28849-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28849-107">EXAMPLES</span></span>

### <span data-ttu-id="28849-108">예제 1: 지정 된 응용 프로그램 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="28849-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="28849-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 이라는 응용 프로그램 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="28849-110">변수</span><span class="sxs-lookup"><span data-stu-id="28849-110">PARAMETERS</span></span>

### <span data-ttu-id="28849-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28849-111">-DefaultProfile</span></span>
<span data-ttu-id="28849-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28849-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28849-113">-Force</span><span class="sxs-lookup"><span data-stu-id="28849-113">-Force</span></span>
<span data-ttu-id="28849-114">리소스가 할당 되었는지 여부에 관계 없이 cmdlet이 응용 프로그램 게이트웨이를 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="28849-115">-이름</span><span class="sxs-lookup"><span data-stu-id="28849-115">-Name</span></span>
<span data-ttu-id="28849-116">제거할 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="28849-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28849-117">-PassThru</span></span>
<span data-ttu-id="28849-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28849-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28849-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28849-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28849-120">-ResourceGroupName</span></span>
<span data-ttu-id="28849-121">응용 프로그램 게이트웨이가 속한 리소스 그룹 이름의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="28849-122">-확인</span><span class="sxs-lookup"><span data-stu-id="28849-122">-Confirm</span></span>
<span data-ttu-id="28849-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28849-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28849-124">-WhatIf</span></span>
<span data-ttu-id="28849-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28849-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28849-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28849-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28849-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28849-127">CommonParameters</span></span>
<span data-ttu-id="28849-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28849-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28849-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28849-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28849-130">입력</span><span class="sxs-lookup"><span data-stu-id="28849-130">INPUTS</span></span>

### <span data-ttu-id="28849-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28849-131">System.String</span></span>

### <span data-ttu-id="28849-132">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="28849-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="28849-133">출력</span><span class="sxs-lookup"><span data-stu-id="28849-133">OUTPUTS</span></span>

### <span data-ttu-id="28849-134">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="28849-134">System.Boolean</span></span>

## <span data-ttu-id="28849-135">상속자</span><span class="sxs-lookup"><span data-stu-id="28849-135">NOTES</span></span>

## <span data-ttu-id="28849-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28849-136">RELATED LINKS</span></span>

[<span data-ttu-id="28849-137">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="28849-137">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

