---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 4400cb375b60b4f961831927ed5763c608f8e5f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047997"
---
# <span data-ttu-id="424d0-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="424d0-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="424d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424d0-102">SYNOPSIS</span></span>
<span data-ttu-id="424d0-103">API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-103">Creates an API management group.</span></span>

## <span data-ttu-id="424d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="424d0-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="424d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="424d0-105">DESCRIPTION</span></span>
<span data-ttu-id="424d0-106">**AzApiManagementGroup** CMDLET은 API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="424d0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="424d0-107">EXAMPLES</span></span>

### <span data-ttu-id="424d0-108">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="424d0-108">Example 1: Create a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="424d0-109">이 명령은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-109">This command creates a management group.</span></span>

### <span data-ttu-id="424d0-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="424d0-110">Example 2</span></span>

<span data-ttu-id="424d0-111">API 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-111">Creates an API management group.</span></span> <span data-ttu-id="424d0-112">생성</span><span class="sxs-lookup"><span data-stu-id="424d0-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementGroup -Context <PsApiManagementContext> -Description 'Create Echo Api V4' -GroupId '0001' -Name 'Group0001' -Type Custom
```

## <span data-ttu-id="424d0-113">변수</span><span class="sxs-lookup"><span data-stu-id="424d0-113">PARAMETERS</span></span>

### <span data-ttu-id="424d0-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="424d0-114">-Context</span></span>
<span data-ttu-id="424d0-115">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-115">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424d0-116">-DefaultProfile</span></span>
<span data-ttu-id="424d0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="424d0-118">-설명</span><span class="sxs-lookup"><span data-stu-id="424d0-118">-Description</span></span>
<span data-ttu-id="424d0-119">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-119">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424d0-120">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="424d0-120">-ExternalId</span></span>
<span data-ttu-id="424d0-121">외부 그룹의 경우이 속성에는 외부 id 공급자 (예: Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c)의 그룹 id가 포함 됩니다. 그렇지 않으면 값이 null입니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-121">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="424d0-122">-GroupId</span><span class="sxs-lookup"><span data-stu-id="424d0-122">-GroupId</span></span>
<span data-ttu-id="424d0-123">새 관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-123">Specifies the identifier of the new management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424d0-124">-이름</span><span class="sxs-lookup"><span data-stu-id="424d0-124">-Name</span></span>
<span data-ttu-id="424d0-125">관리 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-125">Specifies the management group name.</span></span>

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

### <span data-ttu-id="424d0-126">-Type</span><span class="sxs-lookup"><span data-stu-id="424d0-126">-Type</span></span>
<span data-ttu-id="424d0-127">그룹 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-127">Group Type.</span></span> <span data-ttu-id="424d0-128">사용자 지정 그룹은 사용자가 정의한 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-128">Custom Group is User defined Group.</span></span> <span data-ttu-id="424d0-129">시스템 그룹에는 관리자, 개발자, 게스트 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-129">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="424d0-130">시스템 그룹을 만들거나 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-130">You cannot create or update a System Group.</span></span>  <span data-ttu-id="424d0-131">외부 그룹은 Azure Active Directory와 같은 외부 Id 공급자의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-131">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="424d0-132">이 매개 변수는 선택 사항이 며 기본적으로 사용자 지정 그룹으로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-132">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424d0-133">CommonParameters</span></span>
<span data-ttu-id="424d0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="424d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424d0-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="424d0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424d0-136">입력</span><span class="sxs-lookup"><span data-stu-id="424d0-136">INPUTS</span></span>

### <span data-ttu-id="424d0-137">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="424d0-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="424d0-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="424d0-138">System.String</span></span>

### <span data-ttu-id="424d0-139">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementGroupType, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="424d0-139">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="424d0-140">출력</span><span class="sxs-lookup"><span data-stu-id="424d0-140">OUTPUTS</span></span>

### <span data-ttu-id="424d0-141">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="424d0-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="424d0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="424d0-142">NOTES</span></span>

## <span data-ttu-id="424d0-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="424d0-143">RELATED LINKS</span></span>

[<span data-ttu-id="424d0-144">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="424d0-144">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="424d0-145">제거-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="424d0-145">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="424d0-146">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="424d0-146">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)

