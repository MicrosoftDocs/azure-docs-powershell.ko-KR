---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204643"
---
# <span data-ttu-id="70954-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="70954-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="70954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70954-102">SYNOPSIS</span></span>
<span data-ttu-id="70954-103">Azure 가상 컴퓨터를 이미지로 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="70954-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70954-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70954-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70954-105">DESCRIPTION</span></span>
<span data-ttu-id="70954-106">**AzVMReimage** Cmdlet은 Azure 가상 컴퓨터를 다시 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="70954-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70954-107">EXAMPLES</span></span>

### <span data-ttu-id="70954-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="70954-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="70954-109">이 명령은 ResourceGroup11의 VirtualMachine07 이라는 가상 컴퓨터를 다시 이미지에 이미지로 재구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="70954-110">변수</span><span class="sxs-lookup"><span data-stu-id="70954-110">PARAMETERS</span></span>

### <span data-ttu-id="70954-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70954-111">-AsJob</span></span>
<span data-ttu-id="70954-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="70954-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70954-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70954-113">-DefaultProfile</span></span>
<span data-ttu-id="70954-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="70954-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70954-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70954-115">-ResourceGroupName</span></span>
<span data-ttu-id="70954-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="70954-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="70954-117">-TempDisk</span></span>
<span data-ttu-id="70954-118">Temp 디스크를 이미지로 인쇄할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="70954-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="70954-119">-VMName</span></span>
<span data-ttu-id="70954-120">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70954-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="70954-121">-확인</span><span class="sxs-lookup"><span data-stu-id="70954-121">-Confirm</span></span>
<span data-ttu-id="70954-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70954-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70954-123">-WhatIf</span></span>
<span data-ttu-id="70954-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70954-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70954-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70954-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70954-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70954-126">CommonParameters</span></span>
<span data-ttu-id="70954-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70954-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70954-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="70954-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70954-129">입력</span><span class="sxs-lookup"><span data-stu-id="70954-129">INPUTS</span></span>

### <span data-ttu-id="70954-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70954-130">System.String</span></span>

## <span data-ttu-id="70954-131">출력</span><span class="sxs-lookup"><span data-stu-id="70954-131">OUTPUTS</span></span>

### <span data-ttu-id="70954-132">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="70954-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="70954-133">상속자</span><span class="sxs-lookup"><span data-stu-id="70954-133">NOTES</span></span>

## <span data-ttu-id="70954-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70954-134">RELATED LINKS</span></span>