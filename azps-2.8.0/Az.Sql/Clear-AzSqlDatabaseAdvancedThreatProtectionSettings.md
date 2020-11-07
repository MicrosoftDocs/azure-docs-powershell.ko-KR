---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSettings.md
ms.openlocfilehash: f15ccf5c397ece13a034c99c29ac6cd5f18f9f58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873002"
---
# <span data-ttu-id="ae4bc-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="ae4bc-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="ae4bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4bc-103">데이터베이스에서 고급 위협 방지 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="ae4bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae4bc-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae4bc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4bc-106">**AzSqlDatabaseAdvancedThreatProtectionSettings** Cmdlet은 AZUREAZURE SQL 데이터베이스에서 고급 위협 방지 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSettings** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="ae4bc-107">이 cmdlet을 사용 하려면 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 하 여이 cmdlet이 설정을 제거 하는 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="ae4bc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ae4bc-108">EXAMPLES</span></span>

### <span data-ttu-id="ae4bc-109">예제 1: 데이터베이스에 대 한 고급 위협 방지 설정 제거</span><span class="sxs-lookup"><span data-stu-id="ae4bc-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ae4bc-110">이 명령은 Server01 이라는 서버의 Database01 이라는 데이터베이스에서 고급 위협 방지 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="ae4bc-111">변수</span><span class="sxs-lookup"><span data-stu-id="ae4bc-111">PARAMETERS</span></span>

### <span data-ttu-id="ae4bc-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae4bc-112">-DatabaseName</span></span>
<span data-ttu-id="ae4bc-113">고급 위협 방지 설정을 제거 해야 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="ae4bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4bc-114">-DefaultProfile</span></span>
<span data-ttu-id="ae4bc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ae4bc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae4bc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae4bc-116">-PassThru</span></span>
<span data-ttu-id="ae4bc-117">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae4bc-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae4bc-120">서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="ae4bc-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ae4bc-121">-ServerName</span></span>
<span data-ttu-id="ae4bc-122">데이터베이스가 실행 되는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="ae4bc-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ae4bc-123">-Confirm</span></span>
<span data-ttu-id="ae4bc-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae4bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4bc-125">-WhatIf</span></span>
<span data-ttu-id="ae4bc-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae4bc-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae4bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4bc-128">CommonParameters</span></span>
<span data-ttu-id="ae4bc-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4bc-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4bc-131">입력</span><span class="sxs-lookup"><span data-stu-id="ae4bc-131">INPUTS</span></span>

### <span data-ttu-id="ae4bc-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae4bc-132">System.String</span></span>

## <span data-ttu-id="ae4bc-133">출력</span><span class="sxs-lookup"><span data-stu-id="ae4bc-133">OUTPUTS</span></span>

### <span data-ttu-id="ae4bc-134">ThreatDetection. DatabaseThreatDetectionsettingsModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="ae4bc-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="ae4bc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ae4bc-135">NOTES</span></span>

## <span data-ttu-id="ae4bc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae4bc-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae4bc-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ae4bc-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

