---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: a902c88c53736f1e0db238cdb53ea381e5e887a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524648"
---
# <span data-ttu-id="c99e5-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c99e5-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="c99e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c99e5-103">자동화에서 DSC 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c99e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c99e5-104">SYNTAX</span></span>

### <span data-ttu-id="c99e5-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="c99e5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99e5-106">ById</span><span class="sxs-lookup"><span data-stu-id="c99e5-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99e5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c99e5-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99e5-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c99e5-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c99e5-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="c99e5-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99e5-110">설명은</span><span class="sxs-lookup"><span data-stu-id="c99e5-110">DESCRIPTION</span></span>
<span data-ttu-id="c99e5-111">**AzureRmAutomationDscNode** Cmdlet은 Azure AUTOMATION에서 Ap (원하는 상태 구성) 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="c99e5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c99e5-112">EXAMPLES</span></span>

### <span data-ttu-id="c99e5-113">예제 1: 모든 DSC 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="c99e5-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c99e5-114">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 DSC 노드에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c99e5-115">예제 2: DSC 구성에 대 한 모든 DSC 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="c99e5-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="c99e5-116">이 명령은 DSC 구성 ContosoConfiguration에서 생성 된 DSC 노드 구성에 매핑되는 Contoso17 이라는 자동화 계정의 모든 DSC 노드에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="c99e5-117">예제 3: ID로 DSC 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="c99e5-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="c99e5-118">이 명령은 Contoso17 이라는 자동화 계정에서 지정 된 ID를 사용 하 여 DSC 노드의 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c99e5-119">예제 4: 이름별로 DSC 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="c99e5-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="c99e5-120">이 명령은 Contoso17 이라는 Automation 계정의 이름 Computer14를 사용 하 여 DSC 노드의 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c99e5-121">예제 5: DSC 노드 구성에 매핑된 모든 DSC 노드 가져오기</span><span class="sxs-lookup"><span data-stu-id="c99e5-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="c99e5-122">이 명령은 ContosoConfiguration 이라는 DSC 노드 구성에 매핑되는 Contoso17 이라는 자동화 계정의 모든 DSC 노드에 대 한 메타 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="c99e5-123">변수</span><span class="sxs-lookup"><span data-stu-id="c99e5-123">PARAMETERS</span></span>

### <span data-ttu-id="c99e5-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c99e5-124">-AutomationAccountName</span></span>
<span data-ttu-id="c99e5-125">이 cmdlet이 가져오는 DSC 노드를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c99e5-126">-ConfigurationName</span></span>
<span data-ttu-id="c99e5-127">DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="c99e5-128">이 cmdlet은이 매개 변수에서 지정 하는 구성에서 생성 된 노드 구성과 일치 하는 DSC 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99e5-129">-DefaultProfile</span></span>
<span data-ttu-id="c99e5-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c99e5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c99e5-131">-Id</span><span class="sxs-lookup"><span data-stu-id="c99e5-131">-Id</span></span>
<span data-ttu-id="c99e5-132">이 cmdlet이 가져오는 DSC 노드의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-133">-이름</span><span class="sxs-lookup"><span data-stu-id="c99e5-133">-Name</span></span>
<span data-ttu-id="c99e5-134">이 cmdlet이 가져오는 DSC 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c99e5-135">-NodeConfigurationName</span></span>
<span data-ttu-id="c99e5-136">이 cmdlet이 가져오는 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99e5-137">-ResourceGroupName</span></span>
<span data-ttu-id="c99e5-138">이 cmdlet이 DSC 노드를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-139">-상태</span><span class="sxs-lookup"><span data-stu-id="c99e5-139">-Status</span></span>
<span data-ttu-id="c99e5-140">이 cmdlet이 가져오는 DSC 노드의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="c99e5-141">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-141">Valid values are:</span></span> 
- <span data-ttu-id="c99e5-142">기준</span><span class="sxs-lookup"><span data-stu-id="c99e5-142">Compliant</span></span> 
- <span data-ttu-id="c99e5-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="c99e5-143">NotCompliant</span></span>
- <span data-ttu-id="c99e5-144">못함</span><span class="sxs-lookup"><span data-stu-id="c99e5-144">Failed</span></span>
- <span data-ttu-id="c99e5-145">중일</span><span class="sxs-lookup"><span data-stu-id="c99e5-145">Pending</span></span> 
- <span data-ttu-id="c99e5-146">받아들여졌습니다</span><span class="sxs-lookup"><span data-stu-id="c99e5-146">Received</span></span>
- <span data-ttu-id="c99e5-147">중단</span><span class="sxs-lookup"><span data-stu-id="c99e5-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99e5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99e5-148">CommonParameters</span></span>
<span data-ttu-id="c99e5-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c99e5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99e5-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99e5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99e5-151">입력</span><span class="sxs-lookup"><span data-stu-id="c99e5-151">INPUTS</span></span>

### <span data-ttu-id="c99e5-152">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c99e5-152">System.Guid</span></span>

### <span data-ttu-id="c99e5-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c99e5-153">System.String</span></span>

## <span data-ttu-id="c99e5-154">출력</span><span class="sxs-lookup"><span data-stu-id="c99e5-154">OUTPUTS</span></span>

### <span data-ttu-id="c99e5-155">Microsoft Azure.-DscNode</span><span class="sxs-lookup"><span data-stu-id="c99e5-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="c99e5-156">상속자</span><span class="sxs-lookup"><span data-stu-id="c99e5-156">NOTES</span></span>

## <span data-ttu-id="c99e5-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c99e5-157">RELATED LINKS</span></span>

[<span data-ttu-id="c99e5-158">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c99e5-158">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="c99e5-159">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c99e5-159">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="c99e5-160">등록 취소-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="c99e5-160">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)

