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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 152f3032876d6473f1716afa46507196cd5ecc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820755"
---
# <a name="ssubrestriction"></a><span data-ttu-id="02cef-103">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="02cef-103">SSubRestriction</span></span>

  
  
<span data-ttu-id="02cef-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02cef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02cef-105">Describe una restricción de objetos secundarios que se usa para filtrar las filas de datos adjuntos o la tabla de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="02cef-105">Describes a sub-object restriction which is used to filter the rows of a message's attachment or recipient table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02cef-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="02cef-106">Header file:</span></span>  <br/> |<span data-ttu-id="02cef-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02cef-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a><span data-ttu-id="02cef-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="02cef-108">Members</span></span>

 <span data-ttu-id="02cef-109">**ulSubObject**</span><span class="sxs-lookup"><span data-stu-id="02cef-109">**ulSubObject**</span></span>
  
> <span data-ttu-id="02cef-110">Tipo de objeto subcaracterística para que sirva como destino para la restricción.</span><span class="sxs-lookup"><span data-stu-id="02cef-110">Type of sub-object to serve as the target for the restriction.</span></span> <span data-ttu-id="02cef-111">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="02cef-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="02cef-112">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="02cef-112">PR_MESSAGE_RECIPIENTS</span></span> 
  
> <span data-ttu-id="02cef-113">Aplicar la restricción a la tabla de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="02cef-113">Apply the restriction to a message's recipient table.</span></span> 
    
<span data-ttu-id="02cef-114">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="02cef-114">PR_MESSAGE_ATTACHMENTS</span></span> 
  
>  <span data-ttu-id="02cef-115">Aplicar la restricción a la tabla de datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="02cef-115">Apply the restriction to a message's attachment table.</span></span> 
    
 <span data-ttu-id="02cef-116">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="02cef-116">**lpRes**</span></span>
  
> <span data-ttu-id="02cef-117">Puntero a una estructura [SRestriction](srestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="02cef-117">Pointer to an [SRestriction](srestriction.md) structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="02cef-118">Notas</span><span class="sxs-lookup"><span data-stu-id="02cef-118">Remarks</span></span>

<span data-ttu-id="02cef-119">Las restricciones de los objetos secundarios no son compatibles con todas las tablas.</span><span class="sxs-lookup"><span data-stu-id="02cef-119">Sub-object restrictions are not supported by all tables.</span></span> <span data-ttu-id="02cef-120">Normalmente, las tablas de contenido de carpeta sólo y son compatibles con las carpetas de los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="02cef-120">Typically, only folder contents tables and search results folders support them.</span></span> <span data-ttu-id="02cef-121">Por ejemplo, las restricciones de los objetos secundarios se usan para encontrar un mensaje que tiene un tipo de datos adjuntos o un destinatario determinado.</span><span class="sxs-lookup"><span data-stu-id="02cef-121">For example, sub-object restrictions are used to find a message that has a particular type of attachment or recipient.</span></span> 
  
<span data-ttu-id="02cef-122">Si una implementación no es compatible con las restricciones de los objetos secundarios, devuelve MAPI_E_TOO_COMPLEX desde sus métodos [IMAPITable:: Restrict](imapitable-restrict.md) o [IMAPITable:: FindRow](imapitable-findrow.md) .</span><span class="sxs-lookup"><span data-stu-id="02cef-122">If an implementation does not support sub-object restrictions, it returns MAPI_E_TOO_COMPLEX from its [IMAPITable::Restrict](imapitable-restrict.md) or [IMAPITable::FindRow](imapitable-findrow.md) methods.</span></span> 
  
<span data-ttu-id="02cef-123">Para obtener una descripción general de cómo funcionan las restricciones, vea [Restricciones de sobre](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="02cef-123">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02cef-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="02cef-124">See also</span></span>



[<span data-ttu-id="02cef-125">SRestriction</span><span class="sxs-lookup"><span data-stu-id="02cef-125">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="02cef-126">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="02cef-126">MAPI Structures</span></span>](mapi-structures.md)

