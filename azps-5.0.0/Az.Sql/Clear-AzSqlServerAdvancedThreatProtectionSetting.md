---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8ff7e7df12bc1415cfe6e4b14dc673e93d8d8791
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217002"
---
# <span data-ttu-id="9ec4c-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="9ec4c-101">Clear-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="9ec4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ec4c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec4c-103">서버에서 고급 위협 방지 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-103">Removes the advanced threat protection settings from a server.</span></span>

## <span data-ttu-id="9ec4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ec4c-104">SYNTAX</span></span>

```
Clear-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec4c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ec4c-105">DESCRIPTION</span></span>
<span data-ttu-id="9ec4c-106">Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet은 Azure SQL server에서 고급 위협 방지 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-106">The Clear-AzSqlServerAdvancedThreatProtectionSetting cmdlet removes the advanced threat protection settings from an Azure SQL server.</span></span>
<span data-ttu-id="9ec4c-107">이 cmdlet을 사용 하려면 ResourceGroupName 및 ServerName 매개 변수를 지정 하 여이 cmdlet이 설정을 제거 하는 서버를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="9ec4c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9ec4c-108">EXAMPLES</span></span>

### <span data-ttu-id="9ec4c-109">예제 1: 데이터베이스에 대 한 고급 위협 방지 설정 제거</span><span class="sxs-lookup"><span data-stu-id="9ec4c-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\> Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="9ec4c-110">이 명령은 Server01 이라는 서버에서 고급 위협 방지 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-110">This command removes the advanced threat protection settings from a server named Server01.</span></span>

## <span data-ttu-id="9ec4c-111">변수</span><span class="sxs-lookup"><span data-stu-id="9ec4c-111">PARAMETERS</span></span>

### <span data-ttu-id="9ec4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec4c-112">-DefaultProfile</span></span>
<span data-ttu-id="9ec4c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ec4c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ec4c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ec4c-114">-PassThru</span></span>
<span data-ttu-id="9ec4c-115">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ec4c-116">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ec4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ec4c-118">서버가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="9ec4c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9ec4c-119">-ServerName</span></span>
<span data-ttu-id="9ec4c-120">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec4c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="9ec4c-121">-Confirm</span></span>
<span data-ttu-id="9ec4c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ec4c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec4c-123">-WhatIf</span></span>
<span data-ttu-id="9ec4c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ec4c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ec4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec4c-126">CommonParameters</span></span>
<span data-ttu-id="9ec4c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec4c-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ec4c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec4c-129">입력</span><span class="sxs-lookup"><span data-stu-id="9ec4c-129">INPUTS</span></span>

### <span data-ttu-id="9ec4c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ec4c-130">System.String</span></span>

## <span data-ttu-id="9ec4c-131">출력</span><span class="sxs-lookup"><span data-stu-id="9ec4c-131">OUTPUTS</span></span>

### <span data-ttu-id="9ec4c-132">ThreatDetection. ServerThreatDetectionsettingsModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9ec4c-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="9ec4c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="9ec4c-133">NOTES</span></span>

## <span data-ttu-id="9ec4c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ec4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ec4c-135">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9ec4c-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
