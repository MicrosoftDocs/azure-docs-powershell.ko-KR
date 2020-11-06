---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536136"
---
# <span data-ttu-id="18fd3-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="18fd3-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="18fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="18fd3-103">API Management 서비스에 대 한 인증서를 PFX 형식으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18fd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18fd3-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18fd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="18fd3-106">**AzureRmApiManagementHostnameCertificate** CMDLET은 API Management 서비스에 대 한 PFX 형식으로 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="18fd3-107">인증서는 사용자 지정 호스트 이름 구성에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="18fd3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="18fd3-108">EXAMPLES</span></span>

### <span data-ttu-id="18fd3-109">예제 1: API Management 호스트 이름 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="18fd3-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="18fd3-110">이 명령은 프록시 사용자 지정 호스트 이름에 대 한 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="18fd3-111">변수</span><span class="sxs-lookup"><span data-stu-id="18fd3-111">PARAMETERS</span></span>

### <span data-ttu-id="18fd3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fd3-112">-DefaultProfile</span></span>
<span data-ttu-id="18fd3-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="18fd3-114">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="18fd3-114">-HostnameType</span></span>
<span data-ttu-id="18fd3-115">이 cmdlet이 인증서를 로드 하는 호스트 이름 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="18fd3-116">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-116">Valid values are:</span></span> 

- <span data-ttu-id="18fd3-117">가상본</span><span class="sxs-lookup"><span data-stu-id="18fd3-117">Proxy</span></span>
- <span data-ttu-id="18fd3-118">포탈</span><span class="sxs-lookup"><span data-stu-id="18fd3-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18fd3-119">-이름</span><span class="sxs-lookup"><span data-stu-id="18fd3-119">-Name</span></span>
<span data-ttu-id="18fd3-120">이 cmdlet이 가져오는 API 관리 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

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

### <span data-ttu-id="18fd3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18fd3-121">-PassThru</span></span>
<span data-ttu-id="18fd3-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="18fd3-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="18fd3-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="18fd3-124">-PfxPassword</span></span>
<span data-ttu-id="18fd3-125">.Pfx 인증서 파일에 대 한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-125">Specifies the password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="18fd3-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="18fd3-126">-PfxPath</span></span>
<span data-ttu-id="18fd3-127">.Pfx 인증서 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-127">Specifies the path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="18fd3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18fd3-128">-ResourceGroupName</span></span>
<span data-ttu-id="18fd3-129">API Management 배포가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="18fd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fd3-130">CommonParameters</span></span>
<span data-ttu-id="18fd3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fd3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18fd3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fd3-133">입력</span><span class="sxs-lookup"><span data-stu-id="18fd3-133">INPUTS</span></span>

### <span data-ttu-id="18fd3-134">않아야</span><span class="sxs-lookup"><span data-stu-id="18fd3-134">None</span></span>
<span data-ttu-id="18fd3-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18fd3-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18fd3-136">출력</span><span class="sxs-lookup"><span data-stu-id="18fd3-136">OUTPUTS</span></span>

### <span data-ttu-id="18fd3-137">ApiManagement. PsApiManagementHostnameCertificate/.</span><span class="sxs-lookup"><span data-stu-id="18fd3-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="18fd3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="18fd3-138">NOTES</span></span>

## <span data-ttu-id="18fd3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18fd3-139">RELATED LINKS</span></span>

[<span data-ttu-id="18fd3-140">새로운 AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="18fd3-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="18fd3-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="18fd3-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)

