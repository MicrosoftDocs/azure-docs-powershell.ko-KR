---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218405"
---
# <span data-ttu-id="00c08-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="00c08-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="00c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00c08-102">SYNOPSIS</span></span>
<span data-ttu-id="00c08-103">가상 컴퓨터 또는 Vmss VM에 대 한 로컬 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="00c08-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00c08-104">SYNTAX</span></span>

### <span data-ttu-id="00c08-105">NormalDiskParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="00c08-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00c08-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="00c08-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00c08-107">설명은</span><span class="sxs-lookup"><span data-stu-id="00c08-107">DESCRIPTION</span></span>
<span data-ttu-id="00c08-108">**AzVMDataDisk** cmdlet은 가상 컴퓨터 또는 VMSS VM에 대 한 로컬 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="00c08-109">예제의</span><span class="sxs-lookup"><span data-stu-id="00c08-109">EXAMPLES</span></span>

### <span data-ttu-id="00c08-110">예제 1: Vmss VM에 관리 되는 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="00c08-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="00c08-111">첫 번째 명령은 관리 되는 기존 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="00c08-112">다음 명령은 관리 되는 디스크를 사용 하 여 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="00c08-113">다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 주어진 기존 Vmss VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="00c08-114">마지막 명령은 새 데이터 디스크를 추가 하 여 Vmss VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="00c08-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="00c08-115">Example 2</span></span>

<span data-ttu-id="00c08-116">가상 컴퓨터 또는 Vmss VM에 대 한 로컬 데이터 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="00c08-117">생성</span><span class="sxs-lookup"><span data-stu-id="00c08-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="00c08-118">변수</span><span class="sxs-lookup"><span data-stu-id="00c08-118">PARAMETERS</span></span>

### <span data-ttu-id="00c08-119">-캐싱</span><span class="sxs-lookup"><span data-stu-id="00c08-119">-Caching</span></span>
<span data-ttu-id="00c08-120">가상 컴퓨터 데이터 디스크의 캐싱.</span><span class="sxs-lookup"><span data-stu-id="00c08-120">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="00c08-121">-CreateOption</span></span>
<span data-ttu-id="00c08-122">가상 컴퓨터 데이터 디스크의 만들기 옵션</span><span class="sxs-lookup"><span data-stu-id="00c08-122">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c08-123">-DefaultProfile</span></span>
<span data-ttu-id="00c08-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00c08-125">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="00c08-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="00c08-126">가상 컴퓨터 관리 디스크 암호화 집합의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="00c08-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="00c08-127">-DiskSizeInGB</span></span>
<span data-ttu-id="00c08-128">가상 컴퓨터 데이터 디스크의 크기 (GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-128">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="00c08-129">-Lun</span></span>
<span data-ttu-id="00c08-130">가상 컴퓨터 데이터 디스크의 Lun.</span><span class="sxs-lookup"><span data-stu-id="00c08-130">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="00c08-131">-ManagedDiskId</span></span>
<span data-ttu-id="00c08-132">가상 컴퓨터 관리 디스크의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-132">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-133">-이름</span><span class="sxs-lookup"><span data-stu-id="00c08-133">-Name</span></span>
<span data-ttu-id="00c08-134">가상 컴퓨터 데이터 디스크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="00c08-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="00c08-135">-SourceImageUri</span></span>
<span data-ttu-id="00c08-136">가상 컴퓨터 OS 디스크의 원본 이미지 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-136">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="00c08-137">-StorageAccountType</span></span>
<span data-ttu-id="00c08-138">가상 컴퓨터 관리 디스크의 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-138">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="00c08-139">-VhdUri</span></span>
<span data-ttu-id="00c08-140">가상 컴퓨터 데이터 디스크의 Vhd Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-140">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="00c08-141">-WriteAccelerator</span></span>
<span data-ttu-id="00c08-142">관리 되는 데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00c08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c08-143">CommonParameters</span></span>
<span data-ttu-id="00c08-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00c08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c08-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="00c08-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c08-146">입력</span><span class="sxs-lookup"><span data-stu-id="00c08-146">INPUTS</span></span>

### <span data-ttu-id="00c08-147">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="00c08-147">System.Int32</span></span>

### <span data-ttu-id="00c08-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00c08-148">System.String</span></span>

### <span data-ttu-id="00c08-149">Microsoft. 관리. m m/. m m 형식</span><span class="sxs-lookup"><span data-stu-id="00c08-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="00c08-150">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="00c08-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="00c08-151">출력</span><span class="sxs-lookup"><span data-stu-id="00c08-151">OUTPUTS</span></span>

### <span data-ttu-id="00c08-152">Microsoft. a q. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="00c08-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="00c08-153">상속자</span><span class="sxs-lookup"><span data-stu-id="00c08-153">NOTES</span></span>

## <span data-ttu-id="00c08-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00c08-154">RELATED LINKS</span></span>