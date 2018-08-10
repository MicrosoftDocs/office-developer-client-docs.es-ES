---
title: STnefProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblem
api_type:
- COM
ms.assetid: 3fe651b7-0ddf-42fd-8277-9224505be1a8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8595cdb411e68f2aed3ac063b2b81965e9b4d975
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820778"
---
# <a name="stnefproblem"></a><span data-ttu-id="9a05a-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="9a05a-103">STnefProblem</span></span>

  
  
<span data-ttu-id="9a05a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9a05a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9a05a-105">Contiene información acerca de un problema de procesamiento de propiedad o un atributo que se ha producido durante la codificación o descodificación de una secuencia de formato de encapsulación neutro de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="9a05a-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a05a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9a05a-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a05a-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="9a05a-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="9a05a-108">Members</span><span class="sxs-lookup"><span data-stu-id="9a05a-108">Members</span></span>

 <span data-ttu-id="9a05a-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="9a05a-109">**ulComponent**</span></span>
  
> <span data-ttu-id="9a05a-110">El tipo de procesamiento durante el cual se produjera el problema.</span><span class="sxs-lookup"><span data-stu-id="9a05a-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="9a05a-111">Si el problema se produjo durante el procesamiento de mensajes, el miembro **ulComponent** se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="9a05a-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="9a05a-112">Si el problema se produjo durante el procesamiento de datos adjuntos, **ulComponent** se establece igual al valor de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la correspondiente de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9a05a-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="9a05a-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="9a05a-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="9a05a-114">Atributo asociado con la propiedad indicada por el miembro de **ulPropTag** o cuando se produce el problema de procesamiento de TNEF cuando una encapsulación de descodificación bloquear, uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9a05a-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="9a05a-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="9a05a-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="9a05a-116">Nivel de mensaje</span><span class="sxs-lookup"><span data-stu-id="9a05a-116">Message level</span></span>
    
 <span data-ttu-id="9a05a-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="9a05a-117">_attAttachment_</span></span>
  
> <span data-ttu-id="9a05a-118">Nivel de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="9a05a-118">Attachment level</span></span>
    
 <span data-ttu-id="9a05a-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="9a05a-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="9a05a-120">Etiqueta de la propiedad de la propiedad que ha provocado el problema de procesamiento de TNEF, excepto cuando el problema se produce cuando la descodificación de un bloque de encapsulación, en la que los casos **ulPropTag** se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="9a05a-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="9a05a-121">**SCODE**</span><span class="sxs-lookup"><span data-stu-id="9a05a-121">**scode**</span></span>
  
> <span data-ttu-id="9a05a-122">Valor de error que indica el problema detectado durante el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="9a05a-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a05a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a05a-123">Remarks</span></span>

<span data-ttu-id="9a05a-124">Si no se genera una estructura de **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación puede continuar en la suposición de que se ha realizado correctamente en el procesamiento de ese atributo o propiedad.</span><span class="sxs-lookup"><span data-stu-id="9a05a-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="9a05a-125">La única excepción se produce cuando surgió el problema durante la descodificación de un bloque de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="9a05a-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="9a05a-126">En este caso, la descodificación del componente correspondiente al bloque se ha detenido y descodificación continúa en otro componente.</span><span class="sxs-lookup"><span data-stu-id="9a05a-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a05a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a05a-127">See also</span></span>



[<span data-ttu-id="9a05a-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="9a05a-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="9a05a-129">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="9a05a-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="9a05a-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="9a05a-130">MAPI Structures</span></span>](mapi-structures.md)
