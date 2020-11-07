---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 25bf6699887219cb4315465d7e0f709f82849438
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876911"
---
# <span data-ttu-id="e08e9-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="e08e9-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="e08e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e08e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e08e9-103">Disk 개체에 대 한 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e08e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e08e9-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e08e9-105">DESCRIPTION</span></span>
<span data-ttu-id="e08e9-106">**Set-AzDiskImageReference** cmdlet은 disk 개체의 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e08e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e08e9-107">EXAMPLES</span></span>

### <span data-ttu-id="e08e9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e08e9-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e08e9-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형의 10GB 크기의 로컬 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e08e9-110">Windows OS 종류도 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="e08e9-111">두 번째 명령은 디스크 obejct의 이미지 id와 논리 단위 번호 0을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-111">The second command sets the image id and the logical unit number 0 for the disk obejct.</span></span>
<span data-ttu-id="e08e9-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e08e9-113">변수</span><span class="sxs-lookup"><span data-stu-id="e08e9-113">PARAMETERS</span></span>

### <span data-ttu-id="e08e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08e9-114">-DefaultProfile</span></span>
<span data-ttu-id="e08e9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e08e9-116">-디스크</span><span class="sxs-lookup"><span data-stu-id="e08e9-116">-Disk</span></span>
<span data-ttu-id="e08e9-117">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e08e9-118">-Id</span><span class="sxs-lookup"><span data-stu-id="e08e9-118">-Id</span></span>
<span data-ttu-id="e08e9-119">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08e9-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="e08e9-120">-Lun</span></span>
<span data-ttu-id="e08e9-121">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e08e9-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e08e9-122">-Confirm</span></span>
<span data-ttu-id="e08e9-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08e9-124">-WhatIf</span></span>
<span data-ttu-id="e08e9-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e08e9-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08e9-127">CommonParameters</span></span>
<span data-ttu-id="e08e9-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08e9-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08e9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08e9-130">입력</span><span class="sxs-lookup"><span data-stu-id="e08e9-130">INPUTS</span></span>

### <span data-ttu-id="e08e9-131">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="e08e9-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="e08e9-132">System.webserver 시스템. Null 허용 ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e08e9-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e08e9-133">출력</span><span class="sxs-lookup"><span data-stu-id="e08e9-133">OUTPUTS</span></span>

### <span data-ttu-id="e08e9-134">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="e08e9-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="e08e9-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e08e9-135">NOTES</span></span>

## <span data-ttu-id="e08e9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e08e9-136">RELATED LINKS</span></span>
