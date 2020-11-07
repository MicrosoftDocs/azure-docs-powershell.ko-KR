---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: c228b00cb8d0d1e8f238e0b2e75427e0d623490f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876812"
---
# <span data-ttu-id="9b9c9-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b9c9-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9b9c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9b9c9-103">저장소 컨테이너에서 특정 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="9b9c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b9c9-104">SYNTAX</span></span>

### <span data-ttu-id="9b9c9-105">InvokeByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b9c9-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b9c9-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b9c9-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b9c9-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b9c9-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b9c9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9b9c9-108">DESCRIPTION</span></span>
<span data-ttu-id="9b9c9-109">**AzDataBoxEdgeStorageContainer** Cmdlet은 데이터 상자 가장자리 장치의 저장소 컨테이너에 대 한 데이터를 새로 고치기 위한 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="9b9c9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9b9c9-110">EXAMPLES</span></span>

### <span data-ttu-id="9b9c9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b9c9-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="9b9c9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9b9c9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="9b9c9-113">변수</span><span class="sxs-lookup"><span data-stu-id="9b9c9-113">PARAMETERS</span></span>

### <span data-ttu-id="9b9c9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b9c9-114">-AsJob</span></span>
<span data-ttu-id="9b9c9-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9b9c9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b9c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b9c9-116">-DefaultProfile</span></span>
<span data-ttu-id="9b9c9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b9c9-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="9b9c9-118">-DeviceName</span></span>
<span data-ttu-id="9b9c9-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="9b9c9-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9c9-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b9c9-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="9b9c9-121">자원 이름</span><span class="sxs-lookup"><span data-stu-id="9b9c9-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9c9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b9c9-122">-InputObject</span></span>
<span data-ttu-id="9b9c9-123">기존 EdgeStorageAccount 개체 제공</span><span class="sxs-lookup"><span data-stu-id="9b9c9-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9c9-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9b9c9-124">-Name</span></span>
<span data-ttu-id="9b9c9-125">자원 이름</span><span class="sxs-lookup"><span data-stu-id="9b9c9-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9c9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b9c9-126">-PassThru</span></span>
<span data-ttu-id="9b9c9-127">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-127">returns true if successful</span></span>

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

### <span data-ttu-id="9b9c9-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="9b9c9-128">-RefreshData</span></span>
<span data-ttu-id="9b9c9-129">클라우드의 데이터를 사용 하 여 컨테이너 메타 데이터 새로 고침</span><span class="sxs-lookup"><span data-stu-id="9b9c9-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="9b9c9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b9c9-130">-ResourceGroupName</span></span>
<span data-ttu-id="9b9c9-131">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9b9c9-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9c9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b9c9-132">-ResourceId</span></span>
<span data-ttu-id="9b9c9-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b9c9-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b9c9-134">-확인</span><span class="sxs-lookup"><span data-stu-id="9b9c9-134">-Confirm</span></span>
<span data-ttu-id="9b9c9-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b9c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b9c9-136">-WhatIf</span></span>
<span data-ttu-id="9b9c9-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b9c9-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b9c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b9c9-139">CommonParameters</span></span>
<span data-ttu-id="9b9c9-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b9c9-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b9c9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b9c9-142">입력</span><span class="sxs-lookup"><span data-stu-id="9b9c9-142">INPUTS</span></span>

### <span data-ttu-id="9b9c9-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b9c9-143">System.String</span></span>

### <span data-ttu-id="9b9c9-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b9c9-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9b9c9-145">출력</span><span class="sxs-lookup"><span data-stu-id="9b9c9-145">OUTPUTS</span></span>

### <span data-ttu-id="9b9c9-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b9c9-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9b9c9-147">상속자</span><span class="sxs-lookup"><span data-stu-id="9b9c9-147">NOTES</span></span>

## <span data-ttu-id="9b9c9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b9c9-148">RELATED LINKS</span></span>