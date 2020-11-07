---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 8b969a3942f72da522937f06621e11c0d8cff32f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873662"
---
# <span data-ttu-id="eac78-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="eac78-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="eac78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eac78-102">SYNOPSIS</span></span>
<span data-ttu-id="eac78-103">탄력적 풀 추천 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="eac78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eac78-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac78-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eac78-105">DESCRIPTION</span></span>
<span data-ttu-id="eac78-106">**AzSqlElasticPoolRecommendation** cmdlet은 서버에 대 한 탄력적 풀 추천 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="eac78-107">이러한 권장 사항에는 다음 값이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="eac78-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="eac78-108">DatabaseCollection.</span></span> <span data-ttu-id="eac78-109">풀에 속한 데이터베이스 이름의 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="eac78-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="eac78-110">DatabaseDtuMin.</span></span> <span data-ttu-id="eac78-111">탄력적 풀의 데이터베이스에 대 한 DTU (데이터 전송 단위) 보장.</span><span class="sxs-lookup"><span data-stu-id="eac78-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="eac78-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="eac78-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="eac78-113">탄력적 풀의 데이터베이스에 대 한 DTU 캡입니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="eac78-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="eac78-114">Dtu.</span></span> <span data-ttu-id="eac78-115">탄력적 풀에 대 한 DTU 보증입니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="eac78-116">StorageMb</span><span class="sxs-lookup"><span data-stu-id="eac78-116">StorageMb.</span></span> <span data-ttu-id="eac78-117">탄력적 풀의 저장소 (mb)입니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="eac78-118">평가판.</span><span class="sxs-lookup"><span data-stu-id="eac78-118">Edition.</span></span> <span data-ttu-id="eac78-119">탄력적 풀 용 에디션.</span><span class="sxs-lookup"><span data-stu-id="eac78-119">Edition for the elastic pool.</span></span> <span data-ttu-id="eac78-120">이 매개 변수에 허용 되는 값은 Basic, Standard 및 Premium입니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="eac78-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="eac78-121">IncludeAllDatabases.</span></span> <span data-ttu-id="eac78-122">탄력적 풀의 모든 데이터베이스가 반환 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="eac78-123">성을.</span><span class="sxs-lookup"><span data-stu-id="eac78-123">Name.</span></span> <span data-ttu-id="eac78-124">탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="eac78-125">예제의</span><span class="sxs-lookup"><span data-stu-id="eac78-125">EXAMPLES</span></span>

### <span data-ttu-id="eac78-126">예제 1: 서버에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="eac78-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="eac78-127">이 명령은 Server01 이라는 서버에 대 한 탄력적 풀 권장 사항을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="eac78-128">변수</span><span class="sxs-lookup"><span data-stu-id="eac78-128">PARAMETERS</span></span>

### <span data-ttu-id="eac78-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac78-129">-DefaultProfile</span></span>
<span data-ttu-id="eac78-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eac78-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eac78-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac78-131">-ResourceGroupName</span></span>
<span data-ttu-id="eac78-132">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eac78-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eac78-133">-ServerName</span></span>
<span data-ttu-id="eac78-134">이 cmdlet이 권장 사항을 제공 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="eac78-135">-확인</span><span class="sxs-lookup"><span data-stu-id="eac78-135">-Confirm</span></span>
<span data-ttu-id="eac78-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac78-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac78-137">-WhatIf</span></span>
<span data-ttu-id="eac78-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac78-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac78-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac78-140">CommonParameters</span></span>
<span data-ttu-id="eac78-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eac78-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac78-142">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eac78-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac78-143">입력</span><span class="sxs-lookup"><span data-stu-id="eac78-143">INPUTS</span></span>

### <span data-ttu-id="eac78-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eac78-144">System.String</span></span>

## <span data-ttu-id="eac78-145">출력</span><span class="sxs-lookup"><span data-stu-id="eac78-145">OUTPUTS</span></span>

### <span data-ttu-id="eac78-146">LegacySdk. UpgradeRecommendedElasticPoolProperties를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="eac78-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="eac78-147">상속자</span><span class="sxs-lookup"><span data-stu-id="eac78-147">NOTES</span></span>

## <span data-ttu-id="eac78-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eac78-148">RELATED LINKS</span></span>