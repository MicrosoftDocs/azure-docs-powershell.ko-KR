---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350133"
---
# <span data-ttu-id="83b6e-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="83b6e-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="83b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="83b6e-103">데이터베이스 서버에 대한 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="83b6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="83b6e-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b6e-105">설명</span><span class="sxs-lookup"><span data-stu-id="83b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="83b6e-106">**Get-AzSqlServer** cmdlet은 하나 이상의 Azure SQL 데이터베이스 서버에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="83b6e-107">해당 서버에 대한 정보만 표시하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="83b6e-108">예제</span><span class="sxs-lookup"><span data-stu-id="83b6e-108">EXAMPLES</span></span>

### <span data-ttu-id="83b6e-109">예제 1: 리소스 그룹에 할당된 SQL Server 인스턴스를 모두 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="83b6e-110">이 명령은 리소스 그룹에 할당된 모든 Azure SQL Database 서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="83b6e-111">예제 2: Azure SQL Database 서버에 대한 정보 얻음</span><span class="sxs-lookup"><span data-stu-id="83b6e-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="83b6e-112">이 명령은 Server01이라는 Azure SQL Database 서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="83b6e-113">예제 3: 구독에서 SQL Server 인스턴스를 모두 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="83b6e-114">이 명령은 현재 구독의 모든 Azure SQL Database 서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="83b6e-115">예제 4: 필터링을 사용하여 리소스 SQL Server 할당된 리소스의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="83b6e-116">이 명령은 "server"로 시작하는 ResourceGroup01 리소스 그룹에 할당된 모든 Azure SQL Database 서버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="83b6e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83b6e-117">PARAMETERS</span></span>

### <span data-ttu-id="83b6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b6e-118">-DefaultProfile</span></span>
<span data-ttu-id="83b6e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="83b6e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83b6e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b6e-120">-ResourceGroupName</span></span>
<span data-ttu-id="83b6e-121">서버를 할당할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-121">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="83b6e-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83b6e-122">-ServerName</span></span>
<span data-ttu-id="83b6e-123">이 cmdlet이 얻을 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83b6e-124">-Confirm</span></span>
<span data-ttu-id="83b6e-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b6e-126">-WhatIf</span></span>
<span data-ttu-id="83b6e-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="83b6e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b6e-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b6e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b6e-129">CommonParameters</span></span>
<span data-ttu-id="83b6e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83b6e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b6e-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83b6e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b6e-132">입력</span><span class="sxs-lookup"><span data-stu-id="83b6e-132">INPUTS</span></span>

### <span data-ttu-id="83b6e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="83b6e-133">System.String</span></span>

## <span data-ttu-id="83b6e-134">출력</span><span class="sxs-lookup"><span data-stu-id="83b6e-134">OUTPUTS</span></span>

### <span data-ttu-id="83b6e-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="83b6e-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="83b6e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83b6e-136">NOTES</span></span>

## <span data-ttu-id="83b6e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83b6e-137">RELATED LINKS</span></span>

[<span data-ttu-id="83b6e-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="83b6e-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="83b6e-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="83b6e-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="83b6e-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="83b6e-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="83b6e-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="83b6e-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

