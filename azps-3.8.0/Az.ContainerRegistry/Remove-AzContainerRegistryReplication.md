---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877910"
---
# <span data-ttu-id="a5c59-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a5c59-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="a5c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c59-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c59-103">컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="a5c59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5c59-104">SYNTAX</span></span>

### <span data-ttu-id="a5c59-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5c59-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c59-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c59-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c59-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c59-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c59-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a5c59-108">DESCRIPTION</span></span>
<span data-ttu-id="a5c59-109">Remove-AzContainerRegistryReplication cmdlet은 컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="a5c59-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a5c59-110">EXAMPLES</span></span>

### <span data-ttu-id="a5c59-111">예제 1: 컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="a5c59-112">컨테이너 레지스트리 복제를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="a5c59-113">변수</span><span class="sxs-lookup"><span data-stu-id="a5c59-113">PARAMETERS</span></span>

### <span data-ttu-id="a5c59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c59-114">-DefaultProfile</span></span>
<span data-ttu-id="a5c59-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c59-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a5c59-116">-Name</span></span>
<span data-ttu-id="a5c59-117">컨테이너 레지스트리 복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="a5c59-118">위치 이름을 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c59-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5c59-119">-PassThru</span></span>
<span data-ttu-id="a5c59-120">제거에 성공한 경우이 cmdlet이 true를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="a5c59-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="a5c59-121">-RegistryName</span></span>
<span data-ttu-id="a5c59-122">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="a5c59-123">-복제</span><span class="sxs-lookup"><span data-stu-id="a5c59-123">-Replication</span></span>
<span data-ttu-id="a5c59-124">컨테이너 레지스트리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c59-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c59-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5c59-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5c59-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c59-127">-ResourceId</span></span>
<span data-ttu-id="a5c59-128">컨테이너 레지스트리 복제 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a5c59-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="a5c59-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a5c59-129">-Confirm</span></span>
<span data-ttu-id="a5c59-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c59-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c59-131">-WhatIf</span></span>
<span data-ttu-id="a5c59-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c59-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c59-134">CommonParameters</span></span>
<span data-ttu-id="a5c59-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c59-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5c59-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c59-137">입력</span><span class="sxs-lookup"><span data-stu-id="a5c59-137">INPUTS</span></span>

### <span data-ttu-id="a5c59-138">ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a5c59-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="a5c59-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5c59-139">System.String</span></span>

## <span data-ttu-id="a5c59-140">출력</span><span class="sxs-lookup"><span data-stu-id="a5c59-140">OUTPUTS</span></span>

### <span data-ttu-id="a5c59-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a5c59-141">System.Boolean</span></span>

## <span data-ttu-id="a5c59-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a5c59-142">NOTES</span></span>

## <span data-ttu-id="a5c59-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5c59-143">RELATED LINKS</span></span>

[<span data-ttu-id="a5c59-144">새로운 AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a5c59-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="a5c59-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="a5c59-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)
