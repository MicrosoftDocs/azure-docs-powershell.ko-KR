---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529027"
---
# <span data-ttu-id="6b396-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6b396-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="6b396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b396-102">SYNOPSIS</span></span>
<span data-ttu-id="6b396-103">가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b396-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b396-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b396-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6b396-105">DESCRIPTION</span></span>
<span data-ttu-id="6b396-106">**추가-AzureRmVMDataDisk** cmdlet은 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="6b396-107">가상 컴퓨터를 만들 때 데이터 디스크를 추가 하거나 기존 가상 컴퓨터에 데이터 디스크를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="6b396-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6b396-108">EXAMPLES</span></span>

### <span data-ttu-id="6b396-109">예제 1: 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="6b396-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="6b396-110">첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6b396-111">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6b396-112">다음 세 개의 명령은 1 개의 데이터 디스크 경로를 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="6b396-113">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="6b396-114">마지막 세 개의 명령은 모두 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6b396-115">명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="6b396-116">각 디스크의 URI는 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="6b396-117">예제 2: 기존 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="6b396-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="6b396-118">첫 번째 명령은 [AzureRmVM](./Get-AzureRmVM.md) cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="6b396-119">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="6b396-120">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="6b396-121">마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="6b396-122">예제 3: 일반화 된 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="6b396-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="6b396-123">첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6b396-124">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6b396-125">다음 두 명령은 데이터 이미지 및 데이터 디스크에 대 한 경로를 $DataImageUri 및 $DataDiskUri 변수에 각각 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="6b396-126">이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="6b396-127">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6b396-128">명령은 디스크의 이름과 다른 디스크의 속성에 대 한 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="6b396-129">예제 4: 특수 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="6b396-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="6b396-130">첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="6b396-131">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="6b396-132">다음 명령은 데이터 디스크의 경로를 $DataDiskUri 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="6b396-133">이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="6b396-134">마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="6b396-135">명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="6b396-136">변수</span><span class="sxs-lookup"><span data-stu-id="6b396-136">PARAMETERS</span></span>

### <span data-ttu-id="6b396-137">-캐싱</span><span class="sxs-lookup"><span data-stu-id="6b396-137">-Caching</span></span>
<span data-ttu-id="6b396-138">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="6b396-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b396-140">읽기</span><span class="sxs-lookup"><span data-stu-id="6b396-140">ReadOnly</span></span>
- <span data-ttu-id="6b396-141">쓰기</span><span class="sxs-lookup"><span data-stu-id="6b396-141">ReadWrite</span></span>
- <span data-ttu-id="6b396-142">않아야</span><span class="sxs-lookup"><span data-stu-id="6b396-142">None</span></span>

<span data-ttu-id="6b396-143">기본값은 ReadWrite입니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="6b396-144">이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="6b396-145">이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6b396-146">-CreateOption</span></span>
<span data-ttu-id="6b396-147">이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="6b396-148">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b396-149">붙일.</span><span class="sxs-lookup"><span data-stu-id="6b396-149">Attach.</span></span>
<span data-ttu-id="6b396-150">특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="6b396-151">이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6b396-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="6b396-152">*VhdUri* 는 가상 컴퓨터에 데이터 디스크로 연결할 VHD (가상 하드 디스크)의 위치를 Azure platform에 알리기 위해 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="6b396-153">비울.</span><span class="sxs-lookup"><span data-stu-id="6b396-153">Empty.</span></span>
<span data-ttu-id="6b396-154">빈 데이터 디스크를 만들려면이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="6b396-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="6b396-155">FromImage.</span></span>
<span data-ttu-id="6b396-156">일반화 된 이미지 또는 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="6b396-157">이 옵션을 지정 하는 경우 데이터 디스크로 연결할 VHD의 위치를 Azure platform에 알려 주는 데에도 *Sourceimageuri* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="6b396-158">*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장 될 위치를 식별 하는 위치로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-159">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="6b396-159">-DiskSizeInGB</span></span>
<span data-ttu-id="6b396-160">가상 컴퓨터에 연결할 빈 디스크의 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-160">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-161">-Lun</span><span class="sxs-lookup"><span data-stu-id="6b396-161">-Lun</span></span>
<span data-ttu-id="6b396-162">데이터 디스크에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-162">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-163">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6b396-163">-ManagedDiskId</span></span>
<span data-ttu-id="6b396-164">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-164">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-165">-이름</span><span class="sxs-lookup"><span data-stu-id="6b396-165">-Name</span></span>
<span data-ttu-id="6b396-166">추가할 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-166">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="6b396-167">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="6b396-167">-SourceImageUri</span></span>
<span data-ttu-id="6b396-168">이 cmdlet이 연결 하는 디스크의 원본 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-168">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-169">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6b396-169">-StorageAccountType</span></span>
<span data-ttu-id="6b396-170">관리 되는 디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-170">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-171">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="6b396-171">-VhdUri</span></span>
<span data-ttu-id="6b396-172">플랫폼 이미지 또는 사용자 이미지를 사용할 때 만들 VHD (가상 하드 디스크) 파일에 대 한 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-172">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="6b396-173">이 cmdlet은 이미지 blob (이진 대형 개체)를이 위치로 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-173">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="6b396-174">가상 컴퓨터를 시작할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-174">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b396-175">-VM</span><span class="sxs-lookup"><span data-stu-id="6b396-175">-VM</span></span>
<span data-ttu-id="6b396-176">데이터 디스크를 추가할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-176">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="6b396-177">**Get-AzureRmVM** cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-177">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="6b396-178">**새 AzureRmVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-178">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="6b396-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b396-179">CommonParameters</span></span>
<span data-ttu-id="6b396-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b396-181">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b396-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b396-182">입력</span><span class="sxs-lookup"><span data-stu-id="6b396-182">INPUTS</span></span>

### <span data-ttu-id="6b396-183">않아야</span><span class="sxs-lookup"><span data-stu-id="6b396-183">None</span></span>
<span data-ttu-id="6b396-184">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b396-184">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b396-185">출력</span><span class="sxs-lookup"><span data-stu-id="6b396-185">OUTPUTS</span></span>

## <span data-ttu-id="6b396-186">상속자</span><span class="sxs-lookup"><span data-stu-id="6b396-186">NOTES</span></span>

## <span data-ttu-id="6b396-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b396-187">RELATED LINKS</span></span>

[<span data-ttu-id="6b396-188">제거-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6b396-188">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="6b396-189">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6b396-189">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6b396-190">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6b396-190">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)