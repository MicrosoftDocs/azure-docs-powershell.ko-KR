---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: af6acce52ee41297e650abb76188324ecf313679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528987"
---
# <span data-ttu-id="03289-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="03289-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="03289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03289-102">SYNOPSIS</span></span>
<span data-ttu-id="03289-103">Azure Data Lake Analytics 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03289-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03289-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03289-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03289-105">DESCRIPTION</span></span>
<span data-ttu-id="03289-106">Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet은 Azure Data Lake Analytics 카탈로그 자격 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="03289-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03289-107">EXAMPLES</span></span>

### <span data-ttu-id="03289-108">예제 1: 자격 증명 제거</span><span class="sxs-lookup"><span data-stu-id="03289-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="03289-109">이 명령은 지정 된 Data Lake Analytics 카탈로그 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="03289-110">변수</span><span class="sxs-lookup"><span data-stu-id="03289-110">PARAMETERS</span></span>

### <span data-ttu-id="03289-111">-계정</span><span class="sxs-lookup"><span data-stu-id="03289-111">-Account</span></span>
<span data-ttu-id="03289-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03289-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03289-113">-DatabaseName</span></span>
<span data-ttu-id="03289-114">자격 증명을 보유 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03289-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03289-115">-DefaultProfile</span></span>
<span data-ttu-id="03289-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="03289-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03289-117">-Force</span><span class="sxs-lookup"><span data-stu-id="03289-117">-Force</span></span>
<span data-ttu-id="03289-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03289-119">-이름</span><span class="sxs-lookup"><span data-stu-id="03289-119">-Name</span></span>
<span data-ttu-id="03289-120">자격 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-120">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03289-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03289-121">-PassThru</span></span>
<span data-ttu-id="03289-122">이 cmdlet이 작업이 완료 될 때까지 대기 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="03289-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="03289-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03289-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03289-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03289-125">-암호</span><span class="sxs-lookup"><span data-stu-id="03289-125">-Password</span></span>
<span data-ttu-id="03289-126">자격 증명의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="03289-126">The password for the credential.</span></span>
<span data-ttu-id="03289-127">이는 호출자가 계정 소유자가 아닌 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03289-128">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="03289-128">-Recurse</span></span>
<span data-ttu-id="03289-129">이 삭제 작업을 수행 하 고이 자격 증명에 종속 된 모든 리소스를 삭제 및 제거 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="03289-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03289-130">-확인</span><span class="sxs-lookup"><span data-stu-id="03289-130">-Confirm</span></span>
<span data-ttu-id="03289-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03289-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03289-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03289-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03289-133">CommonParameters</span></span>
<span data-ttu-id="03289-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03289-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03289-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03289-136">입력</span><span class="sxs-lookup"><span data-stu-id="03289-136">INPUTS</span></span>

### <span data-ttu-id="03289-137">않아야</span><span class="sxs-lookup"><span data-stu-id="03289-137">None</span></span>
<span data-ttu-id="03289-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03289-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03289-139">출력</span><span class="sxs-lookup"><span data-stu-id="03289-139">OUTPUTS</span></span>

### <span data-ttu-id="03289-140">부울</span><span class="sxs-lookup"><span data-stu-id="03289-140">bool</span></span>
<span data-ttu-id="03289-141">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="03289-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="03289-142">상속자</span><span class="sxs-lookup"><span data-stu-id="03289-142">NOTES</span></span>

## <span data-ttu-id="03289-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03289-143">RELATED LINKS</span></span>
