---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217356"
---
# <span data-ttu-id="4ab75-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ab75-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="4ab75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab75-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab75-103">유지 관리 구성 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ab75-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="4ab75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ab75-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ab75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ab75-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab75-106">유지 관리 구성 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ab75-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="4ab75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ab75-107">EXAMPLES</span></span>

### <span data-ttu-id="4ab75-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ab75-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="4ab75-109">유지 관리 구성 레코드 가져오기</span><span class="sxs-lookup"><span data-stu-id="4ab75-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="4ab75-110">변수</span><span class="sxs-lookup"><span data-stu-id="4ab75-110">PARAMETERS</span></span>

### <span data-ttu-id="4ab75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab75-111">-DefaultProfile</span></span>
<span data-ttu-id="4ab75-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ab75-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab75-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4ab75-113">-Name</span></span>
<span data-ttu-id="4ab75-114">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ab75-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab75-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab75-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ab75-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ab75-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab75-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab75-117">CommonParameters</span></span>
<span data-ttu-id="4ab75-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ab75-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab75-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ab75-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab75-120">입력</span><span class="sxs-lookup"><span data-stu-id="4ab75-120">INPUTS</span></span>

### <span data-ttu-id="4ab75-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ab75-121">System.String</span></span>

## <span data-ttu-id="4ab75-122">출력</span><span class="sxs-lookup"><span data-stu-id="4ab75-122">OUTPUTS</span></span>

### <span data-ttu-id="4ab75-123">PSMaintenanceConfiguration/. m m</span><span class="sxs-lookup"><span data-stu-id="4ab75-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="4ab75-124">상속자</span><span class="sxs-lookup"><span data-stu-id="4ab75-124">NOTES</span></span>

## <span data-ttu-id="4ab75-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ab75-125">RELATED LINKS</span></span>