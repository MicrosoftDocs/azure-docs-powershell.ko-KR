---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: b604f0c154b24f8d50e6b341b1f39f8592981793
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873724"
---
# <span data-ttu-id="a7470-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a7470-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="a7470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7470-102">SYNOPSIS</span></span>
<span data-ttu-id="a7470-103">데이터베이스에 대 한 데이터 마스킹 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="a7470-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7470-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7470-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7470-105">DESCRIPTION</span></span>
<span data-ttu-id="a7470-106">**AzSqlDatabaseDataMaskingPolicy** Cmdlet은 Azure SQL 데이터베이스의 데이터 마스킹 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="a7470-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a7470-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a7470-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a7470-109">EXAMPLES</span></span>

### <span data-ttu-id="a7470-110">예제 1: Azure SQL 데이터베이스에 대 한 데이터 마스킹 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="a7470-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="a7470-111">이 명령은 서버 Server01의 리소스 그룹 ResourceGroup01에서 데이터베이스 Database01의 데이터 마스킹 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="a7470-112">변수</span><span class="sxs-lookup"><span data-stu-id="a7470-112">PARAMETERS</span></span>

### <span data-ttu-id="a7470-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7470-113">-DatabaseName</span></span>
<span data-ttu-id="a7470-114">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-114">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7470-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7470-115">-DefaultProfile</span></span>
<span data-ttu-id="a7470-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a7470-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7470-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7470-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7470-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a7470-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7470-119">-ServerName</span></span>
<span data-ttu-id="a7470-120">데이터베이스가 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-120">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7470-121">-확인</span><span class="sxs-lookup"><span data-stu-id="a7470-121">-Confirm</span></span>
<span data-ttu-id="a7470-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7470-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7470-123">-WhatIf</span></span>
<span data-ttu-id="a7470-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7470-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7470-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7470-126">CommonParameters</span></span>
<span data-ttu-id="a7470-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7470-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7470-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a7470-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7470-129">입력</span><span class="sxs-lookup"><span data-stu-id="a7470-129">INPUTS</span></span>

### <span data-ttu-id="a7470-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7470-130">System.String</span></span>

## <span data-ttu-id="a7470-131">출력</span><span class="sxs-lookup"><span data-stu-id="a7470-131">OUTPUTS</span></span>

### <span data-ttu-id="a7470-132">DataMasking. DatabaseDataMaskingPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a7470-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="a7470-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a7470-133">NOTES</span></span>

## <span data-ttu-id="a7470-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7470-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7470-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7470-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a7470-136">새로운 AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7470-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a7470-137">제거-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7470-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a7470-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a7470-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a7470-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a7470-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

