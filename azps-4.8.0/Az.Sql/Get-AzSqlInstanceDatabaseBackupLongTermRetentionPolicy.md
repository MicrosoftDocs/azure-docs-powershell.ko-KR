---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213251"
---
# <span data-ttu-id="8541c-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8541c-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="8541c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8541c-102">SYNOPSIS</span></span>
<span data-ttu-id="8541c-103">관리 데이터베이스의 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="8541c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8541c-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8541c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8541c-105">DESCRIPTION</span></span>
<span data-ttu-id="8541c-106">**AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet은이 관리 데이터베이스에 등록 된 장기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="8541c-107">정책은 백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="8541c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8541c-108">EXAMPLES</span></span>

### <span data-ttu-id="8541c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8541c-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="8541c-110">데이터베이스에 대 한 장기 보존 정책의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="8541c-111">변수</span><span class="sxs-lookup"><span data-stu-id="8541c-111">PARAMETERS</span></span>

### <span data-ttu-id="8541c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8541c-112">-DatabaseName</span></span>
<span data-ttu-id="8541c-113">사용할 Azure 관리 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="8541c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8541c-114">-DefaultProfile</span></span>
<span data-ttu-id="8541c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8541c-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8541c-116">-InstanceName</span></span>
<span data-ttu-id="8541c-117">데이터베이스가 속한 Azure 관리 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="8541c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8541c-118">-ResourceGroupName</span></span>
<span data-ttu-id="8541c-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="8541c-120">-확인</span><span class="sxs-lookup"><span data-stu-id="8541c-120">-Confirm</span></span>
<span data-ttu-id="8541c-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8541c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8541c-122">-WhatIf</span></span>
<span data-ttu-id="8541c-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8541c-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8541c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8541c-125">CommonParameters</span></span>
<span data-ttu-id="8541c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8541c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8541c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8541c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8541c-128">입력</span><span class="sxs-lookup"><span data-stu-id="8541c-128">INPUTS</span></span>

### <span data-ttu-id="8541c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8541c-129">System.String</span></span>

## <span data-ttu-id="8541c-130">출력</span><span class="sxs-lookup"><span data-stu-id="8541c-130">OUTPUTS</span></span>

### <span data-ttu-id="8541c-131">AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel (\*). m. ManagedDatabaseBackup.</span><span class="sxs-lookup"><span data-stu-id="8541c-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="8541c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8541c-132">NOTES</span></span>

## <span data-ttu-id="8541c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8541c-133">RELATED LINKS</span></span>

[<span data-ttu-id="8541c-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8541c-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8541c-135">제거-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8541c-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8541c-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8541c-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8541c-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8541c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)