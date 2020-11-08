---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056951"
---
# <span data-ttu-id="54add-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="54add-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="54add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54add-102">SYNOPSIS</span></span>
<span data-ttu-id="54add-103">Azure SQL Server 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="54add-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="54add-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54add-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54add-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54add-105">DESCRIPTION</span></span>
<span data-ttu-id="54add-106">이 명령은 Azure SQL Server 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="54add-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="54add-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54add-107">EXAMPLES</span></span>

### <span data-ttu-id="54add-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="54add-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="54add-109">기존 Azure SQL Server 가상 네트워크 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="54add-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="54add-110">변수</span><span class="sxs-lookup"><span data-stu-id="54add-110">PARAMETERS</span></span>

### <span data-ttu-id="54add-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54add-111">-AsJob</span></span>
<span data-ttu-id="54add-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="54add-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54add-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54add-113">-DefaultProfile</span></span>
<span data-ttu-id="54add-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54add-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54add-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54add-115">-ResourceGroupName</span></span>
<span data-ttu-id="54add-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54add-116">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54add-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="54add-117">-ServerName</span></span>
<span data-ttu-id="54add-118">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54add-118">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54add-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="54add-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="54add-120">Azure Sql Server 가상 네트워크 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="54add-120">Azure Sql Server Virtual Network Rule name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54add-121">-확인</span><span class="sxs-lookup"><span data-stu-id="54add-121">-Confirm</span></span>
<span data-ttu-id="54add-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54add-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54add-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54add-123">-WhatIf</span></span>
<span data-ttu-id="54add-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54add-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54add-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54add-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54add-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54add-126">CommonParameters</span></span>
<span data-ttu-id="54add-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54add-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54add-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="54add-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54add-129">입력</span><span class="sxs-lookup"><span data-stu-id="54add-129">INPUTS</span></span>

### <span data-ttu-id="54add-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="54add-130">System.String</span></span>

## <span data-ttu-id="54add-131">출력</span><span class="sxs-lookup"><span data-stu-id="54add-131">OUTPUTS</span></span>

### <span data-ttu-id="54add-132">VirtualNetworkRule. AzureSqlServerVirtualNetworkRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="54add-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="54add-133">상속자</span><span class="sxs-lookup"><span data-stu-id="54add-133">NOTES</span></span>

## <span data-ttu-id="54add-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54add-134">RELATED LINKS</span></span>