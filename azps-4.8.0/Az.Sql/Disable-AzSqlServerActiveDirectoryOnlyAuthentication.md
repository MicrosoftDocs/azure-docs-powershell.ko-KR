---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 8d9214b44d5e408717968d042a1cdb86cd25130a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047575"
---
# <span data-ttu-id="7bcb7-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7bcb7-101">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="7bcb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bcb7-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcb7-103">특정 SQL Server에 대해 Azure AD 전용 인증을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-103">Disables Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="7bcb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7bcb7-104">SYNTAX</span></span>

### <span data-ttu-id="7bcb7-105">UseResourceGroupAndServerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7bcb7-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcb7-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bcb7-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bcb7-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bcb7-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bcb7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7bcb7-108">DESCRIPTION</span></span>
<span data-ttu-id="7bcb7-109">**AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet은 현재 구독의 AzureSQL 서버에 대 한 azure AD (Active Directory) 인증 요구 사항만 사용할 수 없도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-109">The **Disable-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="7bcb7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7bcb7-110">EXAMPLES</span></span>

### <span data-ttu-id="7bcb7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7bcb7-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   False
```

<span data-ttu-id="7bcb7-112">이 명령은 ResourceGroup01 이라는 리소스 그룹과 연결 된 Server01 이라는 AzureSQL server에 대해 azure AD (Active Directory)만 인증 요구 사항을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="7bcb7-113">변수</span><span class="sxs-lookup"><span data-stu-id="7bcb7-113">PARAMETERS</span></span>

### <span data-ttu-id="7bcb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcb7-114">-DefaultProfile</span></span>
<span data-ttu-id="7bcb7-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bcb7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bcb7-116">-InputObject</span></span>
<span data-ttu-id="7bcb7-117">사용할 SQL server 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcb7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bcb7-118">-ResourceGroupName</span></span>
<span data-ttu-id="7bcb7-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcb7-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bcb7-120">-ResourceId</span></span>
<span data-ttu-id="7bcb7-121">사용할 인스턴스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcb7-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7bcb7-122">-ServerName</span></span>
<span data-ttu-id="7bcb7-123">Azure Active Directory만 인증을 하는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bcb7-124">-확인</span><span class="sxs-lookup"><span data-stu-id="7bcb7-124">-Confirm</span></span>
<span data-ttu-id="7bcb7-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bcb7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcb7-126">-WhatIf</span></span>
<span data-ttu-id="7bcb7-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bcb7-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bcb7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcb7-129">CommonParameters</span></span>
<span data-ttu-id="7bcb7-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcb7-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7bcb7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcb7-132">입력</span><span class="sxs-lookup"><span data-stu-id="7bcb7-132">INPUTS</span></span>

### <span data-ttu-id="7bcb7-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7bcb7-133">System.String</span></span>

## <span data-ttu-id="7bcb7-134">출력</span><span class="sxs-lookup"><span data-stu-id="7bcb7-134">OUTPUTS</span></span>

### <span data-ttu-id="7bcb7-135">ServerActiveDirectoryAdministrator. AzureSqlServerActiveDirectoryOnlyAuthenticationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="7bcb7-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="7bcb7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="7bcb7-136">NOTES</span></span>

## <span data-ttu-id="7bcb7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bcb7-137">RELATED LINKS</span></span>

[<span data-ttu-id="7bcb7-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7bcb7-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7bcb7-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="7bcb7-139">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="7bcb7-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7bcb7-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="7bcb7-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7bcb7-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="7bcb7-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7bcb7-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)