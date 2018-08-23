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
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592335"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="7b3eb-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="7b3eb-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="7b3eb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b3eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b3eb-105">Recupera la dirección de la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b3eb-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b3eb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7b3eb-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b3eb-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7b3eb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7b3eb-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="7b3eb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b3eb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b3eb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b3eb-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7b3eb-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b3eb-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="7b3eb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="7b3eb-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b3eb-112">Parameters</span></span>

<span data-ttu-id="7b3eb-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b3eb-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="7b3eb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b3eb-114">Return value</span></span>

<span data-ttu-id="7b3eb-115">La función **MAPIGetDefaultMalloc** devuelve un puntero a la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b3eb-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

