---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: 26bd35f59ae5e640093c1695e7caf991e1e1e956
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048497"
---
# <span data-ttu-id="7387e-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7387e-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="7387e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7387e-102">SYNOPSIS</span></span>
<span data-ttu-id="7387e-103">일괄 계정에서 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="7387e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7387e-104">SYNTAX</span></span>

### <span data-ttu-id="7387e-105">ODataFilter (기본값)</span><span class="sxs-lookup"><span data-stu-id="7387e-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7387e-106">손도장</span><span class="sxs-lookup"><span data-stu-id="7387e-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7387e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7387e-107">DESCRIPTION</span></span>
<span data-ttu-id="7387e-108">**AzBatchCertificate** Cmdlet은 *batchcontext* 매개 변수에서 지정 하는 Azure Batch 계정의 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="7387e-109">특정 인증서를 얻으려면 *ThumbprintAlgorithm* 및 *손도장* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="7387e-110">*Filter* 매개 변수를 지정 하 여 열려 있는 데이터 프로토콜 (OData) 필터와 일치 하는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="7387e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7387e-111">EXAMPLES</span></span>

### <span data-ttu-id="7387e-112">예제 1: 손도장으로 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="7387e-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="7387e-113">이 명령은 지정 된 지문이 있는 단일 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="7387e-114">인증서 지문 알고리즘은 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="7387e-115">예제 2: 필터링 된 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="7387e-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      :

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="7387e-116">이 명령은 일괄 계정에서 활성 상태의 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="7387e-117">*필터* 매개 변수는 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="7387e-118">변수</span><span class="sxs-lookup"><span data-stu-id="7387e-118">PARAMETERS</span></span>

### <span data-ttu-id="7387e-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7387e-119">-BatchContext</span></span>
<span data-ttu-id="7387e-120">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7387e-121">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7387e-122">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKey cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7387e-123">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7387e-124">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7387e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7387e-125">-DefaultProfile</span></span>
<span data-ttu-id="7387e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7387e-127">-필터</span><span class="sxs-lookup"><span data-stu-id="7387e-127">-Filter</span></span>
<span data-ttu-id="7387e-128">OData 필터 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="7387e-129">이 매개 변수를 지정 하면이 cmdlet은 필터와 일치 하는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7387e-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7387e-130">-MaxCount</span></span>
<span data-ttu-id="7387e-131">반환할 최대 인증서 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="7387e-132">0 이하의 값을 지정 하면 cmdlet은 상한을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="7387e-133">기본값은 1000입니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7387e-134">-선택</span><span class="sxs-lookup"><span data-stu-id="7387e-134">-Select</span></span>
<span data-ttu-id="7387e-135">OData select 절을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="7387e-136">이 매개 변수에 대 한 값을 지정 하 여 모든 개체 속성이 아닌 특정 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="7387e-137">-지문</span><span class="sxs-lookup"><span data-stu-id="7387e-137">-Thumbprint</span></span>
<span data-ttu-id="7387e-138">이 cmdlet이 가져오는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7387e-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="7387e-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="7387e-140">*손도장* 매개 변수를 파생 하는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="7387e-141">현재는 유효한 값만 sha1입니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7387e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7387e-142">CommonParameters</span></span>
<span data-ttu-id="7387e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7387e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7387e-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7387e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7387e-145">입력</span><span class="sxs-lookup"><span data-stu-id="7387e-145">INPUTS</span></span>

### <span data-ttu-id="7387e-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7387e-146">System.String</span></span>

### <span data-ttu-id="7387e-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7387e-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7387e-148">출력</span><span class="sxs-lookup"><span data-stu-id="7387e-148">OUTPUTS</span></span>

### <span data-ttu-id="7387e-149">Microsoft.Azure.Commands.Batch. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="7387e-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="7387e-150">상속자</span><span class="sxs-lookup"><span data-stu-id="7387e-150">NOTES</span></span>

## <span data-ttu-id="7387e-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7387e-151">RELATED LINKS</span></span>

[<span data-ttu-id="7387e-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7387e-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7387e-153">새로운 AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7387e-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="7387e-154">제거-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7387e-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="7387e-155">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7387e-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)