---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: dc13bdaf737985f6769b3bb326201100204c6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528771"
---
# <span data-ttu-id="cadb7-101">Remove-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="cadb7-101">Remove-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="cadb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cadb7-102">SYNOPSIS</span></span>
<span data-ttu-id="cadb7-103">Azure SQL Server DNS 별칭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-103">Removes Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cadb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cadb7-104">SYNTAX</span></span>

### <span data-ttu-id="cadb7-105">Cmdlet 입력 매개 변수에서 서버 Dns 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="cadb7-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzureRmSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cadb7-106">AzureSqlServerDnsAliasModel 인스턴스 정의에서 서버 Dns 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="cadb7-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzureRmSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cadb7-107">Azure 리소스 id에서 서버 Dns 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="cadb7-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzureRmSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cadb7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cadb7-108">DESCRIPTION</span></span>
<span data-ttu-id="cadb7-109">이 명령은 서버에서 서버를 그대로 둔 채 Azure SQL Server DNS 별칭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="cadb7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cadb7-110">EXAMPLES</span></span>

### <span data-ttu-id="cadb7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cadb7-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="cadb7-112">서버에서 이름이 serverName 인 Azure SQL Server DNS 별칭을 aliasName로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="cadb7-113">변수</span><span class="sxs-lookup"><span data-stu-id="cadb7-113">PARAMETERS</span></span>

### <span data-ttu-id="cadb7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cadb7-114">-AsJob</span></span>
<span data-ttu-id="cadb7-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cadb7-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadb7-116">-DefaultProfile</span></span>
<span data-ttu-id="cadb7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cadb7-118">-Force</span></span>
<span data-ttu-id="cadb7-119">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="cadb7-119">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cadb7-120">-InputObject</span></span>
<span data-ttu-id="cadb7-121">제거할 서버 Dns 별칭 개체</span><span class="sxs-lookup"><span data-stu-id="cadb7-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="cadb7-122">-Name</span></span>
<span data-ttu-id="cadb7-123">Azure Sql Server Dns 별칭 이름</span><span class="sxs-lookup"><span data-stu-id="cadb7-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="cadb7-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-125">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cadb7-126">-ResourceId</span></span>
<span data-ttu-id="cadb7-127">제거할 서버 Dns 별칭 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cadb7-128">-ServerName</span></span>
<span data-ttu-id="cadb7-129">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-129">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-130">-확인</span><span class="sxs-lookup"><span data-stu-id="cadb7-130">-Confirm</span></span>
<span data-ttu-id="cadb7-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cadb7-132">-WhatIf</span></span>
<span data-ttu-id="cadb7-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadb7-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cadb7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadb7-135">CommonParameters</span></span>
<span data-ttu-id="cadb7-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cadb7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadb7-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadb7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadb7-138">입력</span><span class="sxs-lookup"><span data-stu-id="cadb7-138">INPUTS</span></span>

### <span data-ttu-id="cadb7-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cadb7-139">System.String</span></span>
<span data-ttu-id="cadb7-140">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="cadb7-140">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="cadb7-141">출력</span><span class="sxs-lookup"><span data-stu-id="cadb7-141">OUTPUTS</span></span>

### <span data-ttu-id="cadb7-142">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="cadb7-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="cadb7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="cadb7-143">NOTES</span></span>

## <span data-ttu-id="cadb7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cadb7-144">RELATED LINKS</span></span>