---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216909"
---
# <span data-ttu-id="63fb2-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="63fb2-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="63fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="63fb2-103">지정 된 청사진 정의를 JSON 파일로 지정 된 출력 위치에 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="63fb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63fb2-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fb2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="63fb2-106">해당 가공물을 사용 하 여 청사진 정의를 내보내고 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="63fb2-107">이 cmdlet은 청사진의 최신 버전 (초안 또는 게시)을 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="63fb2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="63fb2-108">EXAMPLES</span></span>

### <span data-ttu-id="63fb2-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="63fb2-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="63fb2-110">해당 가공물을 사용 하 여 청사진 정의를 내보내고 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="63fb2-111">변수</span><span class="sxs-lookup"><span data-stu-id="63fb2-111">PARAMETERS</span></span>

### <span data-ttu-id="63fb2-112">-청사진</span><span class="sxs-lookup"><span data-stu-id="63fb2-112">-Blueprint</span></span>
<span data-ttu-id="63fb2-113">내보낼 청사진 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63fb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fb2-114">-DefaultProfile</span></span>
<span data-ttu-id="63fb2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63fb2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="63fb2-116">-Force</span></span>
<span data-ttu-id="63fb2-117">True로 설정 하면 실행 시 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="63fb2-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="63fb2-118">-OutputPath</span></span>
<span data-ttu-id="63fb2-119">JSON 형식으로 청사진 정의를 내보낼 디스크의 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="63fb2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63fb2-120">-PassThru</span></span>
<span data-ttu-id="63fb2-121">설정 되 면 cmdlet은 내보낸 청사진 정의를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="63fb2-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63fb2-123">-버전</span><span class="sxs-lookup"><span data-stu-id="63fb2-123">-Version</span></span>
<span data-ttu-id="63fb2-124">게시 된 청사진 정의 버전.</span><span class="sxs-lookup"><span data-stu-id="63fb2-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="63fb2-125">-확인</span><span class="sxs-lookup"><span data-stu-id="63fb2-125">-Confirm</span></span>
<span data-ttu-id="63fb2-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fb2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fb2-127">-WhatIf</span></span>
<span data-ttu-id="63fb2-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63fb2-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fb2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fb2-130">CommonParameters</span></span>
<span data-ttu-id="63fb2-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63fb2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fb2-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63fb2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fb2-133">입력</span><span class="sxs-lookup"><span data-stu-id="63fb2-133">INPUTS</span></span>

### <span data-ttu-id="63fb2-134">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="63fb2-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="63fb2-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63fb2-135">System.String</span></span>

## <span data-ttu-id="63fb2-136">출력</span><span class="sxs-lookup"><span data-stu-id="63fb2-136">OUTPUTS</span></span>

### <span data-ttu-id="63fb2-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63fb2-137">System.String</span></span>

## <span data-ttu-id="63fb2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="63fb2-138">NOTES</span></span>

## <span data-ttu-id="63fb2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63fb2-139">RELATED LINKS</span></span>