---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529928"
---
# <span data-ttu-id="64628-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="64628-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="64628-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64628-102">SYNOPSIS</span></span>
<span data-ttu-id="64628-103">무인 Windows 설치 응답 파일에 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64628-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64628-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="64628-105">설명은</span><span class="sxs-lookup"><span data-stu-id="64628-105">DESCRIPTION</span></span>
<span data-ttu-id="64628-106">**추가-AzureRmVMAdditionalUnattendContent** cmdlet은 정보를 무인 Windows 설치 응답 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="64628-107">이 cmdlet에서 unattend.xml 파일에 추가 하는 기본 64 인코딩 xml 형식의 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="64628-108">예제의</span><span class="sxs-lookup"><span data-stu-id="64628-108">EXAMPLES</span></span>

### <span data-ttu-id="64628-109">예제 1: unattend.xml에 콘텐츠 추가</span><span class="sxs-lookup"><span data-stu-id="64628-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="64628-110">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="64628-111">두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="64628-112">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="64628-113">가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="64628-114">세 번째 명령은 Get-Credential cmdlet을 사용 하 여 credential 개체를 만든 다음 그 결과를 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="64628-115">명령이 사용자 이름 및 암호를 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="64628-116">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="64628-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="64628-117">네 번째 명령은 **AzureRmVMOperatingSystem** cmdlet을 사용 하 여 $VirtualMachine에 저장 된 가상 컴퓨터를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="64628-118">다섯 번째 명령은 $AucContent 변수에 콘텐츠를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="64628-119">내용에 암호가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64628-119">The content includes a password.</span></span>

<span data-ttu-id="64628-120">마지막 명령은 $AucContent에 저장 된 콘텐츠를 unattend.xml 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="64628-121">변수</span><span class="sxs-lookup"><span data-stu-id="64628-121">PARAMETERS</span></span>

### <span data-ttu-id="64628-122">-콘텐츠</span><span class="sxs-lookup"><span data-stu-id="64628-122">-Content</span></span>
<span data-ttu-id="64628-123">Base 64 인코딩된 XML 형식의 콘텐츠를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="64628-124">이 cmdlet은 콘텐츠를 unattend.xml 파일에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="64628-125">XML 콘텐츠는 4kb 미만 이어야 하며이 cmdlet이 삽입 하는 설정 또는 기능에 대 한 루트 요소를 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="64628-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="64628-126">-SettingName</span></span>
<span data-ttu-id="64628-127">콘텐츠가 적용 되는 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="64628-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="64628-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="64628-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="64628-129">FirstLogonCommands</span></span>
- <span data-ttu-id="64628-130">자동</span><span class="sxs-lookup"><span data-stu-id="64628-130">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64628-131">-VM</span><span class="sxs-lookup"><span data-stu-id="64628-131">-VM</span></span>
<span data-ttu-id="64628-132">이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="64628-133">가상 컴퓨터 개체를 가져오려면 [AzureRmVM](./Get-AzureRmVM.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="64628-134">[새 AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64628-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64628-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64628-135">CommonParameters</span></span>
<span data-ttu-id="64628-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64628-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64628-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64628-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64628-138">입력</span><span class="sxs-lookup"><span data-stu-id="64628-138">INPUTS</span></span>

### <span data-ttu-id="64628-139">않아야</span><span class="sxs-lookup"><span data-stu-id="64628-139">None</span></span>
<span data-ttu-id="64628-140">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64628-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64628-141">출력</span><span class="sxs-lookup"><span data-stu-id="64628-141">OUTPUTS</span></span>

## <span data-ttu-id="64628-142">상속자</span><span class="sxs-lookup"><span data-stu-id="64628-142">NOTES</span></span>

## <span data-ttu-id="64628-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64628-143">RELATED LINKS</span></span>

[<span data-ttu-id="64628-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="64628-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="64628-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="64628-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="64628-146">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="64628-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)