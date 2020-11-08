---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049081"
---
# <span data-ttu-id="26e35-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="26e35-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="26e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e35-102">SYNOPSIS</span></span>
<span data-ttu-id="26e35-103">컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="26e35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26e35-104">SYNTAX</span></span>

### <span data-ttu-id="26e35-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="26e35-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e35-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e35-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e35-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26e35-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e35-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26e35-108">DESCRIPTION</span></span>
<span data-ttu-id="26e35-109">New-AzContainerRegistryWebhook cmdlet은 컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="26e35-110">예제의</span><span class="sxs-lookup"><span data-stu-id="26e35-110">EXAMPLES</span></span>

### <span data-ttu-id="26e35-111">예제 1: 컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="26e35-112">컨테이너 레지스트리 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="26e35-113">변수</span><span class="sxs-lookup"><span data-stu-id="26e35-113">PARAMETERS</span></span>

### <span data-ttu-id="26e35-114">-작업</span><span class="sxs-lookup"><span data-stu-id="26e35-114">-Action</span></span>
<span data-ttu-id="26e35-115">Webhook을 포스트백으로 알리기 위한 작업의 공백으로 구분 된 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e35-116">-DefaultProfile</span></span>
<span data-ttu-id="26e35-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26e35-118">-헤더</span><span class="sxs-lookup"><span data-stu-id="26e35-118">-Header</span></span>
<span data-ttu-id="26e35-119">Webhook 알림에 추가 되는 사용자 지정 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-120">-위치</span><span class="sxs-lookup"><span data-stu-id="26e35-120">-Location</span></span>
<span data-ttu-id="26e35-121">Webhook 위치.</span><span class="sxs-lookup"><span data-stu-id="26e35-121">Webhook Location.</span></span>
<span data-ttu-id="26e35-122">기본값은 레지스트리의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-123">-이름</span><span class="sxs-lookup"><span data-stu-id="26e35-123">-Name</span></span>
<span data-ttu-id="26e35-124">Webhook 이름.</span><span class="sxs-lookup"><span data-stu-id="26e35-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-125">-레지스트리</span><span class="sxs-lookup"><span data-stu-id="26e35-125">-Registry</span></span>
<span data-ttu-id="26e35-126">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="26e35-127">-RegistryName</span></span>
<span data-ttu-id="26e35-128">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-128">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e35-129">-ResourceGroupName</span></span>
<span data-ttu-id="26e35-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e35-131">-ResourceId</span></span>
<span data-ttu-id="26e35-132">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="26e35-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-133">-범위</span><span class="sxs-lookup"><span data-stu-id="26e35-133">-Scope</span></span>
<span data-ttu-id="26e35-134">Webhook 범위.</span><span class="sxs-lookup"><span data-stu-id="26e35-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-135">-상태</span><span class="sxs-lookup"><span data-stu-id="26e35-135">-Status</span></span>
<span data-ttu-id="26e35-136">Webhook 상태, default 값이 사용 하도록 설정 됨</span><span class="sxs-lookup"><span data-stu-id="26e35-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-137">태그</span><span class="sxs-lookup"><span data-stu-id="26e35-137">-Tag</span></span>
<span data-ttu-id="26e35-138">Webhook 태그.</span><span class="sxs-lookup"><span data-stu-id="26e35-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="26e35-139">-Uri</span></span>
<span data-ttu-id="26e35-140">알림을 게시할 webhook에 대 한 서비스 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-141">-확인</span><span class="sxs-lookup"><span data-stu-id="26e35-141">-Confirm</span></span>
<span data-ttu-id="26e35-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e35-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e35-143">-WhatIf</span></span>
<span data-ttu-id="26e35-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e35-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e35-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e35-146">CommonParameters</span></span>
<span data-ttu-id="26e35-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e35-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e35-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26e35-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e35-149">입력</span><span class="sxs-lookup"><span data-stu-id="26e35-149">INPUTS</span></span>

### <span data-ttu-id="26e35-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26e35-150">System.String</span></span>

## <span data-ttu-id="26e35-151">출력</span><span class="sxs-lookup"><span data-stu-id="26e35-151">OUTPUTS</span></span>

### <span data-ttu-id="26e35-152">ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="26e35-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="26e35-153">상속자</span><span class="sxs-lookup"><span data-stu-id="26e35-153">NOTES</span></span>

## <span data-ttu-id="26e35-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26e35-154">RELATED LINKS</span></span>

[<span data-ttu-id="26e35-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="26e35-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="26e35-156">업데이트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="26e35-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="26e35-157">제거-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="26e35-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="26e35-158">테스트-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="26e35-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)