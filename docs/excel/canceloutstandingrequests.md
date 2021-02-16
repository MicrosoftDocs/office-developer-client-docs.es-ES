---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414721"
---
# <a name="canceloutstandingrequests"></a><span data-ttu-id="95783-103">CancelOutstandingRequests</span><span class="sxs-lookup"><span data-stu-id="95783-103">CancelOutstandingRequests</span></span>

<span data-ttu-id="95783-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="95783-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="95783-105">Informa al conector de clúster de que se ha cancelado un cálculo de Excel y, por lo tanto, todas las llamadas de función pendientes dentro de esa sesión también se pueden cancelar (y que Excel no espera devoluciones de llamada con sus resultados).</span><span class="sxs-lookup"><span data-stu-id="95783-105">Informs the cluster connector that an Excel calculation has been canceled, and therefore all pending function calls within that session may be cancelled as well (and that Excel does not expect callbacks with their results).</span></span>
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="95783-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95783-106">Parameters</span></span>

<span data-ttu-id="95783-107">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="95783-107">_SessionID_</span></span>
  
> <span data-ttu-id="95783-108">Identificador de la sesión usada por el cálculo cancelado.</span><span class="sxs-lookup"><span data-stu-id="95783-108">The ID of the session used by the canceled calculation.</span></span> <span data-ttu-id="95783-109">Este valor coincide con el valor devuelto por [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="95783-109">This value matches the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95783-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95783-110">Return value</span></span>

<span data-ttu-id="95783-111">**xlHpcRetSuccess** si el  _argumento SessionId_ es válido; **xlHpcRetInvalidSessionId** si el  _argumento SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores.</span><span class="sxs-lookup"><span data-stu-id="95783-111">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="95783-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="95783-112">Remarks</span></span>

<span data-ttu-id="95783-113">Los implementadores deben detener todos los procesos de la sesión para mejorar el rendimiento, ya que Excel descartará los resultados recibidos después de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="95783-113">Implementers should stop all processes for the session for improved performance, as any results received after this call will be discarded by Excel.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95783-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="95783-114">See also</span></span>

- [<span data-ttu-id="95783-115">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="95783-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

