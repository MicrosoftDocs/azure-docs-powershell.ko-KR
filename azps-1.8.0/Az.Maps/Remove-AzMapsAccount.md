---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: ba474ca3ea3a975262eec8b98df1fb99b0f336cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867441"
---
# <span data-ttu-id="358b5-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="358b5-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="358b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="358b5-102">SYNOPSIS</span></span>
<span data-ttu-id="358b5-103">Azure Maps 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="358b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="358b5-104">SYNTAX</span></span>

### <span data-ttu-id="358b5-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="358b5-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358b5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="358b5-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358b5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="358b5-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358b5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="358b5-108">DESCRIPTION</span></span>
<span data-ttu-id="358b5-109">Remove-AzMapsAccount cmdlet은 지정 된 Azure Maps 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="358b5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="358b5-110">EXAMPLES</span></span>

### <span data-ttu-id="358b5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="358b5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="358b5-112">리소스 그룹 MyResourceGroup에서 계정 내 계정를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="358b5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="358b5-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="358b5-114">지정 된 Azure Maps 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="358b5-115">변수</span><span class="sxs-lookup"><span data-stu-id="358b5-115">PARAMETERS</span></span>

### <span data-ttu-id="358b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358b5-116">-DefaultProfile</span></span>
<span data-ttu-id="358b5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="358b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="358b5-118">-InputObject</span></span>
<span data-ttu-id="358b5-119">AzMapsAccount에서 파이프 맵 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="358b5-120">-이름</span><span class="sxs-lookup"><span data-stu-id="358b5-120">-Name</span></span>
<span data-ttu-id="358b5-121">계정 이름을 매핑합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358b5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="358b5-122">-PassThru</span></span>
<span data-ttu-id="358b5-123">지정 된 계정이 성공적으로 삭제 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="358b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="358b5-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="358b5-126">-ResourceId</span></span>
<span data-ttu-id="358b5-127">Maps 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="358b5-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358b5-128">-확인</span><span class="sxs-lookup"><span data-stu-id="358b5-128">-Confirm</span></span>
<span data-ttu-id="358b5-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358b5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358b5-130">-WhatIf</span></span>
<span data-ttu-id="358b5-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358b5-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358b5-133">CommonParameters</span></span>
<span data-ttu-id="358b5-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="358b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358b5-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358b5-136">입력</span><span class="sxs-lookup"><span data-stu-id="358b5-136">INPUTS</span></span>

### <span data-ttu-id="358b5-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="358b5-137">System.String</span></span>

### <span data-ttu-id="358b5-138">Microsoft Azure. \*. \*. \*.</span><span class="sxs-lookup"><span data-stu-id="358b5-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="358b5-139">출력</span><span class="sxs-lookup"><span data-stu-id="358b5-139">OUTPUTS</span></span>

### <span data-ttu-id="358b5-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="358b5-140">System.Boolean</span></span>

## <span data-ttu-id="358b5-141">상속자</span><span class="sxs-lookup"><span data-stu-id="358b5-141">NOTES</span></span>

## <span data-ttu-id="358b5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="358b5-142">RELATED LINKS</span></span>