---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226424"
---
# <span data-ttu-id="762d2-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="762d2-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="762d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="762d2-102">SYNOPSIS</span></span>
<span data-ttu-id="762d2-103">가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="762d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="762d2-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="762d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="762d2-105">DESCRIPTION</span></span>
<span data-ttu-id="762d2-106">**AzVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="762d2-107">이 cmdlet의 출력을 Update-AzVM cmdlet에 전달 하 여 변경 내용을 구현 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="762d2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="762d2-108">EXAMPLES</span></span>

### <span data-ttu-id="762d2-109">예제 1: 가상 머신에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="762d2-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="762d2-110">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="762d2-111">이 명령은 파이프라인 연산자를 사용 하 여 결과를 Update-AzVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="762d2-112">이 명령은 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="762d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="762d2-113">PARAMETERS</span></span>

### <span data-ttu-id="762d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762d2-114">-DefaultProfile</span></span>
<span data-ttu-id="762d2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="762d2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="762d2-116">-Name</span></span>
<span data-ttu-id="762d2-117">이 cmdlet이 제거 하는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762d2-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="762d2-118">-NoWait</span></span>
<span data-ttu-id="762d2-119">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="762d2-120">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="762d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="762d2-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="762d2-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="762d2-123">-VMName</span></span>
<span data-ttu-id="762d2-124">이 cmdlet이 진단 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762d2-125">CommonParameters</span></span>
<span data-ttu-id="762d2-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762d2-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="762d2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762d2-128">입력</span><span class="sxs-lookup"><span data-stu-id="762d2-128">INPUTS</span></span>

### <span data-ttu-id="762d2-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="762d2-129">System.String</span></span>

## <span data-ttu-id="762d2-130">출력</span><span class="sxs-lookup"><span data-stu-id="762d2-130">OUTPUTS</span></span>

### <span data-ttu-id="762d2-131">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="762d2-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="762d2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="762d2-132">NOTES</span></span>

## <span data-ttu-id="762d2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="762d2-133">RELATED LINKS</span></span>

[<span data-ttu-id="762d2-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="762d2-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="762d2-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="762d2-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="762d2-136">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="762d2-136">Update-AzVM</span></span>](./Update-AzVM.md)

