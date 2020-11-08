---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041703"
---
# <span data-ttu-id="180e0-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="180e0-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="180e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="180e0-102">SYNOPSIS</span></span>
<span data-ttu-id="180e0-103">리소스 그룹 배포의 유효성을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="180e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="180e0-104">SYNTAX</span></span>

### <span data-ttu-id="180e0-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="180e0-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="180e0-106">By서식 Objectandparameterobject</span><span class="sxs-lookup"><span data-stu-id="180e0-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-107">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="180e0-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-108">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="180e0-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-109">By서식 Objectandparameterfile</span><span class="sxs-lookup"><span data-stu-id="180e0-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-110">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="180e0-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-111">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="180e0-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-112">By서식 Objectandparameteruri</span><span class="sxs-lookup"><span data-stu-id="180e0-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-113">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="180e0-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-114">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="180e0-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="180e0-115">By서식 Objectwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="180e0-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="180e0-116">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="180e0-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="180e0-117">설명은</span><span class="sxs-lookup"><span data-stu-id="180e0-117">DESCRIPTION</span></span>
<span data-ttu-id="180e0-118">**AzResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 템플릿과 해당 매개 변수 값이 유효한 지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="180e0-119">예제의</span><span class="sxs-lookup"><span data-stu-id="180e0-119">EXAMPLES</span></span>

### <span data-ttu-id="180e0-120">예제 1: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용 하 여 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="180e0-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="180e0-121">이 명령은 지정 된 템플릿 파일과 매개 변수 파일에서 만든 메모리 내 해시 테이블을 사용 하 여 지정 된 리소스 그룹의 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="180e0-122">예제 2: 템플릿 파일 및 매개 변수 개체를 통한 배포 테스트</span><span class="sxs-lookup"><span data-stu-id="180e0-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="180e0-123">이 명령은 제공 된 템플릿 파일과 매개 변수 파일을 사용 하 여 지정 된 리소스 그룹 및 리소스에서 배포를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="180e0-124">변수</span><span class="sxs-lookup"><span data-stu-id="180e0-124">PARAMETERS</span></span>

### <span data-ttu-id="180e0-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="180e0-125">-ApiVersion</span></span>
<span data-ttu-id="180e0-126">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="180e0-127">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="180e0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180e0-128">-DefaultProfile</span></span>
<span data-ttu-id="180e0-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="180e0-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="180e0-130">-모드</span><span class="sxs-lookup"><span data-stu-id="180e0-130">-Mode</span></span>
<span data-ttu-id="180e0-131">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="180e0-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="180e0-133">진행</span><span class="sxs-lookup"><span data-stu-id="180e0-133">Incremental</span></span>
- <span data-ttu-id="180e0-134">마칠</span><span class="sxs-lookup"><span data-stu-id="180e0-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="180e0-135">-Pre</span></span>
<span data-ttu-id="180e0-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="180e0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="180e0-137">-ResourceGroupName</span></span>
<span data-ttu-id="180e0-138">테스트할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="180e0-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="180e0-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="180e0-140">-RollbackToLastDeployment가 사용 되는 경우 리소스 그룹에서 지정 된 이름을 사용 하 여 성공한 배포로 롤백할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="180e0-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="180e0-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="180e0-142">-RollBackDeploymentName가 사용 되는 경우 리소스 그룹에서 마지막으로 성공한 배포에 롤백하는 것으로 표시 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="180e0-143">-Skip서식 Parameterprompt</span><span class="sxs-lookup"><span data-stu-id="180e0-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="180e0-144">제공 된 템플릿 매개 변수에 템플릿에서 사용 되는 필요한 모든 매개 변수가 포함 되어 있는지 확인 하는 PowerShell 동적 매개 변수 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="180e0-145">이 검사는 누락 된 매개 변수에 대해 사용자에 게 값을 제공 하 라는 메시지를 표시 하지만-Skiptemplate Parameterprompt는이 프롬프트를 무시 하 고 매개 변수를 템플릿에 바인딩하지 않은 경우 즉시 오류를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="180e0-146">비 대화형 스크립트의 경우-Skip비템플릿 Parameterprompt를 제공 하 여 필요한 모든 매개 변수가 충족 되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="180e0-147">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="180e0-147">-TemplateFile</span></span>
<span data-ttu-id="180e0-148">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-148">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-149">-서식 개체</span><span class="sxs-lookup"><span data-stu-id="180e0-149">-TemplateObject</span></span>
<span data-ttu-id="180e0-150">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-150">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-151">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="180e0-151">-TemplateParameterFile</span></span>
<span data-ttu-id="180e0-152">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-153">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="180e0-153">-TemplateParameterObject</span></span>
<span data-ttu-id="180e0-154">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-154">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-155">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="180e0-155">-TemplateParameterUri</span></span>
<span data-ttu-id="180e0-156">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-156">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-157">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="180e0-157">-TemplateUri</span></span>
<span data-ttu-id="180e0-158">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-158">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="180e0-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180e0-159">CommonParameters</span></span>
<span data-ttu-id="180e0-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180e0-161">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="180e0-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180e0-162">입력</span><span class="sxs-lookup"><span data-stu-id="180e0-162">INPUTS</span></span>

### <span data-ttu-id="180e0-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="180e0-163">System.String</span></span>

### <span data-ttu-id="180e0-164">DeploymentMode를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="180e0-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="180e0-165">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="180e0-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="180e0-166">출력</span><span class="sxs-lookup"><span data-stu-id="180e0-166">OUTPUTS</span></span>

### <span data-ttu-id="180e0-167">SdkModels. PSResourceManagerError에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="180e0-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="180e0-168">상속자</span><span class="sxs-lookup"><span data-stu-id="180e0-168">NOTES</span></span>

## <span data-ttu-id="180e0-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="180e0-169">RELATED LINKS</span></span>

[<span data-ttu-id="180e0-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="180e0-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="180e0-171">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="180e0-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="180e0-172">제거-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="180e0-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="180e0-173">중지-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="180e0-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

