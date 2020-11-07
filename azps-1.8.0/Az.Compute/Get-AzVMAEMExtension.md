---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 8cd67aa715b0092c82a3553158a4736d8f1e850e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869101"
---
# <span data-ttu-id="13810-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="13810-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="13810-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13810-102">SYNOPSIS</span></span>
<span data-ttu-id="13810-103">AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="13810-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13810-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13810-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13810-105">DESCRIPTION</span></span>
<span data-ttu-id="13810-106">**AzVMAEMExtension** CMDLET은 AEM (Azure 확장 모니터링) 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="13810-107">예제의</span><span class="sxs-lookup"><span data-stu-id="13810-107">EXAMPLES</span></span>

### <span data-ttu-id="13810-108">예제 1: AEM 확장명 가져오기</span><span class="sxs-lookup"><span data-stu-id="13810-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="13810-109">이 명령은 contoso-server 라는 가상 컴퓨터에 대 한 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="13810-110">변수</span><span class="sxs-lookup"><span data-stu-id="13810-110">PARAMETERS</span></span>

### <span data-ttu-id="13810-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13810-111">-DefaultProfile</span></span>
<span data-ttu-id="13810-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13810-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13810-113">-이름</span><span class="sxs-lookup"><span data-stu-id="13810-113">-Name</span></span>
<span data-ttu-id="13810-114">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13810-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="13810-115">이 cmdlet은이 cmdlet에서 지정 하는 가상 컴퓨터의 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="13810-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="13810-116">-OSType</span></span>
<span data-ttu-id="13810-117">운영 체제 디스크의 운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13810-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="13810-118">운영 체제 디스크에 형식이 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13810-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="13810-119">이 매개 변수에 허용 되는 값은 Windows 및 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="13810-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13810-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13810-120">-ResourceGroupName</span></span>
<span data-ttu-id="13810-121">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13810-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="13810-122">이 cmdlet은 해당 가상 컴퓨터의 AEM 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="13810-123">-상태</span><span class="sxs-lookup"><span data-stu-id="13810-123">-Status</span></span>
<span data-ttu-id="13810-124">이 cmdlet이 AEM extension의 instance 뷰에서만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13810-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="13810-125">-VMName</span></span>
<span data-ttu-id="13810-126">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13810-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="13810-127">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터의 AEM extension에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13810-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="13810-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13810-128">CommonParameters</span></span>
<span data-ttu-id="13810-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13810-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13810-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13810-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13810-131">입력</span><span class="sxs-lookup"><span data-stu-id="13810-131">INPUTS</span></span>

### <span data-ttu-id="13810-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13810-132">System.String</span></span>

### <span data-ttu-id="13810-133">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="13810-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13810-134">출력</span><span class="sxs-lookup"><span data-stu-id="13810-134">OUTPUTS</span></span>

### <span data-ttu-id="13810-135">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="13810-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="13810-136">상속자</span><span class="sxs-lookup"><span data-stu-id="13810-136">NOTES</span></span>

## <span data-ttu-id="13810-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13810-137">RELATED LINKS</span></span>

[<span data-ttu-id="13810-138">제거-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="13810-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="13810-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="13810-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="13810-140">테스트-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="13810-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)

