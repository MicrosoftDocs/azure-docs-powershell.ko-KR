---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204817"
---
# <span data-ttu-id="e97e5-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e97e5-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="e97e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e97e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e97e5-103">SQL server의 키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="e97e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e97e5-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e97e5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e97e5-105">DESCRIPTION</span></span>
<span data-ttu-id="e97e5-106">Get-AzSqlServerKeyVaultKey cmdlet은 SQL server의 키 자격 증명 모음 키에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="e97e5-107">KeyId를 제공 하 여 서버의 모든 키를 보거나 특정 키를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="e97e5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e97e5-108">EXAMPLES</span></span>

### <span data-ttu-id="e97e5-109">예제 1: 모든 키 자격 증명 모음 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="e97e5-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e97e5-110">이 명령은 SQL server의 모든 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="e97e5-111">ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: contoso_contosokey_01234567890123456789012345678901 유형: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 지문: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00 AM ResourceGroupName: ContosoResourceGroup ServerName: ContosoServer ServerKeyName: Contoso_contosokey2_01234567890123456789012345678901 Type: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 지문: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00 AM</span><span class="sxs-lookup"><span data-stu-id="e97e5-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="e97e5-112">예제 2: 특정 키 보관소 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="e97e5-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="e97e5-113">이 명령은 Id가 ' ' 인 키 보관소 키를 가져온 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 다음 $MyServerKeyVaultKey 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="e97e5-114">$MyServerKeyVaultKey의 속성을 검사 하 여 키 자격 증명 모음에 대 한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="e97e5-115">변수</span><span class="sxs-lookup"><span data-stu-id="e97e5-115">PARAMETERS</span></span>

### <span data-ttu-id="e97e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97e5-116">-DefaultProfile</span></span>
<span data-ttu-id="e97e5-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e97e5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e97e5-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e97e5-118">-KeyId</span></span>
<span data-ttu-id="e97e5-119">Azure 키 자격 증명 모음 KeyId.</span><span class="sxs-lookup"><span data-stu-id="e97e5-119">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e97e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="e97e5-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-121">The name of the resource group</span></span>

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

### <span data-ttu-id="e97e5-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e97e5-122">-ServerName</span></span>
<span data-ttu-id="e97e5-123">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e97e5-124">-확인</span><span class="sxs-lookup"><span data-stu-id="e97e5-124">-Confirm</span></span>
<span data-ttu-id="e97e5-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e97e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e97e5-126">-WhatIf</span></span>
<span data-ttu-id="e97e5-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e97e5-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e97e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97e5-129">CommonParameters</span></span>
<span data-ttu-id="e97e5-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e97e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97e5-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e97e5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97e5-132">입력</span><span class="sxs-lookup"><span data-stu-id="e97e5-132">INPUTS</span></span>

### <span data-ttu-id="e97e5-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e97e5-133">System.String</span></span>

## <span data-ttu-id="e97e5-134">출력</span><span class="sxs-lookup"><span data-stu-id="e97e5-134">OUTPUTS</span></span>

### <span data-ttu-id="e97e5-135">ServerKeyVaultKey. AzureSqlServerKeyVaultKeyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e97e5-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="e97e5-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e97e5-136">NOTES</span></span>

## <span data-ttu-id="e97e5-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e97e5-137">RELATED LINKS</span></span>

[<span data-ttu-id="e97e5-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e97e5-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)