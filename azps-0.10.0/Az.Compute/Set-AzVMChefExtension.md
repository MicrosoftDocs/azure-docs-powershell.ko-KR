---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 3bedeb243b79cada713889145771d45511cb7b7f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876882"
---
# <span data-ttu-id="6f066-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6f066-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="6f066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f066-102">SYNOPSIS</span></span>
<span data-ttu-id="6f066-103">가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="6f066-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f066-104">SYNTAX</span></span>

### <span data-ttu-id="6f066-105">Linux</span><span class="sxs-lookup"><span data-stu-id="6f066-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f066-106">창을</span><span class="sxs-lookup"><span data-stu-id="6f066-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f066-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6f066-107">DESCRIPTION</span></span>
<span data-ttu-id="6f066-108">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="6f066-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6f066-109">EXAMPLES</span></span>

### <span data-ttu-id="6f066-110">예제 1: Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6f066-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="6f066-111">이 명령은 WindowsVM001 이라는 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="6f066-112">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="6f066-113">예제 2: Linux 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6f066-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="6f066-114">이 명령은 요리사 확장명을 LinuxVM001 이라는 Linux 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="6f066-115">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="6f066-116">예제 3: 부트스트랩 옵션을 사용 하 여 Windows 가상 컴퓨터에 요리사 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6f066-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="6f066-117">이 명령은 요리사 확장명을 WindowsVM002 이라는 Windows 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="6f066-118">가상 컴퓨터가 시작 되 면 가상 컴퓨터를 bootstraps 요리사 Apache를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="6f066-119">부트스트래핑 후 가상 컴퓨터는 JSON 형식으로 지정 된 BootstrapOptions를 참조 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="6f066-120">변수</span><span class="sxs-lookup"><span data-stu-id="6f066-120">PARAMETERS</span></span>

### <span data-ttu-id="6f066-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6f066-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="6f066-122">-BootstrapOptions</span></span>
<span data-ttu-id="6f066-123">Client_rb 옵션에서 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="6f066-124">-BootstrapVersion</span></span>
<span data-ttu-id="6f066-125">부트스트랩 구성의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="6f066-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="6f066-127">요리사가 실행 되는 빈도 (분 단위)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="6f066-128">Azure VM에 요리사를 설치 하지 않으려는 경우에는이 필드에서 값을 0으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="6f066-129">-ChefServerUrl</span></span>
<span data-ttu-id="6f066-130">요리사 서버 링크를 URL로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="6f066-131">-ClientRb</span></span>
<span data-ttu-id="6f066-132">요리사 클라이언트. rb의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-133">-데몬</span><span class="sxs-lookup"><span data-stu-id="6f066-133">-Daemon</span></span>
<span data-ttu-id="6f066-134">무인 실행을 요리사 클라이언트 서비스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="6f066-135">노드 플랫폼은 Windows 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-135">The node platform should be Windows.</span></span>
<span data-ttu-id="6f066-136">허용 되는 옵션: ' 없음 ', ' 서비스 ' 및 ' 작업 '.</span><span class="sxs-lookup"><span data-stu-id="6f066-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="6f066-137">없음-현재 요리사-클라이언트 서비스가 서비스로 구성 되는 것을 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="6f066-138">서비스-백그라운드에서 서비스로 자동 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="6f066-139">작업-secheduled 작업으로 백그라운드에서 자동으로 실행 되도록 요리사 클라이언트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f066-140">-DefaultProfile</span></span>
<span data-ttu-id="6f066-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f066-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="6f066-142">-JsonAttribute</span></span>
<span data-ttu-id="6f066-143">요리사의 첫 번째 실행에 추가할 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="6f066-144">예:-JsonAttribute ' {"foo": "bar"} '</span><span class="sxs-lookup"><span data-stu-id="6f066-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="6f066-145">-Linux</span></span>
<span data-ttu-id="6f066-146">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-147">-위치</span><span class="sxs-lookup"><span data-stu-id="6f066-147">-Location</span></span>
<span data-ttu-id="6f066-148">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-149">-이름</span><span class="sxs-lookup"><span data-stu-id="6f066-149">-Name</span></span>
<span data-ttu-id="6f066-150">요리사 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="6f066-151">-OrganizationName</span></span>
<span data-ttu-id="6f066-152">요리사 확장의 조직 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-152">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f066-153">-ResourceGroupName</span></span>
<span data-ttu-id="6f066-154">가상 컴퓨터를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="6f066-155">-RunList</span></span>
<span data-ttu-id="6f066-156">요리사 노드 실행 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-156">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-157">-비밀</span><span class="sxs-lookup"><span data-stu-id="6f066-157">-Secret</span></span>
<span data-ttu-id="6f066-158">데이터 모음 항목 값을 암호화 하 고 암호를 해독 하는 데 사용 되는 암호화 키입니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="6f066-159">-SecretFile</span></span>
<span data-ttu-id="6f066-160">데이터 모음 항목 값을 암호화 하 고 해독 하는 데 사용 되는 암호화 키가 포함 된 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6f066-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="6f066-162">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="6f066-163">-ValidationClientName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="6f066-164">-ValidationPem</span></span>
<span data-ttu-id="6f066-165">요리사 유효성 검사기. pem 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-165">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f066-166">-VMName</span></span>
<span data-ttu-id="6f066-167">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6f066-168">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 요리사 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="6f066-169">-Windows</span></span>
<span data-ttu-id="6f066-170">이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-171">-확인</span><span class="sxs-lookup"><span data-stu-id="6f066-171">-Confirm</span></span>
<span data-ttu-id="6f066-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f066-173">-WhatIf</span></span>
<span data-ttu-id="6f066-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6f066-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f066-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f066-176">CommonParameters</span></span>
<span data-ttu-id="6f066-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f066-178">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f066-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f066-179">입력</span><span class="sxs-lookup"><span data-stu-id="6f066-179">INPUTS</span></span>

### <span data-ttu-id="6f066-180">않아야</span><span class="sxs-lookup"><span data-stu-id="6f066-180">None</span></span>
<span data-ttu-id="6f066-181">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f066-182">출력</span><span class="sxs-lookup"><span data-stu-id="6f066-182">OUTPUTS</span></span>

### <span data-ttu-id="6f066-183">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="6f066-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6f066-184">상속자</span><span class="sxs-lookup"><span data-stu-id="6f066-184">NOTES</span></span>

## <span data-ttu-id="6f066-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f066-185">RELATED LINKS</span></span>

[<span data-ttu-id="6f066-186">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6f066-186">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="6f066-187">제거-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="6f066-187">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)