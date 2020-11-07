---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3d6a5488e7e101c904e90d056c8b2ffc03e786fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876366"
---
# <span data-ttu-id="fbc9e-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="fbc9e-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="fbc9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc9e-103">관리 되는 응용 프로그램 정의 업데이트</span><span class="sxs-lookup"><span data-stu-id="fbc9e-103">Updates managed application definition</span></span>

## <span data-ttu-id="fbc9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbc9e-104">SYNTAX</span></span>

### <span data-ttu-id="fbc9e-105">SetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="fbc9e-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbc9e-106">SetById</span><span class="sxs-lookup"><span data-stu-id="fbc9e-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbc9e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fbc9e-107">DESCRIPTION</span></span>
<span data-ttu-id="fbc9e-108">**AzManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="fbc9e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fbc9e-109">EXAMPLES</span></span>

### <span data-ttu-id="fbc9e-110">예제 1: 관리 되는 응용 프로그램 정의 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="fbc9e-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="fbc9e-111">이 명령은 관리 되는 응용 프로그램 정의 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="fbc9e-112">변수</span><span class="sxs-lookup"><span data-stu-id="fbc9e-112">PARAMETERS</span></span>

### <span data-ttu-id="fbc9e-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fbc9e-113">-ApiVersion</span></span>
<span data-ttu-id="fbc9e-114">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fbc9e-115">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fbc9e-116">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="fbc9e-116">-Authorization</span></span>
<span data-ttu-id="fbc9e-117">관리 되는 응용 프로그램 정의 권한 부여입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-117">The managed application definition authorization.</span></span>
<span data-ttu-id="fbc9e-118">\<Principalid \> : \< roleDefinitionId의 형식으로 쉼표로 구분 된 인증 쌍\></span><span class="sxs-lookup"><span data-stu-id="fbc9e-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc9e-119">-DefaultProfile</span></span>
<span data-ttu-id="fbc9e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-121">-설명</span><span class="sxs-lookup"><span data-stu-id="fbc9e-121">-Description</span></span>
<span data-ttu-id="fbc9e-122">관리 되는 응용 프로그램 정의 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fbc9e-123">-DisplayName</span></span>
<span data-ttu-id="fbc9e-124">관리 되는 응용 프로그램 정의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-125">-Id</span><span class="sxs-lookup"><span data-stu-id="fbc9e-125">-Id</span></span>
<span data-ttu-id="fbc9e-126">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="fbc9e-127">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc9e-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-128">-이름</span><span class="sxs-lookup"><span data-stu-id="fbc9e-128">-Name</span></span>
<span data-ttu-id="fbc9e-129">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="fbc9e-130">-PackageFileUri</span></span>
<span data-ttu-id="fbc9e-131">관리 되는 응용 프로그램 정의 패키지 파일 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-131">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="fbc9e-132">-Pre</span></span>
<span data-ttu-id="fbc9e-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fbc9e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc9e-134">-ResourceGroupName</span></span>
<span data-ttu-id="fbc9e-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-136">태그</span><span class="sxs-lookup"><span data-stu-id="fbc9e-136">-Tag</span></span>
<span data-ttu-id="fbc9e-137">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc9e-138">-확인</span><span class="sxs-lookup"><span data-stu-id="fbc9e-138">-Confirm</span></span>
<span data-ttu-id="fbc9e-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc9e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc9e-140">-WhatIf</span></span>
<span data-ttu-id="fbc9e-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbc9e-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc9e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc9e-143">CommonParameters</span></span>
<span data-ttu-id="fbc9e-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbc9e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc9e-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc9e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc9e-146">입력</span><span class="sxs-lookup"><span data-stu-id="fbc9e-146">INPUTS</span></span>

### <span data-ttu-id="fbc9e-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fbc9e-147">System.String</span></span>

### <span data-ttu-id="fbc9e-148">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="fbc9e-148">System.String[]</span></span>

### <span data-ttu-id="fbc9e-149">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="fbc9e-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fbc9e-150">출력</span><span class="sxs-lookup"><span data-stu-id="fbc9e-150">OUTPUTS</span></span>

### <span data-ttu-id="fbc9e-151">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="fbc9e-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fbc9e-152">상속자</span><span class="sxs-lookup"><span data-stu-id="fbc9e-152">NOTES</span></span>

## <span data-ttu-id="fbc9e-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbc9e-153">RELATED LINKS</span></span>