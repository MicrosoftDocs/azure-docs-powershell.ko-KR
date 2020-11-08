---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218208"
---
# <span data-ttu-id="1f7b2-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1f7b2-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="1f7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7b2-103">서비스 사용자와 연결 된 자격 증명 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="1f7b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f7b2-104">SYNTAX</span></span>

### <span data-ttu-id="1f7b2-105">ObjectIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f7b2-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f7b2-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f7b2-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f7b2-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f7b2-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f7b2-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f7b2-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f7b2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1f7b2-109">DESCRIPTION</span></span>
<span data-ttu-id="1f7b2-110">Get-AzADSpCredential cmdlet은 서비스 사용자와 연결 된 자격 증명 목록을 검색 하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="1f7b2-111">이 명령은 서비스 사용자와 연결 된 모든 자격 증명 속성 (자격 증명 값 제외)을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="1f7b2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1f7b2-112">EXAMPLES</span></span>

### <span data-ttu-id="1f7b2-113">예제 1-SPN으로 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="1f7b2-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="1f7b2-114">SPN이 있는 서비스 사용자와 연결 된 자격 증명 목록을 반환 http://test12345 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="1f7b2-115">예제 2-개체 id 별 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="1f7b2-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="1f7b2-116">개체 id가 "58e28616-99cc-4da4-b705-7672130e1047" 인 서비스 사용자와 연결 된 자격 증명 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="1f7b2-117">예제 3-파이핑으로 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="1f7b2-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="1f7b2-118">개체 id가 "58e28616-99cc-4da4-b705-7672130e1047" 인 서비스 사용자를 가져오고이를 Get-AzADSpCredential cmdlet에 파이프 하 여 해당 서비스 사용자의 모든 자격 증명을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="1f7b2-119">변수</span><span class="sxs-lookup"><span data-stu-id="1f7b2-119">PARAMETERS</span></span>

### <span data-ttu-id="1f7b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7b2-120">-DefaultProfile</span></span>
<span data-ttu-id="1f7b2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1f7b2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f7b2-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f7b2-122">-DisplayName</span></span>
<span data-ttu-id="1f7b2-123">서비스 주체의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="1f7b2-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1f7b2-124">-ObjectId</span></span>
<span data-ttu-id="1f7b2-125">자격 증명을 검색할 서비스 주체의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7b2-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1f7b2-126">-ServicePrincipalName</span></span>
<span data-ttu-id="1f7b2-127">자격 증명을 검색할 서비스 주체의 이름 (SPN)입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7b2-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="1f7b2-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="1f7b2-129">자격 증명을 검색할 서비스 사용자 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f7b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7b2-130">CommonParameters</span></span>
<span data-ttu-id="1f7b2-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7b2-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f7b2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7b2-133">입력</span><span class="sxs-lookup"><span data-stu-id="1f7b2-133">INPUTS</span></span>

### <span data-ttu-id="1f7b2-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f7b2-134">System.String</span></span>

### <span data-ttu-id="1f7b2-135">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f7b2-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="1f7b2-136">출력</span><span class="sxs-lookup"><span data-stu-id="1f7b2-136">OUTPUTS</span></span>

### <span data-ttu-id="1f7b2-137">ActiveDirectory Adcredential 자격 증명</span><span class="sxs-lookup"><span data-stu-id="1f7b2-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="1f7b2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1f7b2-138">NOTES</span></span>

## <span data-ttu-id="1f7b2-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f7b2-139">RELATED LINKS</span></span>

[<span data-ttu-id="1f7b2-140">새로운 AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1f7b2-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="1f7b2-141">제거-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1f7b2-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="1f7b2-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1f7b2-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)
