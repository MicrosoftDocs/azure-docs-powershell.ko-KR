---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 0ab290934a956282a16d9e2321b2c5ed948f33af
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876821"
---
# <span data-ttu-id="fba92-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="fba92-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="fba92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba92-102">SYNOPSIS</span></span>
<span data-ttu-id="fba92-103">장치에 대해 구성 된 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fba92-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="fba92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fba92-104">SYNTAX</span></span>

### <span data-ttu-id="fba92-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fba92-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba92-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba92-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba92-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba92-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba92-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fba92-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="fba92-109">설명은</span><span class="sxs-lookup"><span data-stu-id="fba92-109">DESCRIPTION</span></span>
<span data-ttu-id="fba92-110">**AzDataBoxEdgeUser** Cmdlet은 데이터 상자에 지 디바이스에 대해 구성 된 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="fba92-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="fba92-111">매개 변수에 이름을 언급 하 여 특정 사용자에 대 한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fba92-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="fba92-112">예제의</span><span class="sxs-lookup"><span data-stu-id="fba92-112">EXAMPLES</span></span>

### <span data-ttu-id="fba92-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="fba92-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="fba92-114">변수</span><span class="sxs-lookup"><span data-stu-id="fba92-114">PARAMETERS</span></span>

### <span data-ttu-id="fba92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba92-115">-DefaultProfile</span></span>
<span data-ttu-id="fba92-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fba92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba92-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="fba92-117">-DeviceName</span></span>
<span data-ttu-id="fba92-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="fba92-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba92-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fba92-119">-DeviceObject</span></span>
<span data-ttu-id="fba92-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="fba92-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fba92-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fba92-121">-Name</span></span>
<span data-ttu-id="fba92-122">사용자</span><span class="sxs-lookup"><span data-stu-id="fba92-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba92-123">-ResourceGroupName</span></span>
<span data-ttu-id="fba92-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fba92-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba92-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba92-125">-ResourceId</span></span>
<span data-ttu-id="fba92-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fba92-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fba92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba92-127">CommonParameters</span></span>
<span data-ttu-id="fba92-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fba92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba92-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fba92-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba92-130">입력</span><span class="sxs-lookup"><span data-stu-id="fba92-130">INPUTS</span></span>

### <span data-ttu-id="fba92-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fba92-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="fba92-132">출력</span><span class="sxs-lookup"><span data-stu-id="fba92-132">OUTPUTS</span></span>

### <span data-ttu-id="fba92-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="fba92-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="fba92-134">상속자</span><span class="sxs-lookup"><span data-stu-id="fba92-134">NOTES</span></span>

## <span data-ttu-id="fba92-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fba92-135">RELATED LINKS</span></span>