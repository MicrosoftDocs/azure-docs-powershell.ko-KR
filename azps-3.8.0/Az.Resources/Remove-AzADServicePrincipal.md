---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 33eecc20ce11b23953c359e5c8de653cefcaf929
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878082"
---
# <span data-ttu-id="0c7e8-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c7e8-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="0c7e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7e8-103">Azure active directory 서비스 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="0c7e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c7e8-104">SYNTAX</span></span>

### <span data-ttu-id="0c7e8-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c7e8-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7e8-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7e8-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7e8-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7e8-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7e8-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7e8-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7e8-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7e8-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7e8-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c7e8-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c7e8-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0c7e8-111">DESCRIPTION</span></span>
<span data-ttu-id="0c7e8-112">Azure active directory 서비스 사용자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="0c7e8-113">예제의</span><span class="sxs-lookup"><span data-stu-id="0c7e8-113">EXAMPLES</span></span>

### <span data-ttu-id="0c7e8-114">예제 1-개체 id 별 서비스 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0c7e8-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="0c7e8-115">개체 id가 ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' 인 서비스 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="0c7e8-116">예제 2-응용 프로그램 id로 서비스 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0c7e8-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="0c7e8-117">응용 프로그램 id가 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 인 서비스 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="0c7e8-118">예제 3-SPN에서 서비스 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0c7e8-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="0c7e8-119">서비스 사용자 이름이 "MyServicePrincipal" 인 서비스 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="0c7e8-120">예제 4-파이핑을 통해 서비스 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0c7e8-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="0c7e8-121">개체 id가 ' 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 ' 인 서비스 사용자를 가져오고 해당 서비스 사용자를 제거 하기 위해 Remove-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="0c7e8-122">예제 5-응용 프로그램을 파이핑 하 여 서비스 사용자 제거</span><span class="sxs-lookup"><span data-stu-id="0c7e8-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="0c7e8-123">응용 프로그램 id가 ' 9263469e-d328-4321-8646-3e3e75d20e76 ' 인 응용 프로그램을 가져오고 해당 응용 프로그램과 연결 된 서비스 사용자를 제거 하기 위해 Remove-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="0c7e8-124">변수</span><span class="sxs-lookup"><span data-stu-id="0c7e8-124">PARAMETERS</span></span>

### <span data-ttu-id="0c7e8-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0c7e8-125">-ApplicationId</span></span>
<span data-ttu-id="0c7e8-126">서비스 사용자 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e8-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0c7e8-127">-ApplicationObject</span></span>
<span data-ttu-id="0c7e8-128">서비스 사용자가 제거 되 고 있는 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7e8-129">-DefaultProfile</span></span>
<span data-ttu-id="0c7e8-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c7e8-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c7e8-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c7e8-131">-DisplayName</span></span>
<span data-ttu-id="0c7e8-132">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e8-133">-Force</span><span class="sxs-lookup"><span data-stu-id="0c7e8-133">-Force</span></span>
<span data-ttu-id="0c7e8-134">확인 하지 않고 서비스 사용자 삭제로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="0c7e8-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c7e8-135">-InputObject</span></span>
<span data-ttu-id="0c7e8-136">서비스 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e8-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0c7e8-137">-ObjectId</span></span>
<span data-ttu-id="0c7e8-138">삭제할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e8-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c7e8-139">-PassThru</span></span>
<span data-ttu-id="0c7e8-140">지정 된 경우 삭제 된 서비스 사용자를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="0c7e8-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0c7e8-141">-ServicePrincipalName</span></span>
<span data-ttu-id="0c7e8-142">서비스 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e8-143">-확인</span><span class="sxs-lookup"><span data-stu-id="0c7e8-143">-Confirm</span></span>
<span data-ttu-id="0c7e8-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7e8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7e8-145">-WhatIf</span></span>
<span data-ttu-id="0c7e8-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7e8-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c7e8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7e8-148">CommonParameters</span></span>
<span data-ttu-id="0c7e8-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7e8-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c7e8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7e8-151">입력</span><span class="sxs-lookup"><span data-stu-id="0c7e8-151">INPUTS</span></span>

### <span data-ttu-id="0c7e8-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c7e8-152">System.String</span></span>

### <span data-ttu-id="0c7e8-153">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="0c7e8-153">System.Guid</span></span>

### <span data-ttu-id="0c7e8-154">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c7e8-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="0c7e8-155">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="0c7e8-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="0c7e8-156">출력</span><span class="sxs-lookup"><span data-stu-id="0c7e8-156">OUTPUTS</span></span>

### <span data-ttu-id="0c7e8-157">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c7e8-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="0c7e8-158">상속자</span><span class="sxs-lookup"><span data-stu-id="0c7e8-158">NOTES</span></span>
<span data-ttu-id="0c7e8-159">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="0c7e8-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0c7e8-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c7e8-160">RELATED LINKS</span></span>

[<span data-ttu-id="0c7e8-161">새로운 AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c7e8-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="0c7e8-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c7e8-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="0c7e8-163">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0c7e8-163">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="0c7e8-164">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0c7e8-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="0c7e8-165">제거-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0c7e8-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)