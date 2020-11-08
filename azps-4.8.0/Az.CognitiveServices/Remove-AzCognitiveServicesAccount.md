---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047886"
---
# <span data-ttu-id="7c7cf-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c7cf-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="7c7cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7cf-103">인지 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="7c7cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c7cf-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c7cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c7cf-105">DESCRIPTION</span></span>
<span data-ttu-id="7c7cf-106">**AzCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7c7cf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c7cf-107">EXAMPLES</span></span>

### <span data-ttu-id="7c7cf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c7cf-108">Example 1</span></span>
<span data-ttu-id="7c7cf-109">이 명령은 아무것도 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="7c7cf-110">변수</span><span class="sxs-lookup"><span data-stu-id="7c7cf-110">PARAMETERS</span></span>

### <span data-ttu-id="7c7cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7cf-111">-DefaultProfile</span></span>
<span data-ttu-id="7c7cf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7c7cf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c7cf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7c7cf-113">-Force</span></span>
<span data-ttu-id="7c7cf-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c7cf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="7c7cf-115">-Name</span></span>
<span data-ttu-id="7c7cf-116">삭제할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c7cf-118">인지 서비스 계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7cf-119">-확인</span><span class="sxs-lookup"><span data-stu-id="7c7cf-119">-Confirm</span></span>
<span data-ttu-id="7c7cf-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c7cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c7cf-121">-WhatIf</span></span>
<span data-ttu-id="7c7cf-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c7cf-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c7cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7cf-124">CommonParameters</span></span>
<span data-ttu-id="7c7cf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7cf-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c7cf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7cf-127">입력</span><span class="sxs-lookup"><span data-stu-id="7c7cf-127">INPUTS</span></span>

### <span data-ttu-id="7c7cf-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c7cf-128">System.String</span></span>

## <span data-ttu-id="7c7cf-129">출력</span><span class="sxs-lookup"><span data-stu-id="7c7cf-129">OUTPUTS</span></span>

### <span data-ttu-id="7c7cf-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="7c7cf-130">System.Void</span></span>

## <span data-ttu-id="7c7cf-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7c7cf-131">NOTES</span></span>

## <span data-ttu-id="7c7cf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c7cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c7cf-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c7cf-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7c7cf-134">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c7cf-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7c7cf-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7c7cf-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

