---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 737b7170b774be712fb316f5c76b95d326e22fdb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345002"
---
# <span data-ttu-id="f95e4-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="f95e4-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="f95e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f95e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f95e4-103">Azure SQL Database를 .bacpac 파일로 저장소 계정으로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="f95e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="f95e4-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f95e4-105">설명</span><span class="sxs-lookup"><span data-stu-id="f95e4-105">DESCRIPTION</span></span>
<span data-ttu-id="f95e4-106">**New-AzSqlDatabaseExport** cmdlet은 Azure SQL Database를 .bacpac 파일로 저장소 계정으로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="f95e4-107">이 요청에 대한 상태 정보를 검색하기 위해 데이터베이스 내보내기 상태 요청 내보내기 요청을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="f95e4-108">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f95e4-109">이 cmdlet을 사용하려면 Azure SQL Server 방화벽을 "Azure 서비스 및 리소스가 이 서버에 액세스할 수 있도록 허용"으로 구성해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="f95e4-110">구성되지 않은 경우 GatewayTimeout 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="f95e4-111">예제</span><span class="sxs-lookup"><span data-stu-id="f95e4-111">EXAMPLES</span></span>

### <span data-ttu-id="f95e4-112">예제 1: 데이터베이스에 대한 내보내기 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="f95e4-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="f95e4-113">이 명령은 지정된 데이터베이스에 대한 내보내기 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="f95e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f95e4-114">PARAMETERS</span></span>

### <span data-ttu-id="f95e4-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="f95e4-115">-AdministratorLogin</span></span>
<span data-ttu-id="f95e4-116">사용자 지정 관리자의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="f95e4-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f95e4-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f95e4-118">사용자 지정 관리자의 암호를 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-118">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f95e4-119">-AuthenticationType</span></span>
<span data-ttu-id="f95e4-120">서버에 액세스하는 데 사용되는 인증 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="f95e4-121">인증 유형이 SQL 설정되어 있는 경우 기본값이 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="f95e4-122">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="f95e4-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f95e4-123">Sql.</span><span class="sxs-lookup"><span data-stu-id="f95e4-123">Sql.</span></span>
<span data-ttu-id="f95e4-124">SQL 인증을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-124">SQL authentication.</span></span>
<span data-ttu-id="f95e4-125">*AdministratorLogin* 및 *AdministratorLoginPassword를* 관리자 SQL 암호로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="f95e4-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="f95e4-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="f95e4-126">ADPassword.</span></span>
<span data-ttu-id="f95e4-127">Azure Active Directory 인증.</span><span class="sxs-lookup"><span data-stu-id="f95e4-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="f95e4-128">*AdministratorLogin 및* *AdministratorLoginPassword를* Azure AD 관리자 사용자 이름 및 암호로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="f95e4-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="f95e4-129">이 매개 변수는 데이터베이스 V12 SQL 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-129">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f95e4-130">-DatabaseName</span></span>
<span data-ttu-id="f95e4-131">SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="f95e4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95e4-132">-DefaultProfile</span></span>
<span data-ttu-id="f95e4-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f95e4-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f95e4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95e4-134">-ResourceGroupName</span></span>
<span data-ttu-id="f95e4-135">SQL 데이터베이스 서버에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="f95e4-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f95e4-136">-ServerName</span></span>
<span data-ttu-id="f95e4-137">SQL 데이터베이스 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="f95e4-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="f95e4-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="f95e4-139">개인 링크를 만드는 SQL Server 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f95e4-139">The sql server resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="f95e4-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="f95e4-141">개인 링크를 만드는 저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f95e4-141">The storage account resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="f95e4-142">-StorageKey</span></span>
<span data-ttu-id="f95e4-143">저장소 계정에 대한 액세스 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="f95e4-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f95e4-144">-StorageKeyType</span></span>
<span data-ttu-id="f95e4-145">저장소 계정에 대한 액세스 키의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="f95e4-146">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="f95e4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f95e4-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f95e4-147">StorageAccessKey.</span></span>
<span data-ttu-id="f95e4-148">이 값은 저장소 계정 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="f95e4-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="f95e4-149">SharedAccessKey.</span></span>
<span data-ttu-id="f95e4-150">이 값은 SAS(공유 액세스 서명) 키를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-150">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="f95e4-151">-StorageUri</span></span>
<span data-ttu-id="f95e4-152">.bacpac 파일에 대한 BLOB 링크를 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="f95e4-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="f95e4-154">설정된 경우 저장소 계정 및/또는 서버용 개인 SQL 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-154">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f95e4-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f95e4-155">-Confirm</span></span>
<span data-ttu-id="f95e4-156">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95e4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95e4-157">-WhatIf</span></span>
<span data-ttu-id="f95e4-158">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f95e4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95e4-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95e4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95e4-160">CommonParameters</span></span>
<span data-ttu-id="f95e4-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f95e4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95e4-162">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f95e4-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95e4-163">입력</span><span class="sxs-lookup"><span data-stu-id="f95e4-163">INPUTS</span></span>

### <span data-ttu-id="f95e4-164">System.String</span><span class="sxs-lookup"><span data-stu-id="f95e4-164">System.String</span></span>

## <span data-ttu-id="f95e4-165">출력</span><span class="sxs-lookup"><span data-stu-id="f95e4-165">OUTPUTS</span></span>

### <span data-ttu-id="f95e4-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="f95e4-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="f95e4-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f95e4-167">NOTES</span></span>
* <span data-ttu-id="f95e4-168">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="f95e4-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f95e4-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f95e4-169">RELATED LINKS</span></span>

[<span data-ttu-id="f95e4-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="f95e4-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="f95e4-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="f95e4-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="f95e4-172">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f95e4-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)