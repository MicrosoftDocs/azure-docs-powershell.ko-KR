---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: bbfbf2a8a0cace2580dbd929a81bfec8a120cfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526251"
---
# <span data-ttu-id="88956-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="88956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88956-102">SYNOPSIS</span></span>
<span data-ttu-id="88956-103">Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88956-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88956-104">SYNTAX</span></span>

### <span data-ttu-id="88956-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="88956-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88956-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="88956-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88956-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88956-107">DESCRIPTION</span></span>
<span data-ttu-id="88956-108">**AzureRmVM** Cmdlet은 Azure에서 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="88956-109">예제의</span><span class="sxs-lookup"><span data-stu-id="88956-109">EXAMPLES</span></span>

### <span data-ttu-id="88956-110">예제 1: 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="88956-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="88956-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="88956-112">변수</span><span class="sxs-lookup"><span data-stu-id="88956-112">PARAMETERS</span></span>

### <span data-ttu-id="88956-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88956-113">-AsJob</span></span>
<span data-ttu-id="88956-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="88956-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88956-115">-DefaultProfile</span></span>
<span data-ttu-id="88956-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88956-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88956-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88956-117">-Force</span></span>
<span data-ttu-id="88956-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88956-119">-Id</span><span class="sxs-lookup"><span data-stu-id="88956-119">-Id</span></span>
<span data-ttu-id="88956-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88956-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88956-121">-이름</span><span class="sxs-lookup"><span data-stu-id="88956-121">-Name</span></span>
<span data-ttu-id="88956-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88956-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88956-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88956-123">-ResourceGroupName</span></span>
<span data-ttu-id="88956-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88956-125">-확인</span><span class="sxs-lookup"><span data-stu-id="88956-125">-Confirm</span></span>
<span data-ttu-id="88956-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88956-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88956-127">-WhatIf</span></span>
<span data-ttu-id="88956-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88956-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88956-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88956-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88956-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88956-130">CommonParameters</span></span>
<span data-ttu-id="88956-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88956-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88956-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88956-133">입력</span><span class="sxs-lookup"><span data-stu-id="88956-133">INPUTS</span></span>

### <span data-ttu-id="88956-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88956-134">System.String</span></span>

## <span data-ttu-id="88956-135">출력</span><span class="sxs-lookup"><span data-stu-id="88956-135">OUTPUTS</span></span>

### <span data-ttu-id="88956-136">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="88956-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="88956-137">상속자</span><span class="sxs-lookup"><span data-stu-id="88956-137">NOTES</span></span>

## <span data-ttu-id="88956-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88956-138">RELATED LINKS</span></span>

[<span data-ttu-id="88956-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="88956-140">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-140">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="88956-141">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="88956-142">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="88956-143">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-143">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="88956-144">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88956-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

