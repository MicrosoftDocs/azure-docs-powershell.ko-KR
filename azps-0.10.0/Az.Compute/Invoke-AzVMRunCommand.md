---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 3036b26c4f3ebe6fc6f039f1754acdb3b50977f6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877022"
---
# <span data-ttu-id="cb17f-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="cb17f-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="cb17f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb17f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb17f-103">VM의 실행 명령</span><span class="sxs-lookup"><span data-stu-id="cb17f-103">Run command on the VM.</span></span>

## <span data-ttu-id="cb17f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb17f-104">SYNTAX</span></span>

### <span data-ttu-id="cb17f-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="cb17f-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb17f-106">VMParameter</span><span class="sxs-lookup"><span data-stu-id="cb17f-106">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb17f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cb17f-107">DESCRIPTION</span></span>
<span data-ttu-id="cb17f-108">VM에서 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-108">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="cb17f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cb17f-109">EXAMPLES</span></span>

### <span data-ttu-id="cb17f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb17f-110">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="cb17f-111">' sample.ps1 ' 스크립트와 ' rgname ' 리소스 그룹의 ' vmname ' VM에 있는 매개 변수를 재정의 하 여 RunPowerShellScript의 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-111">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="cb17f-112">변수</span><span class="sxs-lookup"><span data-stu-id="cb17f-112">PARAMETERS</span></span>

### <span data-ttu-id="cb17f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb17f-113">-AsJob</span></span>
<span data-ttu-id="cb17f-114">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-115">-CommandId</span><span class="sxs-lookup"><span data-stu-id="cb17f-115">-CommandId</span></span>
<span data-ttu-id="cb17f-116">실행 명령 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-116">The run command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb17f-117">-DefaultProfile</span></span>
<span data-ttu-id="cb17f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="cb17f-119">-Parameter</span></span>
<span data-ttu-id="cb17f-120">실행 명령 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-120">The run command parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb17f-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb17f-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-123">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="cb17f-123">-ScriptPath</span></span>
<span data-ttu-id="cb17f-124">실행할 스크립트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-124">Path of the script to be executed.</span></span>  <span data-ttu-id="cb17f-125">이 값을 지정 하면 지정 된 스크립트는 명령의 기본 스크립트를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-125">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-126">-VM</span><span class="sxs-lookup"><span data-stu-id="cb17f-126">-VM</span></span>
<span data-ttu-id="cb17f-127">PS 가상 머신 개체</span><span class="sxs-lookup"><span data-stu-id="cb17f-127">The PS virtual Machine Object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="cb17f-128">-VMName</span></span>
<span data-ttu-id="cb17f-129">가상 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-129">The name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb17f-130">-확인</span><span class="sxs-lookup"><span data-stu-id="cb17f-130">-Confirm</span></span>
<span data-ttu-id="cb17f-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb17f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb17f-132">-WhatIf</span></span>
<span data-ttu-id="cb17f-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb17f-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb17f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb17f-135">CommonParameters</span></span>
<span data-ttu-id="cb17f-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb17f-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb17f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb17f-138">입력</span><span class="sxs-lookup"><span data-stu-id="cb17f-138">INPUTS</span></span>

### <span data-ttu-id="cb17f-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cb17f-139">System.String</span></span>
<span data-ttu-id="cb17f-140">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb17f-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="cb17f-141">출력</span><span class="sxs-lookup"><span data-stu-id="cb17f-141">OUTPUTS</span></span>

### <span data-ttu-id="cb17f-142">Microsoft. a. m a. 모델. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="cb17f-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="cb17f-143">상속자</span><span class="sxs-lookup"><span data-stu-id="cb17f-143">NOTES</span></span>

## <span data-ttu-id="cb17f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb17f-144">RELATED LINKS</span></span>
