---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: aa34157f556de3fe0acc5d8197caaa1a14dc364d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041750"
---
# <span data-ttu-id="69e12-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="69e12-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="69e12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69e12-102">SYNOPSIS</span></span>
<span data-ttu-id="69e12-103">배포 템플릿을 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="69e12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69e12-104">SYNTAX</span></span>

### <span data-ttu-id="69e12-105">SaveByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="69e12-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69e12-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="69e12-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69e12-107">설명은</span><span class="sxs-lookup"><span data-stu-id="69e12-107">DESCRIPTION</span></span>
<span data-ttu-id="69e12-108">**AzDeploymentTemplate** cmdlet은 배포 템플릿을 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="69e12-109">예제의</span><span class="sxs-lookup"><span data-stu-id="69e12-109">EXAMPLES</span></span>

### <span data-ttu-id="69e12-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="69e12-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="69e12-111">이 명령은 TestDeployment에서 배포 템플릿을 가져와 현재 디렉터리에 JSON 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="69e12-112">예제 2: 배포 가져오기 및 서식 파일 저장</span><span class="sxs-lookup"><span data-stu-id="69e12-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="69e12-113">이 명령은 현재 구독 범위에서 배포 "역할 배포"를 가져와 해당 템플릿을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="69e12-114">변수</span><span class="sxs-lookup"><span data-stu-id="69e12-114">PARAMETERS</span></span>

### <span data-ttu-id="69e12-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="69e12-115">-ApiVersion</span></span>
<span data-ttu-id="69e12-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="69e12-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="69e12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e12-118">-DefaultProfile</span></span>
<span data-ttu-id="69e12-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e12-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="69e12-120">-DeploymentName</span></span>
<span data-ttu-id="69e12-121">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-121">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e12-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="69e12-122">-DeploymentObject</span></span>
<span data-ttu-id="69e12-123">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-123">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69e12-124">-Force</span><span class="sxs-lookup"><span data-stu-id="69e12-124">-Force</span></span>
<span data-ttu-id="69e12-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="69e12-126">-Path</span><span class="sxs-lookup"><span data-stu-id="69e12-126">-Path</span></span>
<span data-ttu-id="69e12-127">서식 파일의 출력 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="69e12-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="69e12-128">-Pre</span></span>
<span data-ttu-id="69e12-129">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="69e12-130">-확인</span><span class="sxs-lookup"><span data-stu-id="69e12-130">-Confirm</span></span>
<span data-ttu-id="69e12-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e12-132">-WhatIf</span></span>
<span data-ttu-id="69e12-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e12-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e12-135">CommonParameters</span></span>
<span data-ttu-id="69e12-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e12-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69e12-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e12-138">입력</span><span class="sxs-lookup"><span data-stu-id="69e12-138">INPUTS</span></span>

### <span data-ttu-id="69e12-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="69e12-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="69e12-140">출력</span><span class="sxs-lookup"><span data-stu-id="69e12-140">OUTPUTS</span></span>

### <span data-ttu-id="69e12-141">SdkModels. PSTemplatePath에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="69e12-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="69e12-142">상속자</span><span class="sxs-lookup"><span data-stu-id="69e12-142">NOTES</span></span>

## <span data-ttu-id="69e12-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69e12-143">RELATED LINKS</span></span>