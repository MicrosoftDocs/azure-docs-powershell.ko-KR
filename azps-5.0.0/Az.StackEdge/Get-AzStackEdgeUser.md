---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216629"
---
# <span data-ttu-id="f513b-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="f513b-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="f513b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f513b-102">SYNOPSIS</span></span>
<span data-ttu-id="f513b-103">장치에 대해 구성 된 사용자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f513b-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="f513b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f513b-104">SYNTAX</span></span>

### <span data-ttu-id="f513b-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f513b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f513b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f513b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f513b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f513b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f513b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f513b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f513b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="f513b-109">DESCRIPTION</span></span>
<span data-ttu-id="f513b-110">**AzStackEdgeUser** Cmdlet은 스택 경계 장치에 대해 구성 된 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f513b-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="f513b-111">매개 변수에 이름을 언급 하 여 특정 사용자에 대 한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f513b-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="f513b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f513b-112">EXAMPLES</span></span>

### <span data-ttu-id="f513b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f513b-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="f513b-114">변수</span><span class="sxs-lookup"><span data-stu-id="f513b-114">PARAMETERS</span></span>

### <span data-ttu-id="f513b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f513b-115">-DefaultProfile</span></span>
<span data-ttu-id="f513b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f513b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f513b-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="f513b-117">-DeviceName</span></span>
<span data-ttu-id="f513b-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="f513b-118">Device Name</span></span>

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

### <span data-ttu-id="f513b-119">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f513b-119">-DeviceObject</span></span>
<span data-ttu-id="f513b-120">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="f513b-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f513b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f513b-121">-Name</span></span>
<span data-ttu-id="f513b-122">사용자</span><span class="sxs-lookup"><span data-stu-id="f513b-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f513b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f513b-123">-ResourceGroupName</span></span>
<span data-ttu-id="f513b-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f513b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f513b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f513b-125">-ResourceId</span></span>
<span data-ttu-id="f513b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f513b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="f513b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f513b-127">CommonParameters</span></span>
<span data-ttu-id="f513b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f513b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f513b-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f513b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f513b-130">입력</span><span class="sxs-lookup"><span data-stu-id="f513b-130">INPUTS</span></span>

### <span data-ttu-id="f513b-131">StackEdge. PSStackEdgeDevice에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="f513b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="f513b-132">출력</span><span class="sxs-lookup"><span data-stu-id="f513b-132">OUTPUTS</span></span>

### <span data-ttu-id="f513b-133">StackEdge. PSStackEdgeUser에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="f513b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="f513b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f513b-134">NOTES</span></span>

## <span data-ttu-id="f513b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f513b-135">RELATED LINKS</span></span>