---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: f05cae3484067f227fde8f30cd7806307832b185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527568"
---
# <span data-ttu-id="a102f-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a102f-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="a102f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a102f-102">SYNOPSIS</span></span>
<span data-ttu-id="a102f-103">Windows 클러스터에 대 한 RDP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a102f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a102f-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a102f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a102f-105">DESCRIPTION</span></span>
<span data-ttu-id="a102f-106">**AzureRmHDInsightRdpServicesAccess** Cmdlet은 Windows 기반 Azure HDInsight 클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a102f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a102f-107">EXAMPLES</span></span>

### <span data-ttu-id="a102f-108">예제 1: 지정 된 클러스터에 대 한 RDP 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a102f-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a102f-109">이 명령은-hadoop-001 이라는 클러스터에 대 한 RDP 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a102f-110">변수</span><span class="sxs-lookup"><span data-stu-id="a102f-110">PARAMETERS</span></span>

### <span data-ttu-id="a102f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a102f-111">-ClusterName</span></span>
<span data-ttu-id="a102f-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a102f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a102f-113">-ResourceGroupName</span></span>
<span data-ttu-id="a102f-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a102f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a102f-115">-DefaultProfile</span></span>
<span data-ttu-id="a102f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a102f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a102f-117">CommonParameters</span></span>
<span data-ttu-id="a102f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a102f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a102f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a102f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a102f-120">입력</span><span class="sxs-lookup"><span data-stu-id="a102f-120">INPUTS</span></span>

## <span data-ttu-id="a102f-121">출력</span><span class="sxs-lookup"><span data-stu-id="a102f-121">OUTPUTS</span></span>

### <span data-ttu-id="a102f-122">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="a102f-122">System.Void</span></span>

## <span data-ttu-id="a102f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="a102f-123">NOTES</span></span>

## <span data-ttu-id="a102f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a102f-124">RELATED LINKS</span></span>

[<span data-ttu-id="a102f-125">부여-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a102f-125">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)

