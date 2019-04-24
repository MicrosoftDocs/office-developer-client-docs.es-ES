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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345782"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="0fce3-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="0fce3-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="0fce3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fce3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fce3-105">Recupera la dirección de la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0fce3-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fce3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0fce3-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fce3-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="0fce3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0fce3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0fce3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0fce3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fce3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0fce3-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0fce3-110">Called by:</span></span>  <br/> |<span data-ttu-id="0fce3-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0fce3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="0fce3-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fce3-112">Parameters</span></span>

<span data-ttu-id="0fce3-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0fce3-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="0fce3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0fce3-114">Return value</span></span>

<span data-ttu-id="0fce3-115">La función **MAPIGetDefaultMalloc** devuelve un puntero a la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0fce3-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

