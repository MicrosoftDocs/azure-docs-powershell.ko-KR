---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212279"
---
# <span data-ttu-id="a6b24-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="a6b24-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="a6b24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6b24-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b24-103">원본 데이터베이스 백업을 수행할 로컬 네트워크 공유를 지정 하는 Azure 데이터베이스 마이그레이션 서비스에 대 한 데이터 공유 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6b24-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="a6b24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6b24-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6b24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6b24-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b24-106">New-AzDataMigrationFileShare cmdlet은 Azure 데이터베이스 마이그레이션 서비스에서 원본 데이터베이스 백업을 수행할 수 있는 로컬 네트워크 공유를 지정 하는 공유 되지 않는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a6b24-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="a6b24-107">원본 SQL Server 인스턴스를 실행 하는 서비스 계정에이 네트워크 공유에 대 한 쓰기 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b24-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="a6b24-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a6b24-108">EXAMPLES</span></span>

### <span data-ttu-id="a6b24-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6b24-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="a6b24-110">변수</span><span class="sxs-lookup"><span data-stu-id="a6b24-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b24-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="a6b24-111">-Credential</span></span>
<span data-ttu-id="a6b24-112">파일 공유에 액세스 하기 위한 자격 증명</span><span class="sxs-lookup"><span data-stu-id="a6b24-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6b24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b24-113">-DefaultProfile</span></span>
<span data-ttu-id="a6b24-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6b24-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6b24-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a6b24-115">-Path</span></span>
<span data-ttu-id="a6b24-116">파일 공유 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a6b24-116">File share path.</span></span>

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

### <span data-ttu-id="a6b24-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b24-117">CommonParameters</span></span>
<span data-ttu-id="a6b24-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6b24-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b24-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6b24-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b24-120">입력</span><span class="sxs-lookup"><span data-stu-id="a6b24-120">INPUTS</span></span>

### <span data-ttu-id="a6b24-121">않아야</span><span class="sxs-lookup"><span data-stu-id="a6b24-121">None</span></span>

## <span data-ttu-id="a6b24-122">출력</span><span class="sxs-lookup"><span data-stu-id="a6b24-122">OUTPUTS</span></span>

### <span data-ttu-id="a6b24-123">DataMigration. MigrateSqlServerSqlDbDatabaseInput/.</span><span class="sxs-lookup"><span data-stu-id="a6b24-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="a6b24-124">상속자</span><span class="sxs-lookup"><span data-stu-id="a6b24-124">NOTES</span></span>

## <span data-ttu-id="a6b24-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6b24-125">RELATED LINKS</span></span>