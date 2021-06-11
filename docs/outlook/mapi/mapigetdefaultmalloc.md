---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438207"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="4f284-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="4f284-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="4f284-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f284-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f284-105">Recupera la dirección de la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4f284-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4f284-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4f284-106">Header file:</span></span>  <br/> |<span data-ttu-id="4f284-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4f284-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4f284-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4f284-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4f284-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4f284-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4f284-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4f284-110">Called by:</span></span>  <br/> |<span data-ttu-id="4f284-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4f284-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="4f284-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f284-112">Parameters</span></span>

<span data-ttu-id="4f284-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4f284-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="4f284-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f284-114">Return value</span></span>

<span data-ttu-id="4f284-115">La **función MAPIGetDefaultMalloc** devuelve un puntero a la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4f284-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

