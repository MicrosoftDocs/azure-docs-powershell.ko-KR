---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: b467d629b578e9f9883dac4c0a8e268f9007a373
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204896"
---
# <span data-ttu-id="2a5c5-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2a5c5-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="2a5c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a5c5-103">Active directory 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="2a5c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a5c5-104">SYNTAX</span></span>

### <span data-ttu-id="2a5c5-105">EmptyParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a5c5-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2a5c5-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5c5-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2a5c5-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5c5-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2a5c5-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5c5-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2a5c5-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5c5-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2a5c5-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5c5-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="2a5c5-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a5c5-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="2a5c5-112">설명은</span><span class="sxs-lookup"><span data-stu-id="2a5c5-112">DESCRIPTION</span></span>
<span data-ttu-id="2a5c5-113">Active directory 서비스 사용자를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="2a5c5-114">예제의</span><span class="sxs-lookup"><span data-stu-id="2a5c5-114">EXAMPLES</span></span>

### <span data-ttu-id="2a5c5-115">예제 1: 광고 서비스 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="2a5c5-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="2a5c5-116">테 넌 트에서 모든 광고 서비스 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="2a5c5-117">예제 2: 페이징을 사용 하 여 광고 서비스 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="2a5c5-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="2a5c5-118">테 넌 트에서 첫 번째 100 광고 서비스 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="2a5c5-119">예제 3: SPN을 기준으로 서비스 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="2a5c5-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="2a5c5-120">SPN이 ' 36f81fc3-b00f-48cd-8218-3879f51ff39f ' 인 서비스 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="2a5c5-121">예제 4: 검색 문자열을 기준으로 서비스 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="2a5c5-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="2a5c5-122">표시 이름이 "Web"으로 시작 하는 모든 광고 서비스 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="2a5c5-123">예제 5: 파이핑을 기준으로 서비스 사용자 나열</span><span class="sxs-lookup"><span data-stu-id="2a5c5-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="2a5c5-124">개체 id가 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' 인 광고 응용 프로그램을 가져오고이를 Get-AzADServicePrincipal cmdlet에 파이프 하 여 해당 응용 프로그램의 모든 서비스 사용자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="2a5c5-125">변수</span><span class="sxs-lookup"><span data-stu-id="2a5c5-125">PARAMETERS</span></span>

### <span data-ttu-id="2a5c5-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2a5c5-126">-ApplicationId</span></span>
<span data-ttu-id="2a5c5-127">서비스 사용자 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-127">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2a5c5-128">-ApplicationObject</span></span>
<span data-ttu-id="2a5c5-129">서비스 사용자가 검색 되 고 있는 응용 프로그램 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a5c5-130">-DefaultProfile</span></span>
<span data-ttu-id="2a5c5-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2a5c5-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a5c5-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a5c5-132">-DisplayName</span></span>
<span data-ttu-id="2a5c5-133">서비스 사용자 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-133">The service principal display name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="2a5c5-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="2a5c5-135">서비스 사용자 검색 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2a5c5-136">-ObjectId</span></span>
<span data-ttu-id="2a5c5-137">서비스 사용자의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-137">Object id of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a5c5-138">-ServicePrincipalName</span></span>
<span data-ttu-id="2a5c5-139">서비스의 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-139">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="2a5c5-140">-IncludeTotalCount</span></span>
<span data-ttu-id="2a5c5-141">데이터 집합의 개체 수를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="2a5c5-142">현재이 매개 변수는 아무런 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="2a5c5-143">-생략</span><span class="sxs-lookup"><span data-stu-id="2a5c5-143">-Skip</span></span>
<span data-ttu-id="2a5c5-144">첫 N 개 개체를 무시 하 고 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-144">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-145">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="2a5c5-145">-First</span></span>
<span data-ttu-id="2a5c5-146">반환할 최대 개체 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-146">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a5c5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a5c5-147">CommonParameters</span></span>
<span data-ttu-id="2a5c5-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a5c5-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2a5c5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a5c5-150">입력</span><span class="sxs-lookup"><span data-stu-id="2a5c5-150">INPUTS</span></span>

### <span data-ttu-id="2a5c5-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a5c5-151">System.String</span></span>

### <span data-ttu-id="2a5c5-152">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="2a5c5-152">System.Guid</span></span>

### <span data-ttu-id="2a5c5-153">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="2a5c5-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="2a5c5-154">출력</span><span class="sxs-lookup"><span data-stu-id="2a5c5-154">OUTPUTS</span></span>

### <span data-ttu-id="2a5c5-155">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2a5c5-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2a5c5-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2a5c5-156">NOTES</span></span>

## <span data-ttu-id="2a5c5-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a5c5-157">RELATED LINKS</span></span>

[<span data-ttu-id="2a5c5-158">새로운 AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2a5c5-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="2a5c5-159">업데이트-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2a5c5-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="2a5c5-160">제거-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2a5c5-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="2a5c5-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2a5c5-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="2a5c5-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2a5c5-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)
