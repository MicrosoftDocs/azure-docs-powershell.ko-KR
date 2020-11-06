---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529903"
---
# <span data-ttu-id="527af-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="527af-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="527af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="527af-102">SYNOPSIS</span></span>
<span data-ttu-id="527af-103">스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="527af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="527af-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="527af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="527af-105">DESCRIPTION</span></span>
<span data-ttu-id="527af-106">**제거-AzureRmSnapshot** cmdlet은 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="527af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="527af-107">EXAMPLES</span></span>

### <span data-ttu-id="527af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="527af-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="527af-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Snapshot01 ' 인 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="527af-110">변수</span><span class="sxs-lookup"><span data-stu-id="527af-110">PARAMETERS</span></span>

### <span data-ttu-id="527af-111">-Force</span><span class="sxs-lookup"><span data-stu-id="527af-111">-Force</span></span>
<span data-ttu-id="527af-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527af-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="527af-113">-ResourceGroupName</span></span>
<span data-ttu-id="527af-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-114">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="527af-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="527af-115">-SnapshotName</span></span>
<span data-ttu-id="527af-116">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-116">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="527af-117">-확인</span><span class="sxs-lookup"><span data-stu-id="527af-117">-Confirm</span></span>
<span data-ttu-id="527af-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527af-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="527af-119">-WhatIf</span></span>
<span data-ttu-id="527af-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="527af-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="527af-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="527af-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527af-122">CommonParameters</span></span>
<span data-ttu-id="527af-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="527af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527af-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527af-125">입력</span><span class="sxs-lookup"><span data-stu-id="527af-125">INPUTS</span></span>

### <span data-ttu-id="527af-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="527af-126">System.String</span></span>

## <span data-ttu-id="527af-127">출력</span><span class="sxs-lookup"><span data-stu-id="527af-127">OUTPUTS</span></span>

### <span data-ttu-id="527af-128">System. 개체</span><span class="sxs-lookup"><span data-stu-id="527af-128">System.Object</span></span>

## <span data-ttu-id="527af-129">상속자</span><span class="sxs-lookup"><span data-stu-id="527af-129">NOTES</span></span>

## <span data-ttu-id="527af-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="527af-130">RELATED LINKS</span></span>
