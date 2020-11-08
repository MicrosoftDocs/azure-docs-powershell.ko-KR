---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046152"
---
# <span data-ttu-id="b737e-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b737e-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="b737e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b737e-102">SYNOPSIS</span></span>
<span data-ttu-id="b737e-103">네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-103">Removes a network security group.</span></span>

## <span data-ttu-id="b737e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b737e-104">SYNTAX</span></span>

### <span data-ttu-id="b737e-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="b737e-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b737e-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="b737e-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b737e-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="b737e-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b737e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b737e-108">DESCRIPTION</span></span>
<span data-ttu-id="b737e-109">**AzureNetworkSecurityGroupAssociation** cmdlet은 가상 컴퓨터에서 네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="b737e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b737e-110">EXAMPLES</span></span>

### <span data-ttu-id="b737e-111">예제 1: 네트워크 보안 그룹에 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="b737e-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="b737e-112">이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="b737e-113">현재 cmdlet은 해당 가상 컴퓨터에서 ContosoNetworkSecurityGroup 이라는 네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="b737e-114">변수</span><span class="sxs-lookup"><span data-stu-id="b737e-114">PARAMETERS</span></span>

### <span data-ttu-id="b737e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b737e-115">-Force</span></span>
<span data-ttu-id="b737e-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b737e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b737e-117">-Name</span></span>
<span data-ttu-id="b737e-118">이 cmdlet이 제거 하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b737e-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="b737e-120">이 cmdlet에서 네트워크 보안 그룹을 제거 하는 네트워크 어댑터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b737e-121">-PassThru</span></span>
<span data-ttu-id="b737e-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b737e-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b737e-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="b737e-124">-Profile</span></span>
<span data-ttu-id="b737e-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b737e-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b737e-127">-RoleName</span></span>
<span data-ttu-id="b737e-128">이 cmdlet에서 네트워크 보안 그룹을 제거 하는 PaaS 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b737e-129">-ServiceName</span></span>
<span data-ttu-id="b737e-130">클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="b737e-131">이 cmdlet이 네트워크 보안 그룹을 제거 하는 PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-132">-슬롯</span><span class="sxs-lookup"><span data-stu-id="b737e-132">-Slot</span></span>
<span data-ttu-id="b737e-133">PaaS 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="b737e-134">이 cmdlet에서 네트워크 보안 그룹을 제거 하는 PaaS 역할은이 매개 변수에서 지정 하는 슬롯을가지고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="b737e-135">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-135">Valid values are:</span></span>

- <span data-ttu-id="b737e-136">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="b737e-136">Production</span></span>
- <span data-ttu-id="b737e-137">대기</span><span class="sxs-lookup"><span data-stu-id="b737e-137">Staging</span></span>

<span data-ttu-id="b737e-138">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b737e-139">-SubnetName</span></span>
<span data-ttu-id="b737e-140">이 cmdlet이 네트워크 보안 그룹을 제거 하는 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b737e-141">-VirtualNetworkName</span></span>
<span data-ttu-id="b737e-142">이 cmdlet이 네트워크 보안 그룹을 제거 하는 서브넷을 포함 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-143">-VM</span><span class="sxs-lookup"><span data-stu-id="b737e-143">-VM</span></span>
<span data-ttu-id="b737e-144">이 cmdlet이 네트워크 보안 그룹을 적용 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b737e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b737e-145">CommonParameters</span></span>
<span data-ttu-id="b737e-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b737e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b737e-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b737e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b737e-148">입력</span><span class="sxs-lookup"><span data-stu-id="b737e-148">INPUTS</span></span>

## <span data-ttu-id="b737e-149">출력</span><span class="sxs-lookup"><span data-stu-id="b737e-149">OUTPUTS</span></span>

### <span data-ttu-id="b737e-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b737e-150">System.Boolean</span></span>

## <span data-ttu-id="b737e-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b737e-151">NOTES</span></span>

## <span data-ttu-id="b737e-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b737e-152">RELATED LINKS</span></span>

[<span data-ttu-id="b737e-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b737e-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="b737e-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b737e-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)