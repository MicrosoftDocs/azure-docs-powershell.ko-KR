---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340581"
---
# <span data-ttu-id="6166d-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="6166d-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="6166d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6166d-102">SYNOPSIS</span></span>
<span data-ttu-id="6166d-103">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="6166d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6166d-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6166d-105">설명</span><span class="sxs-lookup"><span data-stu-id="6166d-105">DESCRIPTION</span></span>
<span data-ttu-id="6166d-106">주어진 서버에 대한 모든 복제본을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="6166d-107">예제</span><span class="sxs-lookup"><span data-stu-id="6166d-107">EXAMPLES</span></span>

### <span data-ttu-id="6166d-108">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 복제본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6166d-109">이 cmdlet은 리소스 그룹 및 서버 이름으로 PostgreSql 서버 복제본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="6166d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6166d-110">PARAMETERS</span></span>

### <span data-ttu-id="6166d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6166d-111">-DefaultProfile</span></span>
<span data-ttu-id="6166d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6166d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6166d-113">-ResourceGroupName</span></span>
<span data-ttu-id="6166d-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-114">The name of the resource group.</span></span>
<span data-ttu-id="6166d-115">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6166d-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6166d-116">-ServerName</span></span>
<span data-ttu-id="6166d-117">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-117">The name of the server.</span></span>

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

### <span data-ttu-id="6166d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6166d-118">-SubscriptionId</span></span>
<span data-ttu-id="6166d-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6166d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6166d-120">CommonParameters</span></span>
<span data-ttu-id="6166d-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6166d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6166d-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6166d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6166d-123">입력</span><span class="sxs-lookup"><span data-stu-id="6166d-123">INPUTS</span></span>

## <span data-ttu-id="6166d-124">출력</span><span class="sxs-lookup"><span data-stu-id="6166d-124">OUTPUTS</span></span>

### <span data-ttu-id="6166d-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="6166d-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6166d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6166d-126">NOTES</span></span>

<span data-ttu-id="6166d-127">별칭</span><span class="sxs-lookup"><span data-stu-id="6166d-127">ALIASES</span></span>

## <span data-ttu-id="6166d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6166d-128">RELATED LINKS</span></span>
