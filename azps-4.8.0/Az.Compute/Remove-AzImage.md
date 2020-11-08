---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048408"
---
# <span data-ttu-id="4cce3-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="4cce3-101">Remove-AzImage</span></span>

## <span data-ttu-id="4cce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cce3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cce3-103">이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-103">Removes an image.</span></span>

## <span data-ttu-id="4cce3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cce3-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cce3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4cce3-105">DESCRIPTION</span></span>
<span data-ttu-id="4cce3-106">**AzImage** cmdlet은 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="4cce3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4cce3-107">EXAMPLES</span></span>

### <span data-ttu-id="4cce3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4cce3-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="4cce3-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Image01 ' 인 이미지를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4cce3-110">변수</span><span class="sxs-lookup"><span data-stu-id="4cce3-110">PARAMETERS</span></span>

### <span data-ttu-id="4cce3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cce3-111">-AsJob</span></span>
<span data-ttu-id="4cce3-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4cce3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cce3-113">-DefaultProfile</span></span>
<span data-ttu-id="4cce3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cce3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4cce3-115">-Force</span></span>
<span data-ttu-id="4cce3-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cce3-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4cce3-117">-ImageName</span></span>
<span data-ttu-id="4cce3-118">이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cce3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cce3-119">-ResourceGroupName</span></span>
<span data-ttu-id="4cce3-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4cce3-121">-확인</span><span class="sxs-lookup"><span data-stu-id="4cce3-121">-Confirm</span></span>
<span data-ttu-id="4cce3-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cce3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cce3-123">-WhatIf</span></span>
<span data-ttu-id="4cce3-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cce3-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cce3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cce3-126">CommonParameters</span></span>
<span data-ttu-id="4cce3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cce3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cce3-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cce3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cce3-129">입력</span><span class="sxs-lookup"><span data-stu-id="4cce3-129">INPUTS</span></span>

### <span data-ttu-id="4cce3-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4cce3-130">System.String</span></span>

## <span data-ttu-id="4cce3-131">출력</span><span class="sxs-lookup"><span data-stu-id="4cce3-131">OUTPUTS</span></span>

### <span data-ttu-id="4cce3-132">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="4cce3-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4cce3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4cce3-133">NOTES</span></span>

## <span data-ttu-id="4cce3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cce3-134">RELATED LINKS</span></span>