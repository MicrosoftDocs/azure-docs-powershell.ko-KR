---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535444"
---
# <span data-ttu-id="1d689-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="1d689-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="1d689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d689-102">SYNOPSIS</span></span>
<span data-ttu-id="1d689-103">관리 되는 응용 프로그램 정의 제거</span><span class="sxs-lookup"><span data-stu-id="1d689-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d689-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d689-104">SYNTAX</span></span>

### <span data-ttu-id="1d689-105">관리 되는 응용 프로그램 정의 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="1d689-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="1d689-106">기본값</span><span class="sxs-lookup"><span data-stu-id="1d689-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d689-107">관리 되는 응용 프로그램 정의 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="1d689-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d689-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1d689-108">DESCRIPTION</span></span>
<span data-ttu-id="1d689-109">**Remove-AzureRmManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="1d689-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1d689-110">EXAMPLES</span></span>

### <span data-ttu-id="1d689-111">예제 1: 리소스 ID 별 관리 되는 응용 프로그램 정의 제거</span><span class="sxs-lookup"><span data-stu-id="1d689-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="1d689-112">첫 번째 명령은 Get-AzureRmManagedApplicationDefinition cmdlet을 사용 하 여 myAppDef 이라는 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="1d689-113">명령이 $ApplicationDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="1d689-114">두 번째 명령은 $ApplicationDefinition의 **ResourceId** 속성으로 식별 되는 관리 되는 응용 프로그램 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="1d689-115">변수</span><span class="sxs-lookup"><span data-stu-id="1d689-115">PARAMETERS</span></span>

### <span data-ttu-id="1d689-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1d689-116">-ApiVersion</span></span>
<span data-ttu-id="1d689-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1d689-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d689-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d689-119">-DefaultProfile</span></span>
<span data-ttu-id="1d689-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d689-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1d689-121">-Force</span></span>
<span data-ttu-id="1d689-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1d689-123">-Id</span><span class="sxs-lookup"><span data-stu-id="1d689-123">-Id</span></span>
<span data-ttu-id="1d689-124">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="1d689-125">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1d689-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d689-126">-이름</span><span class="sxs-lookup"><span data-stu-id="1d689-126">-Name</span></span>
<span data-ttu-id="1d689-127">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d689-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="1d689-128">-Pre</span></span>
<span data-ttu-id="1d689-129">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1d689-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d689-130">-ResourceGroupName</span></span>
<span data-ttu-id="1d689-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d689-132">-확인</span><span class="sxs-lookup"><span data-stu-id="1d689-132">-Confirm</span></span>
<span data-ttu-id="1d689-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d689-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d689-134">-WhatIf</span></span>
<span data-ttu-id="1d689-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d689-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d689-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d689-137">CommonParameters</span></span>
<span data-ttu-id="1d689-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d689-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d689-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d689-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d689-140">입력</span><span class="sxs-lookup"><span data-stu-id="1d689-140">INPUTS</span></span>

### <span data-ttu-id="1d689-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1d689-141">System.String</span></span>

## <span data-ttu-id="1d689-142">출력</span><span class="sxs-lookup"><span data-stu-id="1d689-142">OUTPUTS</span></span>

### <span data-ttu-id="1d689-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1d689-143">System.Boolean</span></span>

## <span data-ttu-id="1d689-144">상속자</span><span class="sxs-lookup"><span data-stu-id="1d689-144">NOTES</span></span>

## <span data-ttu-id="1d689-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d689-145">RELATED LINKS</span></span>
