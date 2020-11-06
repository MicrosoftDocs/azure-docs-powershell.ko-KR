---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/test-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: 35ce8352670aa2af2a7051736e1b986b83bcc64b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530938"
---
# <span data-ttu-id="d6b3a-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d6b3a-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="d6b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b3a-103">논리 앱 정의의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6b3a-104">SYNTAX</span></span>

### <span data-ttu-id="d6b3a-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b3a-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6b3a-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b3a-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b3a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d6b3a-107">DESCRIPTION</span></span>
<span data-ttu-id="d6b3a-108">**테스트 AzureRmLogicApp** cmdlet은 리소스 그룹의 논리 앱 정의에 대 한 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="d6b3a-109">논리 앱 이름, 리소스 그룹 이름, 위치, 상태, 통합 계정 ID 또는 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="d6b3a-110">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d6b3a-111">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d6b3a-112">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d6b3a-113">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d6b3a-114">예제의</span><span class="sxs-lookup"><span data-stu-id="d6b3a-114">EXAMPLES</span></span>

### <span data-ttu-id="d6b3a-115">예제 1: 파일 경로를 사용 하 여 논리 앱 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="d6b3a-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="d6b3a-116">이 명령은 지정 된 리소스 그룹에서 LogicApp01 이라는 논리 앱의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="d6b3a-117">명령은 정의 및 매개 변수 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="d6b3a-118">예제 2: 개체를 사용 하 여 논리 앱 유효성 검사</span><span class="sxs-lookup"><span data-stu-id="d6b3a-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="d6b3a-119">이 명령은 지정 된 리소스 그룹에서 LogicApp01 이라는 논리 앱의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="d6b3a-120">명령에서 정의 및 매개 변수 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="d6b3a-121">변수</span><span class="sxs-lookup"><span data-stu-id="d6b3a-121">PARAMETERS</span></span>

### <span data-ttu-id="d6b3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b3a-122">-DefaultProfile</span></span>
<span data-ttu-id="d6b3a-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d6b3a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6b3a-124">-정의</span><span class="sxs-lookup"><span data-stu-id="d6b3a-124">-Definition</span></span>
<span data-ttu-id="d6b3a-125">논리 앱의 정의를 개체 또는 JSON (JavaScript 개체 표시법) 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b3a-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="d6b3a-126">-DefinitionFilePath</span></span>
<span data-ttu-id="d6b3a-127">논리 앱의 정의를 JSON 형식의 정의 파일 경로로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b3a-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="d6b3a-128">-IntegrationAccountId</span></span>
<span data-ttu-id="d6b3a-129">논리 앱의 통합 계정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="d6b3a-130">-위치</span><span class="sxs-lookup"><span data-stu-id="d6b3a-130">-Location</span></span>
<span data-ttu-id="d6b3a-131">논리 앱의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="d6b3a-132">Azure 데이터 센터 위치 (예: 서쪽 미국 또는 동남 아시아)를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="d6b3a-133">임의의 위치에 논리 앱을 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="d6b3a-134">-이름</span><span class="sxs-lookup"><span data-stu-id="d6b3a-134">-Name</span></span>
<span data-ttu-id="d6b3a-135">논리 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-135">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b3a-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="d6b3a-136">-ParameterFilePath</span></span>
<span data-ttu-id="d6b3a-137">JSON 형식의 매개 변수 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="d6b3a-138">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="d6b3a-138">-Parameters</span></span>
<span data-ttu-id="d6b3a-139">논리 앱의 parameters 컬렉션 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="d6b3a-140">해시 테이블, 사전 \<string\> 또는 사전을 지정 \<string, WorkflowParameter\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="d6b3a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b3a-141">-ResourceGroupName</span></span>
<span data-ttu-id="d6b3a-142">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d6b3a-143">-상태</span><span class="sxs-lookup"><span data-stu-id="d6b3a-143">-State</span></span>
<span data-ttu-id="d6b3a-144">논리 앱의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="d6b3a-145">이 매개 변수에 허용 되는 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b3a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b3a-146">CommonParameters</span></span>
<span data-ttu-id="d6b3a-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6b3a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b3a-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b3a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b3a-149">입력</span><span class="sxs-lookup"><span data-stu-id="d6b3a-149">INPUTS</span></span>

### <span data-ttu-id="d6b3a-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6b3a-150">System.String</span></span>

## <span data-ttu-id="d6b3a-151">출력</span><span class="sxs-lookup"><span data-stu-id="d6b3a-151">OUTPUTS</span></span>

### <span data-ttu-id="d6b3a-152">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d6b3a-152">System.Void</span></span>

## <span data-ttu-id="d6b3a-153">상속자</span><span class="sxs-lookup"><span data-stu-id="d6b3a-153">NOTES</span></span>

## <span data-ttu-id="d6b3a-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6b3a-154">RELATED LINKS</span></span>

[<span data-ttu-id="d6b3a-155">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d6b3a-155">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="d6b3a-156">새로운 AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d6b3a-156">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="d6b3a-157">제거-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d6b3a-157">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="d6b3a-158">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d6b3a-158">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="d6b3a-159">시작-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d6b3a-159">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

