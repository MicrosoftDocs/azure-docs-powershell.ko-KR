---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216946"
---
# <span data-ttu-id="a814d-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="a814d-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="a814d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a814d-102">SYNOPSIS</span></span>
<span data-ttu-id="a814d-103">Sql 가상 컴퓨터에 대 한 새 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="a814d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a814d-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a814d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a814d-105">DESCRIPTION</span></span>
<span data-ttu-id="a814d-106">New-AzSqlVMConfig cmdlet은 sql 가상 컴퓨터에 대 한 새 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="a814d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a814d-107">EXAMPLES</span></span>

### <span data-ttu-id="a814d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a814d-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="a814d-109">Azure sql 가상 컴퓨터를 만들기 위해 사용할 수 있는 sql 가상 컴퓨터의 로컬 구성 가능 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="a814d-110">변수</span><span class="sxs-lookup"><span data-stu-id="a814d-110">PARAMETERS</span></span>

### <span data-ttu-id="a814d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a814d-111">-DefaultProfile</span></span>
<span data-ttu-id="a814d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a814d-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a814d-113">-LicenseType</span></span>
<span data-ttu-id="a814d-114">SQL 가상 컴퓨터 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a814d-115">-제공</span><span class="sxs-lookup"><span data-stu-id="a814d-115">-Offer</span></span>
<span data-ttu-id="a814d-116">SQL 가상 컴퓨터 제공</span><span class="sxs-lookup"><span data-stu-id="a814d-116">SQL virtual machine offer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a814d-117">-Sku</span><span class="sxs-lookup"><span data-stu-id="a814d-117">-Sku</span></span>
<span data-ttu-id="a814d-118">SQL virtual machine edition 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-118">SQL virtual machine edition type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a814d-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="a814d-119">-SqlManagementType</span></span>
<span data-ttu-id="a814d-120">SQL 가상 컴퓨터 관리 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-120">SQL virtual machine management type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a814d-121">태그</span><span class="sxs-lookup"><span data-stu-id="a814d-121">-Tag</span></span>
<span data-ttu-id="a814d-122">SQL 가상 컴퓨터와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="a814d-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a814d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a814d-123">CommonParameters</span></span>
<span data-ttu-id="a814d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a814d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a814d-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a814d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a814d-126">입력</span><span class="sxs-lookup"><span data-stu-id="a814d-126">INPUTS</span></span>

### <span data-ttu-id="a814d-127">않아야</span><span class="sxs-lookup"><span data-stu-id="a814d-127">None</span></span>

## <span data-ttu-id="a814d-128">출력</span><span class="sxs-lookup"><span data-stu-id="a814d-128">OUTPUTS</span></span>

### <span data-ttu-id="a814d-129">SqlVirtualMachine를 SqlVirtualMachine 합니다. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="a814d-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="a814d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a814d-130">NOTES</span></span>

## <span data-ttu-id="a814d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a814d-131">RELATED LINKS</span></span>