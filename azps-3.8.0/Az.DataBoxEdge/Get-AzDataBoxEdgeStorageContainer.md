---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043412"
---
# <span data-ttu-id="14fe8-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="14fe8-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="14fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="14fe8-103">디바이스의 Edge 저장소 계정에 대 한 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14fe8-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="14fe8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14fe8-104">SYNTAX</span></span>

### <span data-ttu-id="14fe8-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="14fe8-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14fe8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fe8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14fe8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fe8-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14fe8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14fe8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="14fe8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="14fe8-109">DESCRIPTION</span></span>
<span data-ttu-id="14fe8-110">**AzDataBoxEdgeStorageContainer** Cmdlet은 데이터 상자 가장자리 디바이스의 edge 저장소 계정에 대 한 저장소 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14fe8-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="14fe8-111">Cmdlet에서 이름을 매개 변수로 지정 하 여 특정 저장소 컨테이너의 세부 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14fe8-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="14fe8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="14fe8-112">EXAMPLES</span></span>

### <span data-ttu-id="14fe8-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="14fe8-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="14fe8-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="14fe8-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="14fe8-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="14fe8-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="14fe8-116">변수</span><span class="sxs-lookup"><span data-stu-id="14fe8-116">PARAMETERS</span></span>

### <span data-ttu-id="14fe8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fe8-117">-DefaultProfile</span></span>
<span data-ttu-id="14fe8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14fe8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14fe8-119">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="14fe8-119">-DeviceName</span></span>
<span data-ttu-id="14fe8-120">장치 이름</span><span class="sxs-lookup"><span data-stu-id="14fe8-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14fe8-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14fe8-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="14fe8-122">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="14fe8-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14fe8-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="14fe8-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="14fe8-124">기존 EdgeStorageAccount 개체 제공</span><span class="sxs-lookup"><span data-stu-id="14fe8-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14fe8-125">-이름</span><span class="sxs-lookup"><span data-stu-id="14fe8-125">-Name</span></span>
<span data-ttu-id="14fe8-126">EdgeStorageContainer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14fe8-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14fe8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14fe8-127">-ResourceGroupName</span></span>
<span data-ttu-id="14fe8-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="14fe8-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14fe8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14fe8-129">-ResourceId</span></span>
<span data-ttu-id="14fe8-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14fe8-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14fe8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fe8-131">CommonParameters</span></span>
<span data-ttu-id="14fe8-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14fe8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fe8-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14fe8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fe8-134">입력</span><span class="sxs-lookup"><span data-stu-id="14fe8-134">INPUTS</span></span>

### <span data-ttu-id="14fe8-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14fe8-135">System.String</span></span>

### <span data-ttu-id="14fe8-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14fe8-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="14fe8-137">출력</span><span class="sxs-lookup"><span data-stu-id="14fe8-137">OUTPUTS</span></span>

### <span data-ttu-id="14fe8-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="14fe8-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="14fe8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="14fe8-139">NOTES</span></span>

## <span data-ttu-id="14fe8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14fe8-140">RELATED LINKS</span></span>