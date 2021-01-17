---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330338"
---
# <span data-ttu-id="9ca32-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9ca32-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9ca32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca32-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca32-103">디바이스의 주문 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="9ca32-103">Get the order details for a device</span></span>

## <span data-ttu-id="9ca32-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ca32-104">SYNTAX</span></span>

### <span data-ttu-id="9ca32-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ca32-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ca32-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca32-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca32-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ca32-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ca32-108">설명</span><span class="sxs-lookup"><span data-stu-id="9ca32-108">DESCRIPTION</span></span>
<span data-ttu-id="9ca32-109">**Get-AzDataBoxEdgeOrder** cmdlet은 Data Box Edge 디바이스에 대한 주문 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca32-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="9ca32-110">예제</span><span class="sxs-lookup"><span data-stu-id="9ca32-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca32-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ca32-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="9ca32-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ca32-112">PARAMETERS</span></span>

### <span data-ttu-id="9ca32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca32-113">-DefaultProfile</span></span>
<span data-ttu-id="9ca32-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ca32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca32-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9ca32-115">-DeviceName</span></span>
<span data-ttu-id="9ca32-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9ca32-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca32-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9ca32-117">-DeviceObject</span></span>
<span data-ttu-id="9ca32-118">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="9ca32-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca32-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca32-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ca32-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9ca32-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca32-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca32-121">-ResourceId</span></span>
<span data-ttu-id="9ca32-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ca32-122">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca32-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca32-123">CommonParameters</span></span>
<span data-ttu-id="9ca32-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca32-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca32-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ca32-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca32-126">입력</span><span class="sxs-lookup"><span data-stu-id="9ca32-126">INPUTS</span></span>

### <span data-ttu-id="9ca32-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9ca32-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="9ca32-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9ca32-128">System.String</span></span>

## <span data-ttu-id="9ca32-129">출력</span><span class="sxs-lookup"><span data-stu-id="9ca32-129">OUTPUTS</span></span>

### <span data-ttu-id="9ca32-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9ca32-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="9ca32-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ca32-131">NOTES</span></span>

## <span data-ttu-id="9ca32-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ca32-132">RELATED LINKS</span></span>