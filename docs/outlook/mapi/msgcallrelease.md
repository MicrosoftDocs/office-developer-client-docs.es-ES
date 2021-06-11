---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405915"
---
# <a name="msgcallrelease"></a><span data-ttu-id="e6803-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="e6803-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="e6803-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6803-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6803-105">Define una función de devolución de llamada que puede liberar una interfaz **IStorage** después de la versión final de un objeto **IMessage** integrado en ella con la función [OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="e6803-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6803-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="e6803-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6803-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="e6803-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e6803-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="e6803-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="e6803-109">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="e6803-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="e6803-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="e6803-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="e6803-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6803-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="e6803-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6803-112">Parameters</span></span>

 <span data-ttu-id="e6803-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="e6803-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="e6803-114">[in] Contiene información de aplicación de llamada sobre la **interfaz IMessage.**</span><span class="sxs-lookup"><span data-stu-id="e6803-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="e6803-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="e6803-115">_lpMessage_</span></span>
  
> <span data-ttu-id="e6803-116">[in] Puntero al mensaje de nivel superior y a los datos adjuntos que se han liberado.</span><span class="sxs-lookup"><span data-stu-id="e6803-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6803-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6803-117">Return value</span></span>

<span data-ttu-id="e6803-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e6803-118">None.</span></span>
  

