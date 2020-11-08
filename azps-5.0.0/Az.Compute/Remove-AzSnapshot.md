---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215717"
---
# <span data-ttu-id="e5248-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="e5248-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="e5248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5248-102">SYNOPSIS</span></span>
<span data-ttu-id="e5248-103">스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-103">Removes a snapshot.</span></span>

## <span data-ttu-id="e5248-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5248-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5248-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5248-105">DESCRIPTION</span></span>
<span data-ttu-id="e5248-106">**제거-AzSnapshot** cmdlet은 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="e5248-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5248-107">EXAMPLES</span></span>

### <span data-ttu-id="e5248-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5248-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="e5248-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Snapshot01 ' 인 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e5248-110">변수</span><span class="sxs-lookup"><span data-stu-id="e5248-110">PARAMETERS</span></span>

### <span data-ttu-id="e5248-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5248-111">-AsJob</span></span>
<span data-ttu-id="e5248-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e5248-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5248-113">-DefaultProfile</span></span>
<span data-ttu-id="e5248-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5248-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e5248-115">-Force</span></span>
<span data-ttu-id="e5248-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5248-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5248-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5248-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5248-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e5248-119">-SnapshotName</span></span>
<span data-ttu-id="e5248-120">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="e5248-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e5248-121">-Confirm</span></span>
<span data-ttu-id="e5248-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5248-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5248-123">-WhatIf</span></span>
<span data-ttu-id="e5248-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5248-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5248-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5248-126">CommonParameters</span></span>
<span data-ttu-id="e5248-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5248-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5248-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e5248-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5248-129">입력</span><span class="sxs-lookup"><span data-stu-id="e5248-129">INPUTS</span></span>

### <span data-ttu-id="e5248-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5248-130">System.String</span></span>

## <span data-ttu-id="e5248-131">출력</span><span class="sxs-lookup"><span data-stu-id="e5248-131">OUTPUTS</span></span>

### <span data-ttu-id="e5248-132">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="e5248-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e5248-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e5248-133">NOTES</span></span>

## <span data-ttu-id="e5248-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5248-134">RELATED LINKS</span></span>