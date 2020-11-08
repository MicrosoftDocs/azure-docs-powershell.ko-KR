---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044204"
---
# <span data-ttu-id="9f5c3-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9f5c3-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="9f5c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5c3-103">사용자가 할당 한 Id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="9f5c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f5c3-104">SYNTAX</span></span>

### <span data-ttu-id="9f5c3-105">ResourceGroupAndNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f5c3-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5c3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5c3-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5c3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f5c3-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f5c3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9f5c3-108">DESCRIPTION</span></span>
<span data-ttu-id="9f5c3-109">**제거-AzUserAssignedIdentity** 에서 지정 된 사용자가 할당 한 id를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="9f5c3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9f5c3-110">EXAMPLES</span></span>

### <span data-ttu-id="9f5c3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f5c3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="9f5c3-112">이 예제 cmdlet은 리소스 그룹 **Psrg** 에서 id **ID1** 를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="9f5c3-113">False</span><span class="sxs-lookup"><span data-stu-id="9f5c3-113">True</span></span>

## <span data-ttu-id="9f5c3-114">변수</span><span class="sxs-lookup"><span data-stu-id="9f5c3-114">PARAMETERS</span></span>

### <span data-ttu-id="9f5c3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f5c3-115">-AsJob</span></span>
<span data-ttu-id="9f5c3-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9f5c3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f5c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5c3-117">-DefaultProfile</span></span>
<span data-ttu-id="9f5c3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5c3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9f5c3-119">-Force</span></span>
<span data-ttu-id="9f5c3-120">{{Force 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="9f5c3-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="9f5c3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f5c3-121">-InputObject</span></span>
<span data-ttu-id="9f5c3-122">Id 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5c3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9f5c3-123">-Name</span></span>
<span data-ttu-id="9f5c3-124">Id 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f5c3-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5c3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f5c3-127">-ResourceId</span></span>
<span data-ttu-id="9f5c3-128">Id의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5c3-129">-확인</span><span class="sxs-lookup"><span data-stu-id="9f5c3-129">-Confirm</span></span>
<span data-ttu-id="9f5c3-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f5c3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f5c3-131">-WhatIf</span></span>
<span data-ttu-id="9f5c3-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f5c3-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f5c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5c3-134">CommonParameters</span></span>
<span data-ttu-id="9f5c3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5c3-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5c3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5c3-137">입력</span><span class="sxs-lookup"><span data-stu-id="9f5c3-137">INPUTS</span></span>

### <span data-ttu-id="9f5c3-138">ManagedServiceIdentity. PsUserAssignedIdentity/.</span><span class="sxs-lookup"><span data-stu-id="9f5c3-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="9f5c3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f5c3-139">System.String</span></span>

## <span data-ttu-id="9f5c3-140">출력</span><span class="sxs-lookup"><span data-stu-id="9f5c3-140">OUTPUTS</span></span>

### <span data-ttu-id="9f5c3-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9f5c3-141">System.Boolean</span></span>

## <span data-ttu-id="9f5c3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9f5c3-142">NOTES</span></span>

## <span data-ttu-id="9f5c3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f5c3-143">RELATED LINKS</span></span>