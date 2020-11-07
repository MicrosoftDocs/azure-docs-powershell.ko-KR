---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 1b01550e8501a0a7f81ac5c04cd0083fc521fec5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872225"
---
# <span data-ttu-id="a46ca-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a46ca-101">New-AzStorageTable</span></span>

## <span data-ttu-id="a46ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a46ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a46ca-103">저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-103">Creates a storage table.</span></span>

## <span data-ttu-id="a46ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a46ca-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a46ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a46ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a46ca-106">**AzStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a46ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a46ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a46ca-108">예제 1: azure 저장소 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="a46ca-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="a46ca-109">이 명령은 tableabc의 이름을 사용 하 여 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="a46ca-110">예제 2: 여러 azure storage 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="a46ca-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="a46ca-111">이 명령은 여러 개의 표를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-111">This command creates multiple tables.</span></span>
<span data-ttu-id="a46ca-112">.NET **문자열** 클래스의 **Split** 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a46ca-113">변수</span><span class="sxs-lookup"><span data-stu-id="a46ca-113">PARAMETERS</span></span>

### <span data-ttu-id="a46ca-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a46ca-114">-Context</span></span>
<span data-ttu-id="a46ca-115">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-115">Specifies the storage context.</span></span>
<span data-ttu-id="a46ca-116">이를 만들기 위해 New-AzStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a46ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46ca-117">-DefaultProfile</span></span>
<span data-ttu-id="a46ca-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46ca-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a46ca-119">-Name</span></span>
<span data-ttu-id="a46ca-120">새 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a46ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46ca-121">CommonParameters</span></span>
<span data-ttu-id="a46ca-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46ca-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46ca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46ca-124">입력</span><span class="sxs-lookup"><span data-stu-id="a46ca-124">INPUTS</span></span>

### <span data-ttu-id="a46ca-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a46ca-125">System.String</span></span>

### <span data-ttu-id="a46ca-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a46ca-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a46ca-127">출력</span><span class="sxs-lookup"><span data-stu-id="a46ca-127">OUTPUTS</span></span>

### <span data-ttu-id="a46ca-128">WindowsAzure. ResourceModel를 AzureStorageTable로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a46ca-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="a46ca-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a46ca-129">NOTES</span></span>

## <span data-ttu-id="a46ca-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a46ca-130">RELATED LINKS</span></span>

[<span data-ttu-id="a46ca-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a46ca-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="a46ca-132">제거-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a46ca-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)

