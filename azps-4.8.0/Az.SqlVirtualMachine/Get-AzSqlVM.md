---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213845"
---
# <span data-ttu-id="7edce-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="7edce-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="7edce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7edce-102">SYNOPSIS</span></span>
<span data-ttu-id="7edce-103">하나 이상의 sql 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="7edce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7edce-104">SYNTAX</span></span>

### <span data-ttu-id="7edce-105">ResourceGroupOnly (기본값)</span><span class="sxs-lookup"><span data-stu-id="7edce-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7edce-106">성을</span><span class="sxs-lookup"><span data-stu-id="7edce-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7edce-107">리소스</span><span class="sxs-lookup"><span data-stu-id="7edce-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7edce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7edce-108">DESCRIPTION</span></span>
<span data-ttu-id="7edce-109">Get-AzSqlVM cmdlet은 하나 이상의 sql 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="7edce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7edce-110">EXAMPLES</span></span>

### <span data-ttu-id="7edce-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7edce-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7edce-112">이 명령은 현재 구독의 모든 Azure SQL 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="7edce-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7edce-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7edce-114">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 현재 구독의 모든 Azure SQL 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="7edce-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7edce-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="7edce-116">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 SQL 가상 컴퓨터 "vm"에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="7edce-117">변수</span><span class="sxs-lookup"><span data-stu-id="7edce-117">PARAMETERS</span></span>

### <span data-ttu-id="7edce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7edce-118">-DefaultProfile</span></span>
<span data-ttu-id="7edce-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7edce-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7edce-120">-Name</span></span>
<span data-ttu-id="7edce-121">SQL 가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7edce-122">-ResourceGroupName</span></span>
<span data-ttu-id="7edce-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7edce-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7edce-124">-ResourceId</span></span>
<span data-ttu-id="7edce-125">SQL 가상 컴퓨터 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7edce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7edce-126">CommonParameters</span></span>
<span data-ttu-id="7edce-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7edce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7edce-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7edce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7edce-129">입력</span><span class="sxs-lookup"><span data-stu-id="7edce-129">INPUTS</span></span>

### <span data-ttu-id="7edce-130">않아야</span><span class="sxs-lookup"><span data-stu-id="7edce-130">None</span></span>

## <span data-ttu-id="7edce-131">출력</span><span class="sxs-lookup"><span data-stu-id="7edce-131">OUTPUTS</span></span>

### <span data-ttu-id="7edce-132">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="7edce-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="7edce-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7edce-133">NOTES</span></span>

## <span data-ttu-id="7edce-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7edce-134">RELATED LINKS</span></span>