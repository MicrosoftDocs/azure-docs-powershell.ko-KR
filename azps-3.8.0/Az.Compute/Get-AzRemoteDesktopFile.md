---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 650602ef229dd6c7371c6befebbb15dacae1d706
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043432"
---
# <span data-ttu-id="2b501-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="2b501-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="2b501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b501-102">SYNOPSIS</span></span>
<span data-ttu-id="2b501-103">.Rdp 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="2b501-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b501-104">SYNTAX</span></span>

### <span data-ttu-id="2b501-105">다운로드</span><span class="sxs-lookup"><span data-stu-id="2b501-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b501-106">플러그인</span><span class="sxs-lookup"><span data-stu-id="2b501-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b501-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2b501-107">DESCRIPTION</span></span>
<span data-ttu-id="2b501-108">**AzRemoteDesktopFile** Cmdlet은 원격 데스크톱 프로토콜 (.rdp) 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="2b501-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2b501-109">EXAMPLES</span></span>

### <span data-ttu-id="2b501-110">예제 1: 원격 데스크톱 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="2b501-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="2b501-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대 한 원격 데스크톱 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="2b501-112">명령 결과는 D:\RemoteDesktopFile07.rdp. 라는 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="2b501-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b501-113">PARAMETERS</span></span>

### <span data-ttu-id="2b501-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b501-114">-DefaultProfile</span></span>
<span data-ttu-id="2b501-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b501-116">-시작</span><span class="sxs-lookup"><span data-stu-id="2b501-116">-Launch</span></span>
<span data-ttu-id="2b501-117">이 cmdlet이 .rdp 파일을 가져온 후 원격 데스크톱을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b501-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="2b501-118">-LocalPath</span></span>
<span data-ttu-id="2b501-119">이 cmdlet이 .rdp 파일을 저장 하는 로컬 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b501-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2b501-120">-Name</span></span>
<span data-ttu-id="2b501-121">이 cmdlet이 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b501-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b501-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b501-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2b501-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b501-124">CommonParameters</span></span>
<span data-ttu-id="2b501-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b501-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b501-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b501-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b501-127">입력</span><span class="sxs-lookup"><span data-stu-id="2b501-127">INPUTS</span></span>

### <span data-ttu-id="2b501-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b501-128">System.String</span></span>

## <span data-ttu-id="2b501-129">출력</span><span class="sxs-lookup"><span data-stu-id="2b501-129">OUTPUTS</span></span>

### <span data-ttu-id="2b501-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2b501-130">System.Void</span></span>

## <span data-ttu-id="2b501-131">상속자</span><span class="sxs-lookup"><span data-stu-id="2b501-131">NOTES</span></span>

## <span data-ttu-id="2b501-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b501-132">RELATED LINKS</span></span>