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
ms.openlocfilehash: de92a1328eb9a089a7914978ab20ab0bf5c430ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581961"
---
# <a name="ssubrestriction"></a><span data-ttu-id="b0cf9-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="b0cf9-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="b0cf9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0cf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0cf9-105">Describe una restricción de objetos secundarios que se usa para filtrar las filas de datos adjuntos o la tabla de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0cf9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b0cf9-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0cf9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0cf9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="b0cf9-108">Members</span><span class="sxs-lookup"><span data-stu-id="b0cf9-108">Members</span></span>

 <span data-ttu-id="b0cf9-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="b0cf9-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="b0cf9-110">Tipo de objeto subcaracterística para que sirva como destino para la restricción.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="b0cf9-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b0cf9-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="b0cf9-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="b0cf9-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="b0cf9-113">Aplicar la restricción a la tabla de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="b0cf9-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="b0cf9-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="b0cf9-115">Aplicar la restricción a la tabla de datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="b0cf9-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="b0cf9-116">**lpRes**</span></span>
  
> <span data-ttu-id="b0cf9-117">Puntero a una estructura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="b0cf9-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b0cf9-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0cf9-118">Remarks</span></span>

<span data-ttu-id="b0cf9-119">Las restricciones de los objetos secundarios no son compatibles con todas las tablas.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="b0cf9-120">Normalmente, las tablas de contenido de carpeta sólo y son compatibles con las carpetas de los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="b0cf9-121">Por ejemplo, las restricciones de los objetos secundarios se usan para encontrar un mensaje que tiene un tipo de datos adjuntos o un destinatario determinado.</span><span class="sxs-lookup"><span data-stu-id="b0cf9-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="b0cf9-122">Si una implementación no es compatible con las restricciones de los objetos secundarios, devuelve MAPI_E_TOO_COMPLEX desde sus métodos [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="b0cf9-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="b0cf9-123">Para obtener una descripción general de cómo funcionan las restricciones, vea [Restricciones de sobre](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="b0cf9-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0cf9-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b0cf9-124">See also</span></span>



[<span data-ttu-id="b0cf9-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="b0cf9-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="b0cf9-126">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="b0cf9-126">MAPI Structures</span></span>](mapi-structures.md)

