---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875041"
---
# <span data-ttu-id="e483d-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="e483d-101">New-DataDiskObject</span></span>

## <span data-ttu-id="e483d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e483d-102">SYNOPSIS</span></span>
<span data-ttu-id="e483d-103">새 가상 컴퓨터 플랫폼 이미지를 만드는 데 사용 되는 데이터 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e483d-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="e483d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e483d-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e483d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e483d-105">DESCRIPTION</span></span>
<span data-ttu-id="e483d-106">데이터 디스크에 대 한 정보를 포함 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e483d-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="e483d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e483d-107">EXAMPLES</span></span>

### <span data-ttu-id="e483d-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e483d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="e483d-109">새 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e483d-109">Create a new data disk object.</span></span>

## <span data-ttu-id="e483d-110">변수</span><span class="sxs-lookup"><span data-stu-id="e483d-110">PARAMETERS</span></span>

### <span data-ttu-id="e483d-111">-Lun</span><span class="sxs-lookup"><span data-stu-id="e483d-111">-Lun</span></span>
<span data-ttu-id="e483d-112">논리 단위 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="e483d-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e483d-113">-Uri</span><span class="sxs-lookup"><span data-stu-id="e483d-113">-Uri</span></span>
<span data-ttu-id="e483d-114">디스크 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e483d-114">Location of the disk template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e483d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e483d-115">CommonParameters</span></span>
<span data-ttu-id="e483d-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e483d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e483d-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e483d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e483d-118">입력</span><span class="sxs-lookup"><span data-stu-id="e483d-118">INPUTS</span></span>

## <span data-ttu-id="e483d-119">출력</span><span class="sxs-lookup"><span data-stu-id="e483d-119">OUTPUTS</span></span>

## <span data-ttu-id="e483d-120">상속자</span><span class="sxs-lookup"><span data-stu-id="e483d-120">NOTES</span></span>

## <span data-ttu-id="e483d-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e483d-121">RELATED LINKS</span></span>
