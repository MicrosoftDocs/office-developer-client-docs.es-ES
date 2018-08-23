---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567394"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="dd09d-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="dd09d-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="dd09d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd09d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd09d-105">Disminuye el recuento de referencia, limpia y elimina por instancia global de datos para la DLL de MAPI.</span><span class="sxs-lookup"><span data-stu-id="dd09d-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd09d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="dd09d-106">Header file:</span></span>  <br/> |<span data-ttu-id="dd09d-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="dd09d-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="dd09d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="dd09d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dd09d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dd09d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dd09d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="dd09d-110">Called by:</span></span>  <br/> |<span data-ttu-id="dd09d-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="dd09d-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="dd09d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd09d-112">Parameters</span></span>

<span data-ttu-id="dd09d-113">Ninguna</span><span class="sxs-lookup"><span data-stu-id="dd09d-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="dd09d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd09d-114">Return value</span></span>

<span data-ttu-id="dd09d-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd09d-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd09d-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd09d-116">Remarks</span></span>

<span data-ttu-id="dd09d-117">Una aplicación cliente llama a la función **MAPIUninitialize** para finalizar su interacción con MAPI, comenzado con una llamada a la función [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="dd09d-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="dd09d-118">Después de llamar a **MAPIUninitialize** , no hay otras llamadas MAPI pueden estar por el cliente.</span><span class="sxs-lookup"><span data-stu-id="dd09d-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="dd09d-119">**MAPIUninitialize** disminuye el recuento de referencia, y la función **MAPIInitialize** correspondiente incrementa el recuento de referencia.</span><span class="sxs-lookup"><span data-stu-id="dd09d-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="dd09d-120">Por lo tanto, el número de llamadas a una función debe ser igual que el número de llamadas a otro.</span><span class="sxs-lookup"><span data-stu-id="dd09d-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="dd09d-121">No se puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función de Win32 **DllMain** o cualquier otra función que crea o termina subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dd09d-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="dd09d-122">Para obtener más información, vea [Uso de objetos de subprocesos](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="dd09d-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

