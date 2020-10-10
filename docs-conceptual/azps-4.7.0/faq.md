---
title: FAQ(질문과 대답)
description: Azure PowerShell에 대한 질문과 대답입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90928271"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Azure PowerShell에 대한 질문과 대답

## <a name="what-is-azure-powershell"></a>Azure PowerShell이란?

Azure PowerShell은 PowerShell을 사용하여 직접 Azure 리소스를 관리할 수 있는 cmdlet 세트입니다. 2018년 12월에서는 Az PowerShell 모듈이 일반 공급되었습니다. 이제 Azure와 상호 작용하는 데 권장되는 PowerShell 모듈이 되었습니다. Az PowerShell 모듈에 대한 자세한 내용은 [새로운 Azure PowerShell Az 모듈 소개](/powershell/azure/new-azureps-module-az)를 참조하세요.

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Azure PowerShell에서 호환성이 손상되는 변경 경고 메시지를 비활성화하려면 어떻게 해야 하나요?

Azure PowerShell에서 호환성이 손상되는 변경 경고 메시지를 표시하지 않으려면 환경 변수 `SuppressAzurePowerShellBreakingChangeWarnings`를 `true`로 설정해야 합니다.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```