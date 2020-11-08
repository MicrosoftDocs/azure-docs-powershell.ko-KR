---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: a7aadc195be162db5f612dae47451f0b118fce19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048699"
---
# <span data-ttu-id="d1d1b-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d1d1b-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d1d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d1b-103">데이터베이스 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="d1d1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1d1b-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1d1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d1d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d1b-106">**AzSqlDatabaseGeoBackupPolicy** cmdlet은이 데이터베이스에 등록 된 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="d1d1b-107">백업 저장소 정책을 정의 하는 데 사용 되는 Azure Backup 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d1d1b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d1d1b-108">EXAMPLES</span></span>

### <span data-ttu-id="d1d1b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1d1b-109">Example 1</span></span>

<span data-ttu-id="d1d1b-110">데이터베이스 지역 백업 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-110">Gets a database geo backup policy.</span></span> <span data-ttu-id="d1d1b-111">생성</span><span class="sxs-lookup"><span data-stu-id="d1d1b-111">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlDatabaseGeoBackupPolicy -DatabaseName db1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="d1d1b-112">변수</span><span class="sxs-lookup"><span data-stu-id="d1d1b-112">PARAMETERS</span></span>

### <span data-ttu-id="d1d1b-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1d1b-113">-DatabaseName</span></span>
<span data-ttu-id="d1d1b-114">이 cmdlet이 지역 백업 정책을 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-114">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="d1d1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d1b-115">-DefaultProfile</span></span>
<span data-ttu-id="d1d1b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d1d1b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1d1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1d1b-118">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-118">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d1d1b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1d1b-119">-ServerName</span></span>
<span data-ttu-id="d1d1b-120">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d1d1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d1b-121">CommonParameters</span></span>
<span data-ttu-id="d1d1b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d1b-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1d1b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d1b-124">입력</span><span class="sxs-lookup"><span data-stu-id="d1d1b-124">INPUTS</span></span>

### <span data-ttu-id="d1d1b-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1d1b-125">System.String</span></span>

## <span data-ttu-id="d1d1b-126">출력</span><span class="sxs-lookup"><span data-stu-id="d1d1b-126">OUTPUTS</span></span>

### <span data-ttu-id="d1d1b-127">AzureSqlDatabaseGeoBackupPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="d1d1b-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="d1d1b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d1d1b-128">NOTES</span></span>

## <span data-ttu-id="d1d1b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1d1b-129">RELATED LINKS</span></span>

[<span data-ttu-id="d1d1b-130">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d1d1b-130">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d1d1b-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d1d1b-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)