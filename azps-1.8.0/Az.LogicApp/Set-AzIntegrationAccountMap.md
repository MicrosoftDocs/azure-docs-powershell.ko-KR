---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: e2a66eef93d2ed59f78e492cac7fa7fac4dd0244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867606"
---
# <span data-ttu-id="b9e10-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9e10-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="b9e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e10-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e10-103">통합 계정 맵을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="b9e10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9e10-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9e10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b9e10-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e10-106">**Set-AzIntegrationAccountMap** cmdlet은 통합 계정 맵을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="b9e10-107">이 cmdlet은 통합 계정 맵을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="b9e10-108">통합 계정 이름, 리소스 그룹 이름 및 지도 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="b9e10-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b9e10-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b9e10-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b9e10-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b9e10-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b9e10-113">EXAMPLES</span></span>

### <span data-ttu-id="b9e10-114">예제 1: 통합 계정 맵 수정</span><span class="sxs-lookup"><span data-stu-id="b9e10-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="b9e10-115">이 명령은 지정 된 리소스 그룹의 통합 계정 맵을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="b9e10-116">명령은 이전 명령에 의해 $MapContent 변수에 저장 된 지도 정의를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="b9e10-117">변수</span><span class="sxs-lookup"><span data-stu-id="b9e10-117">PARAMETERS</span></span>

### <span data-ttu-id="b9e10-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b9e10-118">-ContentType</span></span>
<span data-ttu-id="b9e10-119">통합 계정 맵의 콘텐츠 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="b9e10-120">이 cmdlet은 응용 프로그램/xml을 맵 콘텐츠 형식으로 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="b9e10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e10-121">-DefaultProfile</span></span>
<span data-ttu-id="b9e10-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b9e10-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9e10-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b9e10-123">-Force</span></span>
<span data-ttu-id="b9e10-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9e10-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="b9e10-125">-MapDefinition</span></span>
<span data-ttu-id="b9e10-126">통합 계정 맵에 대 한 정의 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="b9e10-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="b9e10-127">-MapFilePath</span></span>
<span data-ttu-id="b9e10-128">통합 계정 맵에 대 한 정의의 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="b9e10-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="b9e10-129">-MapName</span></span>
<span data-ttu-id="b9e10-130">통합 계정 맵의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-130">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="b9e10-131">-MapType</span></span>
<span data-ttu-id="b9e10-132">통합 계정 맵의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="b9e10-133">이 cmdlet은 지도 형식으로 Xslt를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b9e10-134">-Metadata</span></span>
<span data-ttu-id="b9e10-135">지도에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-135">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-136">-이름</span><span class="sxs-lookup"><span data-stu-id="b9e10-136">-Name</span></span>
<span data-ttu-id="b9e10-137">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-137">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e10-138">-ResourceGroupName</span></span>
<span data-ttu-id="b9e10-139">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-139">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-140">-확인</span><span class="sxs-lookup"><span data-stu-id="b9e10-140">-Confirm</span></span>
<span data-ttu-id="b9e10-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e10-142">-WhatIf</span></span>
<span data-ttu-id="b9e10-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e10-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e10-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e10-145">CommonParameters</span></span>
<span data-ttu-id="b9e10-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e10-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e10-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e10-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e10-148">입력</span><span class="sxs-lookup"><span data-stu-id="b9e10-148">INPUTS</span></span>

### <span data-ttu-id="b9e10-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b9e10-149">System.String</span></span>

## <span data-ttu-id="b9e10-150">출력</span><span class="sxs-lookup"><span data-stu-id="b9e10-150">OUTPUTS</span></span>

### <span data-ttu-id="b9e10-151">IntegrationAccountMap를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="b9e10-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b9e10-152">상속자</span><span class="sxs-lookup"><span data-stu-id="b9e10-152">NOTES</span></span>

## <span data-ttu-id="b9e10-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9e10-153">RELATED LINKS</span></span>

[<span data-ttu-id="b9e10-154">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9e10-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="b9e10-155">새로운 AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9e10-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="b9e10-156">제거-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9e10-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

