---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215691"
---
# <span data-ttu-id="06289-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="06289-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="06289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06289-102">SYNOPSIS</span></span>
<span data-ttu-id="06289-103">리소스 그룹 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="06289-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06289-104">SYNTAX</span></span>

### <span data-ttu-id="06289-105">StopByResourceGroupDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="06289-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06289-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="06289-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06289-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06289-107">DESCRIPTION</span></span>
<span data-ttu-id="06289-108">**AzResourceGroupDeployment** cmdlet은 시작 되었지만 완료 되지 않은 Azure 리소스 그룹 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="06289-109">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="06289-110">Azure 리소스는 웹 사이트, 데이터베이스 또는 데이터베이스 서버와 같이 사용자가 관리 하는 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="06289-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="06289-111">리소스 그룹은 하나의 단위로 배포 되는 리소스 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="06289-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="06289-112">리소스 그룹을 배포 하려면 New-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="06289-113">New-AzResource cmdlet은 새 리소스를 만들지만이 cmdlet이 중지할 수 있는 리소스 그룹 배포 작업을 트리거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06289-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="06289-114">이 cmdlet는 실행 중인 하나의 배포만 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="06289-115">특정 배포를 중지 하려면 *Name* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="06289-116">*Name* 매개 변수를 생략 하면 **AzResourceGroupDeployment** 는 실행 중인 배포를 검색 하 고 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="06289-117">Cmdlet이 실행 중인 배포를 두 개 이상 찾으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="06289-118">예제의</span><span class="sxs-lookup"><span data-stu-id="06289-118">EXAMPLES</span></span>

### <span data-ttu-id="06289-119">예제 1: 리소스 그룹 배포 시작 및 중지</span><span class="sxs-lookup"><span data-stu-id="06289-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="06289-120">변수</span><span class="sxs-lookup"><span data-stu-id="06289-120">PARAMETERS</span></span>

### <span data-ttu-id="06289-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06289-121">-DefaultProfile</span></span>
<span data-ttu-id="06289-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06289-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06289-123">-Id</span><span class="sxs-lookup"><span data-stu-id="06289-123">-Id</span></span>
<span data-ttu-id="06289-124">중지할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-124">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06289-125">-이름</span><span class="sxs-lookup"><span data-stu-id="06289-125">-Name</span></span>
<span data-ttu-id="06289-126">중지할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="06289-127">이 매개 변수를 지정 하지 않으면이 cmdlet이 리소스 그룹에서 실행 중인 배포를 검색 하 고 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="06289-128">실행 중인 배포를 두 개 이상 찾으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="06289-129">배포 이름을 가져오려면 Get-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06289-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="06289-130">-Pre</span></span>
<span data-ttu-id="06289-131">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="06289-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="06289-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06289-132">-ResourceGroupName</span></span>
<span data-ttu-id="06289-133">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="06289-134">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06289-135">-확인</span><span class="sxs-lookup"><span data-stu-id="06289-135">-Confirm</span></span>
<span data-ttu-id="06289-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06289-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06289-137">-WhatIf</span></span>
<span data-ttu-id="06289-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06289-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06289-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06289-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06289-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06289-140">CommonParameters</span></span>
<span data-ttu-id="06289-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06289-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06289-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="06289-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06289-143">입력</span><span class="sxs-lookup"><span data-stu-id="06289-143">INPUTS</span></span>

### <span data-ttu-id="06289-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06289-144">System.String</span></span>

## <span data-ttu-id="06289-145">출력</span><span class="sxs-lookup"><span data-stu-id="06289-145">OUTPUTS</span></span>

### <span data-ttu-id="06289-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="06289-146">System.Boolean</span></span>

## <span data-ttu-id="06289-147">상속자</span><span class="sxs-lookup"><span data-stu-id="06289-147">NOTES</span></span>

## <span data-ttu-id="06289-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06289-148">RELATED LINKS</span></span>

[<span data-ttu-id="06289-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="06289-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="06289-150">새로운 AzResource</span><span class="sxs-lookup"><span data-stu-id="06289-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="06289-151">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06289-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="06289-152">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="06289-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="06289-153">제거-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="06289-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="06289-154">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="06289-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)

