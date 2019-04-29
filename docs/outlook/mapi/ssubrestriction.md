---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406328"
---
# <a name="ssubrestriction"></a><span data-ttu-id="fc987-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="fc987-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="fc987-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc987-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc987-105">Describe una restricción de subobjeto que se usa para filtrar las filas de datos adjuntos de un mensaje o la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="fc987-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc987-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fc987-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc987-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fc987-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="fc987-108">Members</span><span class="sxs-lookup"><span data-stu-id="fc987-108">Members</span></span>

 <span data-ttu-id="fc987-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="fc987-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="fc987-110">Tipo de subobjeto que sirve como destino de la restricción.</span><span class="sxs-lookup"><span data-stu-id="fc987-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="fc987-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fc987-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="fc987-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="fc987-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="fc987-113">Aplique la restricción a la tabla de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc987-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="fc987-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="fc987-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="fc987-115">Aplique la restricción a la tabla de datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fc987-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="fc987-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="fc987-116">**lpRes**</span></span>
  
> <span data-ttu-id="fc987-117">Puntero a una estructura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="fc987-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fc987-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc987-118">Remarks</span></span>

<span data-ttu-id="fc987-119">Las restricciones de subobjeto no son compatibles con todas las tablas.</span><span class="sxs-lookup"><span data-stu-id="fc987-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="fc987-120">Normalmente, solo las carpetas de contenido de carpeta y los resultados de búsqueda son compatibles con ellas.</span><span class="sxs-lookup"><span data-stu-id="fc987-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="fc987-121">Por ejemplo, las restricciones de subobjeto se usan para buscar un mensaje que tiene un tipo determinado de datos adjuntos o un destinatario.</span><span class="sxs-lookup"><span data-stu-id="fc987-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="fc987-122">Si una implementación no admite restricciones de subobjeto, devuelve MAPI_E_TOO_COMPLEX de sus métodos [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="fc987-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="fc987-123">Para obtener una descripción general del funcionamiento de las restricciones, consulte [About Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="fc987-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fc987-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="fc987-124">See also</span></span>



[<span data-ttu-id="fc987-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="fc987-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="fc987-126">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="fc987-126">MAPI Structures</span></span>](mapi-structures.md)

