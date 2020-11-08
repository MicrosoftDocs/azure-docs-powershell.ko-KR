---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a316a59492034f0effd2d233ce386cbd6a256c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218006"
---
# <span data-ttu-id="77b31-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="77b31-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="77b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77b31-102">SYNOPSIS</span></span>
<span data-ttu-id="77b31-103">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="77b31-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77b31-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77b31-105">설명은</span><span class="sxs-lookup"><span data-stu-id="77b31-105">DESCRIPTION</span></span>
<span data-ttu-id="77b31-106">JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="77b31-107">예제의</span><span class="sxs-lookup"><span data-stu-id="77b31-107">EXAMPLES</span></span>

### <span data-ttu-id="77b31-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="77b31-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="77b31-109">새 VM 규칙을 사용 하 여 JIT 네트워크 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="77b31-110">변수</span><span class="sxs-lookup"><span data-stu-id="77b31-110">PARAMETERS</span></span>

### <span data-ttu-id="77b31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b31-111">-DefaultProfile</span></span>
<span data-ttu-id="77b31-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77b31-113">-종류</span><span class="sxs-lookup"><span data-stu-id="77b31-113">-Kind</span></span>
<span data-ttu-id="77b31-114">형식.</span><span class="sxs-lookup"><span data-stu-id="77b31-114">Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b31-115">-위치</span><span class="sxs-lookup"><span data-stu-id="77b31-115">-Location</span></span>
<span data-ttu-id="77b31-116">Location.</span><span class="sxs-lookup"><span data-stu-id="77b31-116">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b31-117">-이름</span><span class="sxs-lookup"><span data-stu-id="77b31-117">-Name</span></span>
<span data-ttu-id="77b31-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b31-119">-ResourceGroupName</span></span>
<span data-ttu-id="77b31-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-120">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b31-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="77b31-121">-VirtualMachine</span></span>
<span data-ttu-id="77b31-122">가상 컴퓨터.</span><span class="sxs-lookup"><span data-stu-id="77b31-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b31-123">-확인</span><span class="sxs-lookup"><span data-stu-id="77b31-123">-Confirm</span></span>
<span data-ttu-id="77b31-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77b31-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77b31-125">-WhatIf</span></span>
<span data-ttu-id="77b31-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77b31-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77b31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b31-128">CommonParameters</span></span>
<span data-ttu-id="77b31-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77b31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b31-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77b31-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b31-131">입력</span><span class="sxs-lookup"><span data-stu-id="77b31-131">INPUTS</span></span>

### <span data-ttu-id="77b31-132">않아야</span><span class="sxs-lookup"><span data-stu-id="77b31-132">None</span></span>

## <span data-ttu-id="77b31-133">출력</span><span class="sxs-lookup"><span data-stu-id="77b31-133">OUTPUTS</span></span>

### <span data-ttu-id="77b31-134">JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="77b31-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="77b31-135">상속자</span><span class="sxs-lookup"><span data-stu-id="77b31-135">NOTES</span></span>

## <span data-ttu-id="77b31-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77b31-136">RELATED LINKS</span></span>