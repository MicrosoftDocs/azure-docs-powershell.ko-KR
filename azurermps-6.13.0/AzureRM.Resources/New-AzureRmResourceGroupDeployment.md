---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: beb28c4b49becf072cba526d2bf62b98bc1fd91f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533315"
---
# <span data-ttu-id="dcd52-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd52-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="dcd52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd52-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd52-103">리소스 그룹에 Azure 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dcd52-104">SYNTAX</span></span>

### <span data-ttu-id="dcd52-105">By서식 Filewithnoparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="dcd52-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-106">By서식 Fileandparameterobject</span><span class="sxs-lookup"><span data-stu-id="dcd52-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-107">By서식 Uriandparameterobject</span><span class="sxs-lookup"><span data-stu-id="dcd52-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-108">By서식 파일 Andparameterfile</span><span class="sxs-lookup"><span data-stu-id="dcd52-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-109">By서식 Uriandparameterfile</span><span class="sxs-lookup"><span data-stu-id="dcd52-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-110">By서식 Fileandparameteruri</span><span class="sxs-lookup"><span data-stu-id="dcd52-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-111">By서식 Uriandparameteruri</span><span class="sxs-lookup"><span data-stu-id="dcd52-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd52-112">By서식 Uriwithnoparameters</span><span class="sxs-lookup"><span data-stu-id="dcd52-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd52-113">설명은</span><span class="sxs-lookup"><span data-stu-id="dcd52-113">DESCRIPTION</span></span>
<span data-ttu-id="dcd52-114">**새 AzureRmResourceGroupDeployment** cmdlet은 기존 리소스 그룹에 배포를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="dcd52-115">여기에는 배포에 필요한 리소스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="dcd52-116">Azure 리소스는 사용자가 관리 하는 Azure 엔터티 (예: 데이터베이스 서버, 데이터베이스, 웹 사이트, 가상 컴퓨터 또는 저장소 계정)입니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="dcd52-117">Azure 리소스 그룹은 웹 사이트, 데이터베이스 서버, 재무 웹 사이트에 필요한 데이터베이스 등의 단위로 배포 되는 Azure 리소스의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="dcd52-118">리소스 그룹 배포는 서식 파일을 사용 하 여 리소스 그룹에 리소스를 추가 하 고 Azure에서 사용할 수 있도록 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="dcd52-119">서식 파일을 사용 하지 않고 리소스 그룹에 리소스를 추가 하려면 New-AzureRmResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>
<span data-ttu-id="dcd52-120">리소스 그룹 배포를 추가 하려면 기존 리소스 그룹 및 리소스 그룹 서식 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="dcd52-121">리소스 그룹 템플릿은 웹 포털 등의 복잡 한 클라우드 기반 서비스에 대 한 리소스 그룹을 나타내는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="dcd52-122">이 템플릿에는 필수 리소스 및 구성 가능한 속성 값 (예: 이름 및 크기)에 대 한 매개 변수 자리 표시 자가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="dcd52-123">Azure 서식 파일 갤러리에서 여러 서식 파일을 찾을 수도 있고 서식 파일을 직접 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="dcd52-124">**AzureRmResourceGroupGalleryTemplate** cmdlet을 사용 하 여 갤러리에서 서식 파일을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="dcd52-125">사용자 지정 서식 파일을 사용 하 여 리소스 그룹을 만들려면 하위 *서식 파일* 매개 변수 또는 하위 *서식 uri* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="dcd52-126">각 템플릿에는 구성 가능한 속성에 대 한 매개 변수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="dcd52-127">서식 파일 매개 변수에 대 한 값을 지정 하려면 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="dcd52-128">또는 템플릿을 지정할 때 명령에 동적으로 추가 되는 템플릿 매개 변수를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="dcd52-129">동적 매개 변수를 사용 하려면 명령 프롬프트에 입력 하거나 빼기 기호 (-)를 입력 하 여 매개 변수를 나타내고 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="dcd52-130">명령 프롬프트에서 입력 하는 템플릿 매개 변수 값은 template 매개 변수 개체 또는 파일의 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="dcd52-131">예제의</span><span class="sxs-lookup"><span data-stu-id="dcd52-131">EXAMPLES</span></span>

### <span data-ttu-id="dcd52-132">예제 1: 사용자 지정 서식 파일 및 매개 변수 파일을 사용 하 여 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="dcd52-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="dcd52-133">이 명령은 사용자 지정 서식 파일과 디스크의 서식 파일을 사용 하 여 새 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="dcd52-134">이 명령은 template *파일* 매개 변수를 사용 하 여 템플릿과 매개 변수 값이 포함 된 파일을 지정 하는 서식 파일과 템플릿 매개 변수 *파일* 을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="dcd52-135">변수</span><span class="sxs-lookup"><span data-stu-id="dcd52-135">PARAMETERS</span></span>

### <span data-ttu-id="dcd52-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dcd52-136">-ApiVersion</span></span>
<span data-ttu-id="dcd52-137">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="dcd52-138">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="dcd52-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcd52-139">-AsJob</span></span>
<span data-ttu-id="dcd52-140">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dcd52-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcd52-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd52-141">-DefaultProfile</span></span>
<span data-ttu-id="dcd52-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dcd52-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcd52-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="dcd52-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="dcd52-144">디버그 로그 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-144">Specifies a debug log level.</span></span>
<span data-ttu-id="dcd52-145">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dcd52-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="dcd52-146">RequestContent</span></span>
- <span data-ttu-id="dcd52-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="dcd52-147">ResponseContent</span></span>
- <span data-ttu-id="dcd52-148">모든</span><span class="sxs-lookup"><span data-stu-id="dcd52-148">All</span></span>
- <span data-ttu-id="dcd52-149">않아야</span><span class="sxs-lookup"><span data-stu-id="dcd52-149">None</span></span>

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

### <span data-ttu-id="dcd52-150">-Force</span><span class="sxs-lookup"><span data-stu-id="dcd52-150">-Force</span></span>
<span data-ttu-id="dcd52-151">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcd52-152">-모드</span><span class="sxs-lookup"><span data-stu-id="dcd52-152">-Mode</span></span>
<span data-ttu-id="dcd52-153">배포 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-153">Specifies the deployment mode.</span></span> <span data-ttu-id="dcd52-154">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dcd52-155">마칠</span><span class="sxs-lookup"><span data-stu-id="dcd52-155">Complete</span></span>
- <span data-ttu-id="dcd52-156">완료 모드에서 리소스 관리자는 리소스 그룹에 존재 하지만 서식 파일에 지정 되지 않은 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="dcd52-157">증분 모드에서 리소스 관리자는 리소스 그룹에는 있지만 서식 파일에 지정 되지 않은 변경 되지 않은 리소스를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd52-158">-이름</span><span class="sxs-lookup"><span data-stu-id="dcd52-158">-Name</span></span>
<span data-ttu-id="dcd52-159">만들려는 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-159">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd52-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="dcd52-160">-Pre</span></span>
<span data-ttu-id="dcd52-161">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dcd52-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd52-162">-ResourceGroupName</span></span>
<span data-ttu-id="dcd52-163">배포할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="dcd52-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="dcd52-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="dcd52-165">-RollbackToLastDeployment가 사용 되는 경우 리소스 그룹에서 지정 된 이름을 사용 하 여 성공한 배포로 롤백할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="dcd52-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd52-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="dcd52-167">-RollBackDeploymentName가 사용 되는 경우 리소스 그룹에서 마지막으로 성공한 배포에 롤백하는 것으로 표시 되지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="dcd52-168">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="dcd52-168">-TemplateFile</span></span>
<span data-ttu-id="dcd52-169">JSON 템플릿 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="dcd52-170">이는 사용자 지정 서식 파일 이거나 **AzureRmResourceGroupGalleryTemplate** cmdlet을 사용 하 여 만든 것과 같은 JSON 파일로 저장 되는 갤러리 서식 파일 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="dcd52-171">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="dcd52-171">-TemplateParameterFile</span></span>
<span data-ttu-id="dcd52-172">템플릿 매개 변수의 이름 및 값이 포함 된 JSON 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="dcd52-173">템플릿에 매개 변수가 포함 된 경우에는 template *Parameterfile* 매개 변수 또는 Template *parameterobject* 매개 변수를 사용 하 여 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="dcd52-174">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="dcd52-175">동적 매개 변수를 사용 하려면 매개 변수 이름을 나타내는 빼기 기호 (-)를 입력 한 다음 Tab 키를 사용 하 여 사용 가능한 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd52-176">------# Parameterobject</span><span class="sxs-lookup"><span data-stu-id="dcd52-176">-TemplateParameterObject</span></span>
<span data-ttu-id="dcd52-177">템플릿 매개 변수 이름 및 값의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="dcd52-178">Windows PowerShell의 해시 테이블에 대 한 도움말을 보려면를 입력 `Get-Help about_Hash_Tables` 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="dcd52-179">템플릿에 매개 변수가 있는 경우 매개 변수 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="dcd52-180">서식 파일을 지정 하면 서식 파일 매개 변수가 명령에 동적으로 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd52-181">--# Parameteruri</span><span class="sxs-lookup"><span data-stu-id="dcd52-181">-TemplateParameterUri</span></span>
<span data-ttu-id="dcd52-182">템플릿 매개 변수 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd52-183">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="dcd52-183">-TemplateUri</span></span>
<span data-ttu-id="dcd52-184">JSON 템플릿 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="dcd52-185">이 파일은 **AzureRmResourceGroupGalleryTemplate** 를 사용 하는 것과 같이 JSON 파일로 저장 되는 사용자 지정 서식 파일 또는 갤러리 서식 파일이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="dcd52-186">-확인</span><span class="sxs-lookup"><span data-stu-id="dcd52-186">-Confirm</span></span>
<span data-ttu-id="dcd52-187">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd52-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd52-188">-WhatIf</span></span>
<span data-ttu-id="dcd52-189">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd52-190">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd52-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd52-191">CommonParameters</span></span>
<span data-ttu-id="dcd52-192">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd52-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd52-193">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd52-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd52-194">입력</span><span class="sxs-lookup"><span data-stu-id="dcd52-194">INPUTS</span></span>

### <span data-ttu-id="dcd52-195">않아야</span><span class="sxs-lookup"><span data-stu-id="dcd52-195">None</span></span>

## <span data-ttu-id="dcd52-196">출력</span><span class="sxs-lookup"><span data-stu-id="dcd52-196">OUTPUTS</span></span>

### <span data-ttu-id="dcd52-197">. PSResourceGroupDeployment의 모든 모델</span><span class="sxs-lookup"><span data-stu-id="dcd52-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="dcd52-198">상속자</span><span class="sxs-lookup"><span data-stu-id="dcd52-198">NOTES</span></span>

## <span data-ttu-id="dcd52-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcd52-199">RELATED LINKS</span></span>

[<span data-ttu-id="dcd52-200">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd52-200">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="dcd52-201">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="dcd52-201">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="dcd52-202">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcd52-202">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="dcd52-203">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd52-203">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="dcd52-204">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd52-204">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="dcd52-205">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd52-205">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)

