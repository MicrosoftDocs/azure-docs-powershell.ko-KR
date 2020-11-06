---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 9abb97e5006f6572c7a0b08d8d25bcc55906a765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530351"
---
# <span data-ttu-id="77fc1-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="77fc1-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="77fc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="77fc1-103">새 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77fc1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77fc1-104">SYNTAX</span></span>

### <span data-ttu-id="77fc1-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="77fc1-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77fc1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fc1-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77fc1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77fc1-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77fc1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="77fc1-108">DESCRIPTION</span></span>
<span data-ttu-id="77fc1-109">New-AzureRmDataMigrationProject cmdlet은 새 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="77fc1-110">이 cmdlet은 Azure Resource 그룹의 이름, 새 프로젝트를 만들 Azure Data 마이그레이션 서비스의 이름, 프로젝트를 만들 지역, 새 프로젝트의 고유 이름, 원본 및 대상 연결 개체, 대상 형식 개체 (마이그레이션할 데이터베이스 목록에 대 한 입력) 등 필요한 모든 매개 변수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="77fc1-111">New-AzureRmDataMigrationConnectionInfo cmdlet을 사용 하 여 원본 및 대상 연결 모두에 대해 새 ConnectionInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="77fc1-112">선택한 데이터베이스에 대 한 DataMigration 정보 목록이 있어야 하는 경우 이 개체는 New-AzureRmDataMigrationDatabaseInfo cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="77fc1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="77fc1-113">EXAMPLES</span></span>

### <span data-ttu-id="77fc1-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="77fc1-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="77fc1-115">위 예제에서는 MyDMSProject 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 중앙 US 영역에 있는 새 프로젝트를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="77fc1-116">변수</span><span class="sxs-lookup"><span data-stu-id="77fc1-116">PARAMETERS</span></span>

### <span data-ttu-id="77fc1-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="77fc1-117">-DatabaseInfo</span></span>
<span data-ttu-id="77fc1-118">데이터베이스 Infos.</span><span class="sxs-lookup"><span data-stu-id="77fc1-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77fc1-119">-DefaultProfile</span></span>
<span data-ttu-id="77fc1-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77fc1-121">-InputObject</span></span>
<span data-ttu-id="77fc1-122">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="77fc1-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-123">-위치</span><span class="sxs-lookup"><span data-stu-id="77fc1-123">-Location</span></span>
<span data-ttu-id="77fc1-124">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="77fc1-125">-이름</span><span class="sxs-lookup"><span data-stu-id="77fc1-125">-Name</span></span>
<span data-ttu-id="77fc1-126">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77fc1-127">-ResourceGroupName</span></span>
<span data-ttu-id="77fc1-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77fc1-129">-ResourceId</span></span>
<span data-ttu-id="77fc1-130">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77fc1-131">-ServiceName</span></span>
<span data-ttu-id="77fc1-132">Azure 데이터베이스 마이그레이션 서비스 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="77fc1-133">-SourceConnection</span></span>
<span data-ttu-id="77fc1-134">원본 연결 정보</span><span class="sxs-lookup"><span data-stu-id="77fc1-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="77fc1-135">-SourceType</span></span>
<span data-ttu-id="77fc1-136">Project의 원본 플랫폼 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="77fc1-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="77fc1-137">-TargetConnection</span></span>
<span data-ttu-id="77fc1-138">대상 연결 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77fc1-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="77fc1-139">-TargetType</span></span>
<span data-ttu-id="77fc1-140">Project에 대 한 대상 플랫폼 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="77fc1-141">-확인</span><span class="sxs-lookup"><span data-stu-id="77fc1-141">-Confirm</span></span>
<span data-ttu-id="77fc1-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77fc1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77fc1-143">-WhatIf</span></span>
<span data-ttu-id="77fc1-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77fc1-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77fc1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77fc1-146">CommonParameters</span></span>
<span data-ttu-id="77fc1-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77fc1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77fc1-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77fc1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77fc1-149">입력</span><span class="sxs-lookup"><span data-stu-id="77fc1-149">INPUTS</span></span>

### <span data-ttu-id="77fc1-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="77fc1-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="77fc1-151">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77fc1-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="77fc1-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77fc1-152">System.String</span></span>

## <span data-ttu-id="77fc1-153">출력</span><span class="sxs-lookup"><span data-stu-id="77fc1-153">OUTPUTS</span></span>

### <span data-ttu-id="77fc1-154">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="77fc1-154">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="77fc1-155">상속자</span><span class="sxs-lookup"><span data-stu-id="77fc1-155">NOTES</span></span>

## <span data-ttu-id="77fc1-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77fc1-156">RELATED LINKS</span></span>