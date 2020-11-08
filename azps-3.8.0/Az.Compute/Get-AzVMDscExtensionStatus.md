---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 9b35e76b6c64373a39bd3e14f8c1697c7c5f3baf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042894"
---
# <span data-ttu-id="cff17-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="cff17-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="cff17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff17-102">SYNOPSIS</span></span>
<span data-ttu-id="cff17-103">가상 컴퓨터에 대 한 DSC 확장 처리기의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="cff17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cff17-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff17-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cff17-105">DESCRIPTION</span></span>
<span data-ttu-id="cff17-106">**AzVMDscExtensionStatus** cmdlet은 리소스 그룹의 가상 컴퓨터에 대 한 DSC (원하는 상태 구성) 확장 처리기의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="cff17-107">구성이 적용 되 면이 cmdlet은 Start-DscConfiguration cmdlet과 일치 하는 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="cff17-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cff17-108">EXAMPLES</span></span>

## <span data-ttu-id="cff17-109">변수</span><span class="sxs-lookup"><span data-stu-id="cff17-109">PARAMETERS</span></span>

### <span data-ttu-id="cff17-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff17-110">-DefaultProfile</span></span>
<span data-ttu-id="cff17-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cff17-112">-이름</span><span class="sxs-lookup"><span data-stu-id="cff17-112">-Name</span></span>
<span data-ttu-id="cff17-113">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="cff17-114">Set-AzVMDscExtension cmdlet은이 이름을 **AzVMDscExtensionStatus** 에서 사용 하는 것과 동일한 값인 Microsoft Powershell로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="cff17-115">Set cmdlet의 기본 이름을 변경 하거나 자원 관리자 서식 파일에서 다른 자원 이름을 사용 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff17-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cff17-116">-ResourceGroupName</span></span>
<span data-ttu-id="cff17-117">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cff17-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="cff17-118">-VMName</span></span>
<span data-ttu-id="cff17-119">이 cmdlet이 DSC 확장 상태를 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cff17-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff17-120">CommonParameters</span></span>
<span data-ttu-id="cff17-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cff17-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff17-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cff17-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff17-123">입력</span><span class="sxs-lookup"><span data-stu-id="cff17-123">INPUTS</span></span>

### <span data-ttu-id="cff17-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cff17-124">System.String</span></span>

## <span data-ttu-id="cff17-125">출력</span><span class="sxs-lookup"><span data-stu-id="cff17-125">OUTPUTS</span></span>

### <span data-ttu-id="cff17-126">Microsoft. a. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="cff17-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="cff17-127">상속자</span><span class="sxs-lookup"><span data-stu-id="cff17-127">NOTES</span></span>

## <span data-ttu-id="cff17-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cff17-128">RELATED LINKS</span></span>

[<span data-ttu-id="cff17-129">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="cff17-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)

