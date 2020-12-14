---
title: Azure Az PowerShell 모듈 소개
description: Azure와 상호 작용하는 데 권장되는 모듈이자 AzureRM PowerShell 모듈을 대체하는 Az PowerShell 모듈을 소개합니다.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: d922affd608ebfce41f9608ec82d565d6afe9f7f
ms.sourcegitcommit: 3ef9f7f6c20af98282a0499b1527c291ee54011b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/05/2020
ms.locfileid: "96617722"
---
# <a name="introducing-the-azure-az-powershell-module"></a><span data-ttu-id="dd016-103">Azure Az PowerShell 모듈 소개</span><span class="sxs-lookup"><span data-stu-id="dd016-103">Introducing the Azure Az PowerShell module</span></span>

## <a name="overview"></a><span data-ttu-id="dd016-104">개요</span><span class="sxs-lookup"><span data-stu-id="dd016-104">Overview</span></span>

<span data-ttu-id="dd016-105">Az PowerShell 모듈은 PowerShell에서 직접 Azure 리소스를 관리하기 위한 cmdlet 세트입니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-105">The Az PowerShell module is a set of cmdlets for managing Azure resources directly from PowerShell.</span></span> <span data-ttu-id="dd016-106">PowerShell은 Azure 리소스를 관리(예: CI/CD 파이프라인)하는 데 활용할 수 있는 강력한 자동화 기능을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-106">PowerShell provides powerful features for automation that can be leveraged for managing your Azure resources for examples in the context of a CI/CD pipeline.</span></span>

<span data-ttu-id="dd016-107">Az PowerShell 모듈은 AzureRM을 대체하며 Azure와 상호 작용하는 데 권장되는 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-107">The Az PowerShell module is the replacement of AzureRM and is the recommended version to use for interacting with Azure.</span></span>

<span data-ttu-id="dd016-108">다음 방법 중 하나로 Az PowerShell 모듈을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-108">You can use the Az PowerShell module with one of the following methods:</span></span>

* <span data-ttu-id="dd016-109">[PowerShellGet을 통해 Az PowerShell 모듈을 설치합니다](install-az-ps.md)(권장 옵션).</span><span class="sxs-lookup"><span data-stu-id="dd016-109">[Install the Az PowerShell module via PowerShellGet](install-az-ps.md) (recommended option).</span></span>
* <span data-ttu-id="dd016-110">[MSI를 통해 Az PowerShell 모듈을 설치합니다](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="dd016-110">[Install the Az PowerShell module with MSI](install-az-ps-msi.md).</span></span>
* <span data-ttu-id="dd016-111">[Azure Cloud Shell을 사용합니다](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="dd016-111">[Use Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>
* <span data-ttu-id="dd016-112">[Az PowerShell Docker 컨테이너를 사용합니다](azureps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="dd016-112">[Use the Az PowerShell Docker container](azureps-in-docker.md).</span></span>

## <a name="features"></a><span data-ttu-id="dd016-113">기능</span><span class="sxs-lookup"><span data-stu-id="dd016-113">Features</span></span>

<span data-ttu-id="dd016-114">Az PowerShell 모듈은 다음과 같은 이점을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-114">The Az PowerShell module features the following benefits:</span></span>

* <span data-ttu-id="dd016-115">보안 및 안정성</span><span class="sxs-lookup"><span data-stu-id="dd016-115">Security and stability</span></span>
  * <span data-ttu-id="dd016-116">토큰 캐시 암호화</span><span class="sxs-lookup"><span data-stu-id="dd016-116">Token cache encryption</span></span>
  * <span data-ttu-id="dd016-117">ADFS 2019 지원</span><span class="sxs-lookup"><span data-stu-id="dd016-117">Support for ADFS 2019</span></span>
  * <span data-ttu-id="dd016-118">중간자(man-in-the-middle) 공격을 차단하는 보안 메커니즘</span><span class="sxs-lookup"><span data-stu-id="dd016-118">Security mechanism preventing man-in-the-middle attack types</span></span>
  * <span data-ttu-id="dd016-119">연속 액세스 평가와 같은 기능 지원(2021년에 도입 예정)</span><span class="sxs-lookup"><span data-stu-id="dd016-119">Support for features like continuous access evaluation (coming in 2021)</span></span>
* <span data-ttu-id="dd016-120">모든 Azure 서비스 지원</span><span class="sxs-lookup"><span data-stu-id="dd016-120">Support for all Azure services</span></span>
  * <span data-ttu-id="dd016-121">한 모듈을 각 Azure 서비스에 사용 가능</span><span class="sxs-lookup"><span data-stu-id="dd016-121">A module is available for each Azure service</span></span>
  * <span data-ttu-id="dd016-122">AzureRM 이후 여러 버그 수정 및 API 버전 업그레이드</span><span class="sxs-lookup"><span data-stu-id="dd016-122">Multiple bug fixes and API version upgrades since AzureRM</span></span>
* <span data-ttu-id="dd016-123">추가된 여러 가지 새 기능</span><span class="sxs-lookup"><span data-stu-id="dd016-123">Several additional new capabilities</span></span>
  * <span data-ttu-id="dd016-124">Cloud Shell 및 플랫폼 간 지원</span><span class="sxs-lookup"><span data-stu-id="dd016-124">Support in Cloud Shell and cross-platform</span></span>
  * <span data-ttu-id="dd016-125">액세스 토큰을 가져와서 Azure 리소스에 액세스하는 데 사용 가능</span><span class="sxs-lookup"><span data-stu-id="dd016-125">Can get and use access token to access Azure resources</span></span>
  * <span data-ttu-id="dd016-126">이스케이프 해치 유형 작업을 위한 일반 Az cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd016-126">Generic Az cmdlet for escape hatch type operations</span></span>

> [!NOTE]
> <span data-ttu-id="dd016-127">모든 플랫폼에서 Az PowerShell과 함께 사용할 것을 권장하는 PowerShell 버전은 PowerShell 7 이상입니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-127">PowerShell 7 and later is the recommended version of PowerShell for use with Az PowerShell on all platforms.</span></span>

<span data-ttu-id="dd016-128">Az PowerShell 모듈은 .NET Standard 라이브러리를 기반으로 하며 Windows, macOS 및 Linux를 비롯한 모든 플랫폼에서 PowerShell 7 이상과 함께 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-128">The Az PowerShell module is based on the .NET Standard library and works with PowerShell 7 and later on all platforms including Windows, macOS, and Linux.</span></span> <span data-ttu-id="dd016-129">Windows PowerShell 5.1과도 호환됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-129">It's also compatible with Windows PowerShell 5.1.</span></span>

<span data-ttu-id="dd016-130">저희는 모든 플랫폼에 Azure 지원을 제공하고 모든 Az PowerShell 모듈이 모든 플랫폼에서 작동할 수 있도록 최선을 다하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-130">We're committed to bringing Azure support to all platforms and all Az PowerShell modules are cross-platforms.</span></span>

## <a name="upgrade-your-environment-to-az"></a><span data-ttu-id="dd016-131">현재 환경을 Az로 업그레이드</span><span class="sxs-lookup"><span data-stu-id="dd016-131">Upgrade your environment to Az</span></span>

<span data-ttu-id="dd016-132">PowerShell의 최신 Azure 기능을 계속 유지하려면 Az 모듈로 마이그레이션해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-132">To keep up with the latest Azure features in PowerShell, you should migrate to the Az module.</span></span> <span data-ttu-id="dd016-133">AzureRM에 대한 대체 모듈로 Az 모듈을 설치할 준비가 되지 않았으면 Az를 사용하여 실험할 수 있는 몇 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-133">If you're not ready to install the Az module as a replacement for AzureRM, you have a couple of options available to experiment with Az:</span></span>

* <span data-ttu-id="dd016-134">[Azure Cloud Shell](/azure/cloud-shell/overview)이 있는 `PowerShell` 환경을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-134">Use a `PowerShell` environment with [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span> <span data-ttu-id="dd016-135">Azure Cloud Shell은 Az 모듈이 설치되고 `Enable-AzureRM` 호환성 별칭을 사용하도록 설정된 상태로 제공되는 브라우저 기반 셸 환경입니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-135">Azure Cloud Shell is a browser-based shell environment that comes with the Az module installed and `Enable-AzureRM` compatibility aliases enabled.</span></span>
* <span data-ttu-id="dd016-136">Windows PowerShell 5.1에서 설치한 AzureRM 모듈을 그대로 두고 PowerShell 7 이상에서 Az 모듈을 설치하세요.</span><span class="sxs-lookup"><span data-stu-id="dd016-136">Keep the AzureRM module installed in Windows PowerShell 5.1 and install the Az module in PowerShell 7 or later.</span></span> <span data-ttu-id="dd016-137">Windows PowerShell 5.1과 PowerShell 7 이상은 별도의 모듈 컬렉션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-137">Windows PowerShell 5.1 and PowerShell 7 and later use separate collections of modules.</span></span> <span data-ttu-id="dd016-138">지침에 따라 [최신 버전의 PowerShell](/powershell/scripting/install/installing-powershell)을 설치한 다음, PowerShell 7 이상에서 [Az 모듈을 설치](install-az-ps.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-138">Follow the instructions to install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) and then [install the Az module](install-az-ps.md) from PowerShell 7 or later.</span></span>

<span data-ttu-id="dd016-139">기존 AzureRM 설치에서 업그레이드하려면 다음을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-139">To upgrade from an existing AzureRM install:</span></span>

1. [<span data-ttu-id="dd016-140">Azure PowerShell AzureRM 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="dd016-140">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [<span data-ttu-id="dd016-141">Azure PowerShell Az 모듈 설치</span><span class="sxs-lookup"><span data-stu-id="dd016-141">Install the Azure PowerShell Az module</span></span>](install-az-ps.md)
1. <span data-ttu-id="dd016-142">**선택 사항**: 새 명령 집합을 습득하면서 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias)를 사용하여 AzureRM cmdlet에 대한 별칭을 추가할 수 있는 호환성 모드를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-142">**OPTIONAL**: Enable compatibility mode to add aliases for AzureRM cmdlets with [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) while you become familiar with the new command set.</span></span> <span data-ttu-id="dd016-143">자세한 내용은 다음 섹션 또는 [AzureRM에서 Az로 마이그레이션 시작](migrate-from-azurerm-to-az.md)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dd016-143">For more information, see the next section or [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a><span data-ttu-id="dd016-144">기존 스크립트를 AzureRM에서 Az로 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="dd016-144">Migrate existing scripts from AzureRM to Az</span></span>

<span data-ttu-id="dd016-145">스크립트가 여전히 AzureRM 모듈을 기반으로 하는 분들을 위해 마이그레이션에 도움이 되는 다음과 같은 몇 가지 리소스를 준비해 두었습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-145">If your scripts are still based on the AzureRM module, we have several resources to help you with the migration:</span></span>

* [<span data-ttu-id="dd016-146">AzureRM에서 Az로 마이그레이션 시작</span><span class="sxs-lookup"><span data-stu-id="dd016-146">Get started with migration from AzureRM to Az</span></span>](migrate-from-azurerm-to-az.md)
* [<span data-ttu-id="dd016-147">AzureRM에서 Az 1.0.0으로의 호환성이 손상되는 변경 전체 목록</span><span class="sxs-lookup"><span data-stu-id="dd016-147">Full list of breaking changes from AzureRM to Az 1.0.0</span></span>](migrate-az-1.0.0.md)
* <span data-ttu-id="dd016-148">[Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd016-148">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span></span>

## <a name="supportability"></a><span data-ttu-id="dd016-149">지원 가능성</span><span class="sxs-lookup"><span data-stu-id="dd016-149">Supportability</span></span>

<span data-ttu-id="dd016-150">Az는 가장 최신 버전의 Azure용 PowerShell 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-150">Az is the most current PowerShell module for Azure.</span></span> <span data-ttu-id="dd016-151">문제 또는 기능 요청은 [GitHub 리포지토리](https://github.com/Azure/azure-powershell)에서 직접 기록할 수 있습니다. 또는 지원 계약을 맺은 경우에는 Microsoft 지원을 통해 기록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-151">Issues or feature requests can be logged directly on the [GitHub repository](https://github.com/Azure/azure-powershell), or via Microsoft support if you have a support contract.</span></span> <span data-ttu-id="dd016-152">기능 요청은 최신 버전의 Az에서 구현됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-152">Feature requests will be implemented in the latest version of Az.</span></span> <span data-ttu-id="dd016-153">중요한 문제는 Az의 마지막 두 개 버전에서 구현됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-153">Critical issues will be implemented on the last two versions of Az.</span></span>

<span data-ttu-id="dd016-154">AzureRM은 더 이상 새 cmdlet 또는 기능을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-154">AzureRM will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="dd016-155">그러나 AzureRM 모듈은 여전히 공식적으로 유지 관리되며 2021년 2월까지 중요한 수정이 이루어집니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-155">However, the AzureRM module is still officially maintained and will receive critical fixes through February 2021.</span></span>

## <a name="data-collection"></a><span data-ttu-id="dd016-156">데이터 수집</span><span class="sxs-lookup"><span data-stu-id="dd016-156">Data collection</span></span>

<span data-ttu-id="dd016-157">Azure PowerShell은 기본적으로 원격 분석 데이터를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-157">Azure PowerShell collects telemetry data by default.</span></span> <span data-ttu-id="dd016-158">Microsoft는 수집된 데이터를 집계하여 사용 패턴을 식별하고, 일반적인 문제를 식별하고, Azure PowerShell 환경을 개선시킵니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-158">Microsoft aggregates collected data to identify patterns of usage to identify common issues and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="dd016-159">Microsoft Azure PowerShell은 프라이빗 또는 개인 데이터를 수집하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-159">Microsoft Azure PowerShell does not collect any private or personal data.</span></span> <span data-ttu-id="dd016-160">예를 들어 사용 데이터는 성공률이 낮은 cmdlet과 같은 문제를 식별하고 작업의 우선 순위를 지정하는 데 도움이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-160">For example, the usage data helps identify issues such as cmdlets with low success and helps prioritize our work.</span></span>

<span data-ttu-id="dd016-161">이 데이터가 제공하는 인사이트가 많은 도움이 되지만, 사용 데이터를 제공하는 데 찬성하지 않는 분들도 있다는 것을 잘 알고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-161">While we appreciate the insights this data provides, we also understand that not everyone wants to send usage data.</span></span> <span data-ttu-id="dd016-162">[`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet을 사용하여 데이터 수집을 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-162">You can disable data collection with the [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) cmdlet.</span></span> <span data-ttu-id="dd016-163">[개인정보처리방침](https://privacy.microsoft.com/privacystatement)에서 자세한 내용을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd016-163">You can also read our [privacy statement](https://privacy.microsoft.com/privacystatement) to learn more.</span></span>