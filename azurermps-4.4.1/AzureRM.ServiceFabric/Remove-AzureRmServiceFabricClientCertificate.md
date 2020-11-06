---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d0ba19efaf0cf3dc1f997d06231e056fb20b02f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529135"
---
# <span data-ttu-id="9ba2f-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9ba2f-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="9ba2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba2f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba2f-103">클라이언트 인증에 사용 되지 않는 클라이언트 인증서 또는 인증서 주체 이름 (s)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ba2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ba2f-104">SYNTAX</span></span>

### <span data-ttu-id="9ba2f-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="9ba2f-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba2f-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba2f-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba2f-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="9ba2f-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ba2f-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba2f-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba2f-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9ba2f-109">DESCRIPTION</span></span>
<span data-ttu-id="9ba2f-110">**AzureRmServiceFabricClientCertificate** 을 사용 하 여 클라이언트 인증에 사용 되는 클라이언트 인증서 또는 인증서 주체 이름 (예: 클러스터)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="9ba2f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9ba2f-111">EXAMPLES</span></span>

### <span data-ttu-id="9ba2f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ba2f-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="9ba2f-113">이 명령은 클러스터에서 지문이 ' 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A ' 인 클라이언트 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="9ba2f-114">변수</span><span class="sxs-lookup"><span data-stu-id="9ba2f-114">PARAMETERS</span></span>

### <span data-ttu-id="9ba2f-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba2f-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="9ba2f-116">관리자 권한만 있는 클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-116">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="9ba2f-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="9ba2f-118">클라이언트 일반 이름, 발급자 지문, 인증 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="9ba2f-119">-CommonName</span></span>
<span data-ttu-id="9ba2f-120">클라이언트 인증서 일반 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-120">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-121">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba2f-121">-IssuerThumbprint</span></span>
<span data-ttu-id="9ba2f-122">클라이언트 인증서 발급자 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-122">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9ba2f-123">-Name</span></span>
<span data-ttu-id="9ba2f-124">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-125">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="9ba2f-125">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="9ba2f-126">읽기 전용 권한이 있는 클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-126">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba2f-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ba2f-128">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9ba2f-129">-지문</span><span class="sxs-lookup"><span data-stu-id="9ba2f-129">-Thumbprint</span></span>
<span data-ttu-id="9ba2f-130">클라이언트 인증서 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-130">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="9ba2f-131">-Confirm</span></span>
<span data-ttu-id="9ba2f-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba2f-133">-WhatIf</span></span>
<span data-ttu-id="9ba2f-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ba2f-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba2f-136">-DefaultProfile</span></span>
<span data-ttu-id="9ba2f-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ba2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba2f-138">CommonParameters</span></span>
<span data-ttu-id="9ba2f-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba2f-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ba2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba2f-141">입력</span><span class="sxs-lookup"><span data-stu-id="9ba2f-141">INPUTS</span></span>

### <span data-ttu-id="9ba2f-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="9ba2f-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="9ba2f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ba2f-143">System.String</span></span>

<span data-ttu-id="9ba2f-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9ba2f-144">System.Boolean</span></span>

## <span data-ttu-id="9ba2f-145">출력</span><span class="sxs-lookup"><span data-stu-id="9ba2f-145">OUTPUTS</span></span>

### <span data-ttu-id="9ba2f-146">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="9ba2f-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="9ba2f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="9ba2f-147">NOTES</span></span>

## <span data-ttu-id="9ba2f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba2f-148">RELATED LINKS</span></span>

[<span data-ttu-id="9ba2f-149">추가-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9ba2f-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)