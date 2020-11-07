---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 353d4ca1e5f5eebd1cda1ec22d801a73db239963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876808"
---
# <span data-ttu-id="06670-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="06670-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="06670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06670-102">SYNOPSIS</span></span>
<span data-ttu-id="06670-103">새 데이터 상자에 지 장치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="06670-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="06670-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06670-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06670-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06670-105">DESCRIPTION</span></span>
<span data-ttu-id="06670-106">**AzDataBoxEdgeDevice** cmdlet은 새 데이터 상자 가장자리 장치를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="06670-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="06670-107">예제의</span><span class="sxs-lookup"><span data-stu-id="06670-107">EXAMPLES</span></span>

### <span data-ttu-id="06670-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="06670-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="06670-109">변수</span><span class="sxs-lookup"><span data-stu-id="06670-109">PARAMETERS</span></span>

### <span data-ttu-id="06670-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06670-110">-AsJob</span></span>
<span data-ttu-id="06670-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="06670-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06670-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06670-112">-DefaultProfile</span></span>
<span data-ttu-id="06670-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06670-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06670-114">-위치</span><span class="sxs-lookup"><span data-stu-id="06670-114">-Location</span></span>
<span data-ttu-id="06670-115">장치 위치</span><span class="sxs-lookup"><span data-stu-id="06670-115">Location of the device</span></span>

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

### <span data-ttu-id="06670-116">-이름</span><span class="sxs-lookup"><span data-stu-id="06670-116">-Name</span></span>
<span data-ttu-id="06670-117">자원 이름</span><span class="sxs-lookup"><span data-stu-id="06670-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06670-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06670-118">-ResourceGroupName</span></span>
<span data-ttu-id="06670-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="06670-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06670-120">-Sku</span><span class="sxs-lookup"><span data-stu-id="06670-120">-Sku</span></span>
<span data-ttu-id="06670-121">사용할 수 있는 Sku는 Edge, Gateway입니다.</span><span class="sxs-lookup"><span data-stu-id="06670-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="06670-122">-확인</span><span class="sxs-lookup"><span data-stu-id="06670-122">-Confirm</span></span>
<span data-ttu-id="06670-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06670-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06670-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06670-124">-WhatIf</span></span>
<span data-ttu-id="06670-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06670-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06670-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06670-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06670-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06670-127">CommonParameters</span></span>
<span data-ttu-id="06670-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06670-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06670-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06670-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06670-130">입력</span><span class="sxs-lookup"><span data-stu-id="06670-130">INPUTS</span></span>

### <span data-ttu-id="06670-131">않아야</span><span class="sxs-lookup"><span data-stu-id="06670-131">None</span></span>

## <span data-ttu-id="06670-132">출력</span><span class="sxs-lookup"><span data-stu-id="06670-132">OUTPUTS</span></span>

### <span data-ttu-id="06670-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="06670-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="06670-134">상속자</span><span class="sxs-lookup"><span data-stu-id="06670-134">NOTES</span></span>

## <span data-ttu-id="06670-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06670-135">RELATED LINKS</span></span>