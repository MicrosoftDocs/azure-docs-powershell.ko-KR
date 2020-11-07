---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTask.md
ms.openlocfilehash: 9d1ce9dc517e550fdfada1db000657aedc15c6ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873194"
---
# <span data-ttu-id="b4d2c-101">Get-AzSecurityTask</span><span class="sxs-lookup"><span data-stu-id="b4d2c-101">Get-AzSecurityTask</span></span>

## <span data-ttu-id="b4d2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d2c-103">Azure 보안 센터에서 보안 환경을 강화 하기 위해 수행할 작업을 권장 하는 보안 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-103">Gets the security tasks that Azure Security Center recommends you to do in order to strengthen your security posture.</span></span>

## <span data-ttu-id="b4d2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4d2c-104">SYNTAX</span></span>

### <span data-ttu-id="b4d2c-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4d2c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTask [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d2c-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="b4d2c-106">ResourceGroupScope</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d2c-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b4d2c-107">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTask -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d2c-108">구독 Levelresource</span><span class="sxs-lookup"><span data-stu-id="b4d2c-108">SubscriptionLevelResource</span></span>
```
Get-AzSecurityTask -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4d2c-109">리소스</span><span class="sxs-lookup"><span data-stu-id="b4d2c-109">ResourceId</span></span>
```
Get-AzSecurityTask -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d2c-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b4d2c-110">DESCRIPTION</span></span>
<span data-ttu-id="b4d2c-111">Azure 보안 센터는 리소스를 검사 하 여 잠재적인 보안 문제를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-111">Azure Security Center scans your resources to detect potential security issues.</span></span>
<span data-ttu-id="b4d2c-112">이 cmdlet을 사용 하면 Azure 보안 센터에서 수행할 것을 권장 하는 보안 작업을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-112">This cmdlet lets you discover the security tasks that Azure Security Center recommends you to do.</span></span>

## <span data-ttu-id="b4d2c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b4d2c-113">EXAMPLES</span></span>

### <span data-ttu-id="b4d2c-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4d2c-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTask
Id                                                                                                                                              Name                                 RecommendationType                                  ResourceId
--                                                                                                                                              ----                                 ------------------                                  ----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/08357a1e-c534-756f-cbb9-7b45e73f3137 08357a1e-c534-756f-cbb9-7b45e73f3137 Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/0876feac-8c60-3fef-d95e-2c43b333ff14 0876feac-8c60-3fef-d95e-2c43b333ff14 Antimalware Health Issues                           /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/09ea0fa9-ce5a-d703-e17b-08f1d5246e2c 09ea0fa9-ce5a-d703-e17b-08f1d5246e2c Subscription has machines with failed baseline rule /subscriptions/48...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus/tasks/11ff8541-820e-cecc-75de-91be7c0d8419 11ff8541-820e-cecc-75de-91be7c0d8419 Subscription has machines with failed baseline rule /subscriptions/48...
```

<span data-ttu-id="b4d2c-115">구독 내의 리소스에서 검색 된 모든 보안 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-115">Gets all the security tasks that were discovered on resources inside a subscription.</span></span>

### <span data-ttu-id="b4d2c-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="b4d2c-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1"

Id                                                                                                                                                                        Name                                 RecommendationType                   ResourceI
                                                                                                                                                                                                                                                    d        
--                                                                                                                                                                        ----                                 ------------------                   ---------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/47f736fa-0ec8-a372-de49-8cf18527930c 47f736fa-0ec8-a372-de49-8cf18527930c ConfigureTier2Waf                    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/5696e90f-833d-494c-8833-f3be335fa9cb 5696e90f-833d-494c-8833-f3be335fa9cb NetworkSecurityGroupMissingOnVm      /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/65193cce-25a1-b30f-f94e-69d52e22923c 65193cce-25a1-b30f-f94e-69d52e22923c VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/7e28a40d-e746-4751-8340-5126d6b77ae5 7e28a40d-e746-4751-8340-5126d6b77ae5 NetworkSecurityGroupMissingOnSubnet  /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/94867597-75e5-cfb6-8b71-e5e5253a24e1 94867597-75e5-cfb6-8b71-e5e5253a24e1 EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/a02fffd5-1956-a6d7-73da-a87a65ae02f4 a02fffd5-1956-a6d7-73da-a87a65ae02f4 VulnerabilityAssessmentDeployment    /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/bd382d04-b478-ac77-e89f-300789032367 bd382d04-b478-ac77-e89f-300789032367 ProvisionNgfw                        /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/MYSERVICE1/providers/Microsoft.Security/locations/centralus/tasks/ce43626a-d56b-6a38-49ef-3ad7a731666e ce43626a-d56b-6a38-49ef-3ad7a731666e EncryptionOnVm                       /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/dcfb6365-799e-5ed4-f344-d86a0a4c2992 dcfb6365-799e-5ed4-f344-d86a0a4c2992 Enable auditing for the SQL database /subsc...
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/ed736ed1-3f42-a95a-0b9e-458c44233937 ed736ed1-3f42-a95a-0b9e-458c44233937 Enable auditing for the SQL server   /subsc...
```

<span data-ttu-id="b4d2c-117">리소스 그룹 내의 리소스에서 검색 된 모든 보안 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-117">Gets all the security tasks that were discovered on resources inside a resource group.</span></span>

### <span data-ttu-id="b4d2c-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="b4d2c-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSecurityTask -ResourceGroupName "myService1" -Name "22ef553d-f13a-5227-ee4c-7cc861d28c96"

Id                                                                                                                                                                        Name                                 RecommendationType              ResourceId    
--                                                                                                                                                                        ----                                 ------------------              ----------    
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/tasks/22ef553d-f13a-5227-ee4c-7cc861d28c96 22ef553d-f13a-5227-ee4c-7cc861d28c96 Enable DDoS protection standard /subscripti...
```

<span data-ttu-id="b4d2c-119">특정 보안 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-119">Gets a specific security task.</span></span>

## <span data-ttu-id="b4d2c-120">변수</span><span class="sxs-lookup"><span data-stu-id="b4d2c-120">PARAMETERS</span></span>

### <span data-ttu-id="b4d2c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d2c-121">-DefaultProfile</span></span>
<span data-ttu-id="b4d2c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d2c-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b4d2c-123">-Name</span></span>
<span data-ttu-id="b4d2c-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d2c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d2c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4d2c-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4d2c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d2c-127">-ResourceId</span></span>
<span data-ttu-id="b4d2c-128">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4d2c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d2c-129">CommonParameters</span></span>
<span data-ttu-id="b4d2c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4d2c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d2c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d2c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d2c-132">입력</span><span class="sxs-lookup"><span data-stu-id="b4d2c-132">INPUTS</span></span>

### <span data-ttu-id="b4d2c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4d2c-133">System.String</span></span>

## <span data-ttu-id="b4d2c-134">출력</span><span class="sxs-lookup"><span data-stu-id="b4d2c-134">OUTPUTS</span></span>

### <span data-ttu-id="b4d2c-135">Microsoft. Azure .의. PSSecurityTask. 작업</span><span class="sxs-lookup"><span data-stu-id="b4d2c-135">Microsoft.Azure.Commands.Security.Models.Tasks.PSSecurityTask</span></span>

## <span data-ttu-id="b4d2c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b4d2c-136">NOTES</span></span>

## <span data-ttu-id="b4d2c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4d2c-137">RELATED LINKS</span></span>