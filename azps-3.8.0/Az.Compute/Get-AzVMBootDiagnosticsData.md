---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: c56c9e586b0089311477fc12b6624c74321f9a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94045057"
---
# <span data-ttu-id="8d7ee-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="8d7ee-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="8d7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8d7ee-103">가상 컴퓨터에 대 한 부팅 진단 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="8d7ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d7ee-104">SYNTAX</span></span>

### <span data-ttu-id="8d7ee-105">WindowsParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d7ee-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d7ee-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="8d7ee-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d7ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="8d7ee-108">**AzVMBootDiagnosticsData** cmdlet은 가상 컴퓨터에 대 한 부팅 진단 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="8d7ee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8d7ee-109">EXAMPLES</span></span>

### <span data-ttu-id="8d7ee-110">예제 1: 부팅 진단 데이터 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d7ee-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="8d7ee-111">이 명령은 ContosoVM07 이라는 가상 컴퓨터에 대 한 부팅 진단 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="8d7ee-112">이 가상 컴퓨터는 Windows 운영 체제를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="8d7ee-113">명령은 지정 된 로컬 경로에 데이터를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="8d7ee-114">변수</span><span class="sxs-lookup"><span data-stu-id="8d7ee-114">PARAMETERS</span></span>

### <span data-ttu-id="8d7ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d7ee-115">-DefaultProfile</span></span>
<span data-ttu-id="8d7ee-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d7ee-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="8d7ee-117">-Linux</span></span>
<span data-ttu-id="8d7ee-118">가상 컴퓨터가 Linux 운영 체제를 실행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7ee-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="8d7ee-119">-LocalPath</span></span>
<span data-ttu-id="8d7ee-120">부팅 진단 데이터의 로컬 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d7ee-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8d7ee-121">-Name</span></span>
<span data-ttu-id="8d7ee-122">이 cmdlet이 진단 데이터를 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="8d7ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d7ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d7ee-124">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8d7ee-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="8d7ee-125">-Windows</span></span>
<span data-ttu-id="8d7ee-126">가상 컴퓨터가 Windows 운영 체제를 실행 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d7ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d7ee-127">CommonParameters</span></span>
<span data-ttu-id="8d7ee-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d7ee-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d7ee-130">입력</span><span class="sxs-lookup"><span data-stu-id="8d7ee-130">INPUTS</span></span>

### <span data-ttu-id="8d7ee-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d7ee-131">System.String</span></span>

## <span data-ttu-id="8d7ee-132">출력</span><span class="sxs-lookup"><span data-stu-id="8d7ee-132">OUTPUTS</span></span>

### <span data-ttu-id="8d7ee-133">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d7ee-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8d7ee-134">Microsoft. a. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="8d7ee-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="8d7ee-135">상속자</span><span class="sxs-lookup"><span data-stu-id="8d7ee-135">NOTES</span></span>

## <span data-ttu-id="8d7ee-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d7ee-136">RELATED LINKS</span></span>

[<span data-ttu-id="8d7ee-137">Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8d7ee-137">Set-AzVMBootDiagnostics</span></span>](./Set-AzVMBootDiagnostics.md)

