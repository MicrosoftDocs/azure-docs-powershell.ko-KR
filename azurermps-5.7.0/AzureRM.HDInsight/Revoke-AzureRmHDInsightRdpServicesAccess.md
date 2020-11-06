---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532836"
---
# <span data-ttu-id="530e2-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="530e2-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="530e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="530e2-102">SYNOPSIS</span></span>
<span data-ttu-id="530e2-103">Windows 클러스터에 대 한 RDP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="530e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="530e2-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="530e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="530e2-105">DESCRIPTION</span></span>
<span data-ttu-id="530e2-106">**AzureRmHDInsightRdpServicesAccess** Cmdlet은 Windows 기반 Azure HDInsight 클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="530e2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="530e2-107">EXAMPLES</span></span>

### <span data-ttu-id="530e2-108">예제 1: 지정 된 클러스터에 대 한 RDP 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="530e2-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="530e2-109">이 명령은-hadoop-001 이라는 클러스터에 대 한 RDP 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="530e2-110">변수</span><span class="sxs-lookup"><span data-stu-id="530e2-110">PARAMETERS</span></span>

### <span data-ttu-id="530e2-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="530e2-111">-ClusterName</span></span>
<span data-ttu-id="530e2-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="530e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530e2-113">-DefaultProfile</span></span>
<span data-ttu-id="530e2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="530e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="530e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="530e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="530e2-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="530e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530e2-117">CommonParameters</span></span>
<span data-ttu-id="530e2-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530e2-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="530e2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530e2-120">입력</span><span class="sxs-lookup"><span data-stu-id="530e2-120">INPUTS</span></span>

### <span data-ttu-id="530e2-121">않아야</span><span class="sxs-lookup"><span data-stu-id="530e2-121">None</span></span>
<span data-ttu-id="530e2-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="530e2-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="530e2-123">출력</span><span class="sxs-lookup"><span data-stu-id="530e2-123">OUTPUTS</span></span>

### <span data-ttu-id="530e2-124">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="530e2-124">System.Void</span></span>

## <span data-ttu-id="530e2-125">상속자</span><span class="sxs-lookup"><span data-stu-id="530e2-125">NOTES</span></span>

## <span data-ttu-id="530e2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="530e2-126">RELATED LINKS</span></span>

[<span data-ttu-id="530e2-127">부여-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="530e2-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)

