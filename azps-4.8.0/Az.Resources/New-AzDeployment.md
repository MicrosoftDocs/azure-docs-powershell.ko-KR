---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 56be1071c2a6307bee28f0ce4cf13dde626df72e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047664"
---
# <span data-ttu-id="16fac-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="16fac-101">New-AzDeployment</span></span>

## <span data-ttu-id="16fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16fac-102">SYNOPSIS</span></span>
<span data-ttu-id="16fac-103">배포 만들기</span><span class="sxs-lookup"><span data-stu-id="16fac-103">Create a deployment</span></span>

## <span data-ttu-id="16fac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16fac-104">SYNTAX</span></span>

### <span data-ttu-id="16fac-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="16fac-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fac-106">By서식 Objectandparameterobject</span><span class="sxs-lookup"><span data-stu-id="16fac-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16fac-107">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="16fac-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16fac-108">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="16fac-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16fac-109">By서식 Objectandparameterfile</span><span class="sxs-lookup"><span data-stu-id="16fac-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16fac-110">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="16fac-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fac-111">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="16fac-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fac-112">By서식 Objectandparameteruri</span><span class="sxs-lookup"><span data-stu-id="16fac-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16fac-113">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="16fac-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fac-114">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="16fac-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fac-115">By서식 Objectwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="16fac-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fac-116">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="16fac-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16fac-117">설명은</span><span class="sxs-lookup"><span data-stu-id="16fac-117">DESCRIPTION</span></span>
<span data-ttu-id="16fac-118">**새 AzDeployment** cmdlet은 현재 구독 범위에 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="16fac-119">여기에는 배포에 필요한 리소스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="16fac-120">Azure 리소스는 사용자가 관리 하는 Azure 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="16fac-121">리소스는 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 컴퓨터 또는 저장소 계정과 같은 리소스 그룹에 살고 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="16fac-122">또는 역할 정의, 정책 정의 등과 같은 구독 수준 리소스 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="16fac-123">리소스 그룹에 리소스를 추가 하려면 리소스 그룹에 배포를 만드는 **New AzResourceGroupDeployment** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="16fac-124">**AzDeployment** cmdlet은 구독 수준 리소스를 배포 하는 현재 구독 범위에서 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="16fac-125">구독에서 배포를 추가 하려면 위치 및 템플릿을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="16fac-126">위치는 Azure 리소스 관리자에 배포 데이터를 저장할 위치를 알려 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="16fac-127">템플릿은 배포할 개별 리소스를 포함 하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="16fac-128">이 템플릿에는 필수 리소스 및 구성 가능한 속성 값 (예: 이름 및 크기)에 대 한 매개 변수 자리 표시 자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="16fac-129">배포에 사용자 지정 서식 파일을 사용 하려면 *서식 파일 file* 매개 변수 또는 template *uri* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="16fac-130">각 템플릿에는 구성 가능한 속성에 대 한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="16fac-131">서식 파일 매개 변수에 대 한 값을 지정 하려면 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="16fac-132">또는 템플릿을 지정할 때 명령에 동적으로 추가 되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="16fac-133">동적 매개 변수를 사용 하려면 명령 프롬프트에 입력 하거나 빼기 기호 (-)를 입력 하 여 매개 변수를 나타내고 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="16fac-134">명령 프롬프트에서 입력 하는 템플릿 매개 변수 값은 template 매개 변수 개체 또는 파일의 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="16fac-135">예제의</span><span class="sxs-lookup"><span data-stu-id="16fac-135">EXAMPLES</span></span>

### <span data-ttu-id="16fac-136">예제 1: 사용자 지정 서식 파일 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="16fac-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="16fac-137">이 명령은 정의 된 태그 매개 변수를 사용 하 여 사용자 지정 서식 파일과 디스크의 서식 파일을 사용 하 여 현재 구독 범위에서 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="16fac-138">이 명령은 template *파일* 매개 변수를 사용 하 여 템플릿과 매개 변수 값이 포함 된 파일을 지정 하는 서식 파일과 템플릿 매개 변수 *파일* 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="16fac-139">서식 파일 *버전* 매개 변수를 사용 하 여 템플릿의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="16fac-140">예제 2: 사용자 지정 템플릿 개체 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="16fac-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="16fac-141">이 명령은 메모리 내 hashtable로 변환 된 사용자 지정 서식 파일과 디스크의 템플릿 파일을 사용 하 여 현재 구독 범위에서 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="16fac-142">처음 두 명령은 디스크의 템플릿 파일에 대 한 텍스트를 읽고이를 메모리 내의 hashtable으로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="16fac-143">마지막 명령은 a a i a i a i a i a i a i a i a i a i a a i a i a i a i i a i *매개 변수를* 사용 하 여 *매개 변수*</span><span class="sxs-lookup"><span data-stu-id="16fac-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="16fac-144">서식 파일 *버전* 매개 변수를 사용 하 여 템플릿의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="16fac-145">변수</span><span class="sxs-lookup"><span data-stu-id="16fac-145">PARAMETERS</span></span>

### <span data-ttu-id="16fac-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="16fac-146">-ApiVersion</span></span>
<span data-ttu-id="16fac-147">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="16fac-148">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="16fac-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16fac-149">-AsJob</span></span>
<span data-ttu-id="16fac-150">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="16fac-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16fac-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fac-151">-DefaultProfile</span></span>
<span data-ttu-id="16fac-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16fac-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="16fac-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="16fac-154">배포 디버그 로그 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="16fac-155">-위치</span><span class="sxs-lookup"><span data-stu-id="16fac-155">-Location</span></span>
<span data-ttu-id="16fac-156">배포 데이터를 저장할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="16fac-157">-이름</span><span class="sxs-lookup"><span data-stu-id="16fac-157">-Name</span></span>
<span data-ttu-id="16fac-158">만들려는 배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-158">The name of the deployment it's going to create.</span></span> <span data-ttu-id="16fac-159">지정 하지 않으면 템플릿 파일이 제공 될 때 기본적으로 템플릿 파일 이름이 만들어집니다. 템플릿 개체가 제공 되는 현재 시간을 기본값으로 설정 합니다 (예: "20131223140835").</span><span class="sxs-lookup"><span data-stu-id="16fac-159">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fac-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="16fac-160">-Pre</span></span>
<span data-ttu-id="16fac-161">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-161">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="16fac-162">-Skip서식 Parameterprompt</span><span class="sxs-lookup"><span data-stu-id="16fac-162">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="16fac-163">제공 된 템플릿 매개 변수에 템플릿에서 사용 되는 필요한 모든 매개 변수가 포함 되어 있는지 확인 하는 PowerShell 동적 매개 변수 처리를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-163">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="16fac-164">이 검사는 누락 된 매개 변수에 대해 사용자에 게 값을 제공 하 라는 메시지를 표시 하지만-Skiptemplate Parameterprompt는이 프롬프트를 무시 하 고 매개 변수를 템플릿에 바인딩하지 않은 경우 즉시 오류를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-164">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="16fac-165">비 대화형 스크립트의 경우-Skip비템플릿 Parameterprompt를 제공 하 여 필요한 모든 매개 변수가 충족 되지 않는 경우 더 나은 오류 메시지를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-165">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="16fac-166">태그</span><span class="sxs-lookup"><span data-stu-id="16fac-166">-Tag</span></span>
<span data-ttu-id="16fac-167">배포에 포함할 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-167">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fac-168">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="16fac-168">-TemplateFile</span></span>
<span data-ttu-id="16fac-169">서식 파일에 대 한 로컬 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-169">Local path to the template file.</span></span>

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

### <span data-ttu-id="16fac-170">-서식 개체</span><span class="sxs-lookup"><span data-stu-id="16fac-170">-TemplateObject</span></span>
<span data-ttu-id="16fac-171">템플릿을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="16fac-172">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="16fac-172">-TemplateParameterFile</span></span>
<span data-ttu-id="16fac-173">템플릿 매개 변수가 있는 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-173">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="16fac-174">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="16fac-174">-TemplateParameterObject</span></span>
<span data-ttu-id="16fac-175">매개 변수를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-175">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="16fac-176">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="16fac-176">-TemplateParameterUri</span></span>
<span data-ttu-id="16fac-177">Template 매개 변수 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-177">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="16fac-178">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="16fac-178">-TemplateUri</span></span>
<span data-ttu-id="16fac-179">템플릿 파일에 대 한 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="16fac-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="16fac-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="16fac-181">What-If 결과에서 제외할 쉼표로 구분 된 리소스 변경 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="16fac-182">-WhatIf 또는-Confirm 스위치가 설정 된 경우 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fac-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="16fac-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="16fac-184">What-If 결과 서식입니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-184">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fac-185">-확인</span><span class="sxs-lookup"><span data-stu-id="16fac-185">-Confirm</span></span>
<span data-ttu-id="16fac-186">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16fac-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16fac-187">-WhatIf</span></span>
<span data-ttu-id="16fac-188">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16fac-189">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16fac-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fac-190">CommonParameters</span></span>
<span data-ttu-id="16fac-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16fac-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fac-192">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16fac-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fac-193">입력</span><span class="sxs-lookup"><span data-stu-id="16fac-193">INPUTS</span></span>

### <span data-ttu-id="16fac-194">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="16fac-194">System.Collections.Hashtable</span></span>

### <span data-ttu-id="16fac-195">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16fac-195">System.String</span></span>

## <span data-ttu-id="16fac-196">출력</span><span class="sxs-lookup"><span data-stu-id="16fac-196">OUTPUTS</span></span>

### <span data-ttu-id="16fac-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="16fac-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="16fac-198">상속자</span><span class="sxs-lookup"><span data-stu-id="16fac-198">NOTES</span></span>

## <span data-ttu-id="16fac-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16fac-199">RELATED LINKS</span></span>