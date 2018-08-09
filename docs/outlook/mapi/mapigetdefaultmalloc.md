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
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818244"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="26ae5-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="26ae5-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="26ae5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="26ae5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="26ae5-105">Recupera la dirección de la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26ae5-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26ae5-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="26ae5-106">Header file:</span></span>  <br/> |<span data-ttu-id="26ae5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="26ae5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="26ae5-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="26ae5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="26ae5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="26ae5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="26ae5-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="26ae5-110">Called by:</span></span>  <br/> |<span data-ttu-id="26ae5-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="26ae5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="26ae5-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26ae5-112">Parameters</span></span>

<span data-ttu-id="26ae5-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="26ae5-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="26ae5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26ae5-114">Return value</span></span>

<span data-ttu-id="26ae5-115">La función **MAPIGetDefaultMalloc** devuelve un puntero a la función de asignación de memoria MAPI predeterminada.</span><span class="sxs-lookup"><span data-stu-id="26ae5-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

