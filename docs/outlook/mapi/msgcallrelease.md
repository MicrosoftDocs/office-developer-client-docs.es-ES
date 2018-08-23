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
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573190"
---
# <a name="msgcallrelease"></a><span data-ttu-id="665f2-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="665f2-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="665f2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="665f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="665f2-105">Define una función de devolución de llamada que puede liberar una interfaz **IStorage** después de la versión final de un objeto **IMessage** fundamentan con la función [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="665f2-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="665f2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="665f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="665f2-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="665f2-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="665f2-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="665f2-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="665f2-109">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="665f2-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="665f2-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="665f2-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="665f2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="665f2-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="665f2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="665f2-112">Parameters</span></span>

 <span data-ttu-id="665f2-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="665f2-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="665f2-114">[entrada] Contiene información de la aplicación que llama acerca de **la interfaz** .</span><span class="sxs-lookup"><span data-stu-id="665f2-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="665f2-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="665f2-115">_lpMessage_</span></span>
  
> <span data-ttu-id="665f2-116">[entrada] Puntero para el mensaje de nivel superior y los datos adjuntos que se han publicado.</span><span class="sxs-lookup"><span data-stu-id="665f2-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="665f2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="665f2-117">Return value</span></span>

<span data-ttu-id="665f2-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="665f2-118">None.</span></span>
  

