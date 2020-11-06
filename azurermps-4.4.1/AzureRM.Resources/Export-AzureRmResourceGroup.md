---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 3b83b18bf7a795dd8df3c93a7fd2f8b25974ce35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529173"
---
# <span data-ttu-id="04d2b-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04d2b-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="04d2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="04d2b-103">리소스 그룹을 서식 파일로 캡처하여 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04d2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04d2b-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04d2b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04d2b-105">DESCRIPTION</span></span>
<span data-ttu-id="04d2b-106">**Export-AzureRmResourceGroup** cmdlet은 지정 된 리소스 그룹을 템플릿으로 캡처하여 JSON 파일에 저장 합니다. 이는 리소스 그룹에 리소스를 이미 만든 다음 서식 파일을 사용 하 여 얻을 수 있는 기능을 활용 하려는 시나리오에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="04d2b-107">이 cmdlet을 사용 하면 리소스 그룹의 기존 리소스에 대 한 템플릿을 생성 하 여 쉽게 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="04d2b-108">이 cmdlet이 템플릿의 일부를 생성 하지 못하는 경우가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="04d2b-109">실패 한 리소스를 알리는 경고 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="04d2b-110">이 서식 파일은 성공한 파트에 대해 계속 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="04d2b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="04d2b-111">EXAMPLES</span></span>

### <span data-ttu-id="04d2b-112">예제 1: 리소스 그룹 내보내기</span><span class="sxs-lookup"><span data-stu-id="04d2b-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="04d2b-113">이 명령은 TestGroup 이라는 리소스 그룹을 템플릿으로 캡처하여 현재 디렉터리의 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="04d2b-114">변수</span><span class="sxs-lookup"><span data-stu-id="04d2b-114">PARAMETERS</span></span>

### <span data-ttu-id="04d2b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="04d2b-115">-ApiVersion</span></span>
<span data-ttu-id="04d2b-116">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="04d2b-117">지정 하지 않으면 최신 API 버전이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="04d2b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="04d2b-118">-Force</span></span>
<span data-ttu-id="04d2b-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04d2b-120">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="04d2b-120">-IncludeComments</span></span>
<span data-ttu-id="04d2b-121">이 작업에서 템플릿을 주석으로 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-121">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="04d2b-122">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="04d2b-122">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="04d2b-123">이 작업에서 템플릿 매개 변수를 기본값으로 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-123">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="04d2b-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="04d2b-124">-InformationAction</span></span>
<span data-ttu-id="04d2b-125">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="04d2b-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04d2b-127">하기로</span><span class="sxs-lookup"><span data-stu-id="04d2b-127">Continue</span></span>
- <span data-ttu-id="04d2b-128">숨기기</span><span class="sxs-lookup"><span data-stu-id="04d2b-128">Ignore</span></span>
- <span data-ttu-id="04d2b-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="04d2b-129">Inquire</span></span>
- <span data-ttu-id="04d2b-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04d2b-130">SilentlyContinue</span></span>
- <span data-ttu-id="04d2b-131">중지가</span><span class="sxs-lookup"><span data-stu-id="04d2b-131">Stop</span></span>
- <span data-ttu-id="04d2b-132">대기</span><span class="sxs-lookup"><span data-stu-id="04d2b-132">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d2b-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04d2b-133">-InformationVariable</span></span>
<span data-ttu-id="04d2b-134">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-134">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d2b-135">-Path</span><span class="sxs-lookup"><span data-stu-id="04d2b-135">-Path</span></span>
<span data-ttu-id="04d2b-136">서식 파일의 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-136">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="04d2b-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="04d2b-137">-Pre</span></span>
<span data-ttu-id="04d2b-138">사용할 API 버전을 자동으로 결정할 때이 cmdlet이 시험판 API 버전을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-138">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="04d2b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d2b-139">-ResourceGroupName</span></span>
<span data-ttu-id="04d2b-140">내보낼 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-140">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d2b-141">-확인</span><span class="sxs-lookup"><span data-stu-id="04d2b-141">-Confirm</span></span>
<span data-ttu-id="04d2b-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d2b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d2b-143">-WhatIf</span></span>
<span data-ttu-id="04d2b-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d2b-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d2b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d2b-146">-DefaultProfile</span></span>
<span data-ttu-id="04d2b-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04d2b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d2b-148">CommonParameters</span></span>
<span data-ttu-id="04d2b-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d2b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d2b-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d2b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d2b-151">입력</span><span class="sxs-lookup"><span data-stu-id="04d2b-151">INPUTS</span></span>

## <span data-ttu-id="04d2b-152">출력</span><span class="sxs-lookup"><span data-stu-id="04d2b-152">OUTPUTS</span></span>

### <span data-ttu-id="04d2b-153">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="04d2b-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="04d2b-154">상속자</span><span class="sxs-lookup"><span data-stu-id="04d2b-154">NOTES</span></span>

## <span data-ttu-id="04d2b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04d2b-155">RELATED LINKS</span></span>

[<span data-ttu-id="04d2b-156">찾기-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="04d2b-156">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)

