---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815519"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="3e329-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="3e329-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="3e329-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3e329-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3e329-105">Informa el conector de clúster que se ha cancelado un cálculo de Excel y, por lo tanto, todos los pendientes llamadas a la función dentro de esa sesión es posible que se puede cancelar así como (y que Excel no espera las devoluciones de llamada con sus resultados).</span><span class="sxs-lookup"><span data-stu-id="3e329-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="3e329-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e329-106">Parameters</span></span>

<span data-ttu-id="3e329-107">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="3e329-107">_SessionID_</span></span>
  
> <span data-ttu-id="3e329-108">El identificador de la sesión usado por el cálculo cancelado.</span><span class="sxs-lookup"><span data-stu-id="3e329-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="3e329-109">Este valor coincide con el valor devuelto por [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="3e329-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e329-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e329-110">Return value</span></span>

<span data-ttu-id="3e329-111">**xlHpcRetSuccess** si el argumento de _SessionId_ es válido; **xlHpcRetInvalidSessionId** si el argumento de _SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores.</span><span class="sxs-lookup"><span data-stu-id="3e329-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3e329-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3e329-112">Remarks</span></span>

<span data-ttu-id="3e329-113">Los implementadores deben detener todos los procesos de la sesión para mejorar el rendimiento, como los resultados recibidos después de esta llamada se descartarán por Excel.</span><span class="sxs-lookup"><span data-stu-id="3e329-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3e329-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e329-114">See also</span></span>

- [<span data-ttu-id="3e329-115">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="3e329-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

