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
ms.openlocfilehash: 19d20a3fb06f6a0a0671ba4bfd938da314001778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435183"
---
# <a name="stnefproblem"></a><span data-ttu-id="42ac9-103">STnefProblem</span><span class="sxs-lookup"><span data-stu-id="42ac9-103">STnefProblem</span></span>

  
  
<span data-ttu-id="42ac9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42ac9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42ac9-105">Contiene información sobre un problema de procesamiento de propiedades o atributos que se produjo durante la codificación o decodificación de una secuencia de formato de encapsulamiento neutro de transporte (TNEF).</span><span class="sxs-lookup"><span data-stu-id="42ac9-105">Contains information about a property or attribute processing problem that occurred during the encoding or decoding of a Transport Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42ac9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="42ac9-106">Header file:</span></span>  <br/> |<span data-ttu-id="42ac9-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="42ac9-107">Tnef.h</span></span>  <br/> |
   
```cpp
typedef struct _STnefProblem
{
  ULONG ulComponent;
  ULONG ulAttribute;
  ULONG ulPropTag;
  SCODE scode;
} STnefProblem;

```

## <a name="members"></a><span data-ttu-id="42ac9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="42ac9-108">Members</span></span>

 <span data-ttu-id="42ac9-109">**ulComponent**</span><span class="sxs-lookup"><span data-stu-id="42ac9-109">**ulComponent**</span></span>
  
> <span data-ttu-id="42ac9-110">Tipo de procesamiento durante el cual se produjo el problema.</span><span class="sxs-lookup"><span data-stu-id="42ac9-110">The type of processing during which the problem occurred.</span></span> <span data-ttu-id="42ac9-111">Si el problema se produjo durante el procesamiento de mensajes, el **miembro ulComponent** se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="42ac9-111">If the problem occurred during message processing, the **ulComponent** member is set to zero.</span></span> <span data-ttu-id="42ac9-112">Si el problema se produjo durante el procesamiento de datos adjuntos, **ulComponent** se establece igual al valor de PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="42ac9-112">If the problem occurred during attachment processing, **ulComponent** is set equal to the corresponding attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) value.</span></span>
    
 <span data-ttu-id="42ac9-113">**ulAttribute**</span><span class="sxs-lookup"><span data-stu-id="42ac9-113">**ulAttribute**</span></span>
  
> <span data-ttu-id="42ac9-114">Atributo asociado a la propiedad indicada por el miembro **ulPropTag** o, cuando se produce el problema de procesamiento TNEF al decodificar un bloque de encapsulación, uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="42ac9-114">Attribute associated with the property indicated by the **ulPropTag** member or, when the TNEF processing problem occurs when decoding an encapsulation block, one of the following values:</span></span> 
    
 <span data-ttu-id="42ac9-115">_attMAPIProps_</span><span class="sxs-lookup"><span data-stu-id="42ac9-115">_attMAPIProps_</span></span>
  
> <span data-ttu-id="42ac9-116">Nivel de mensaje</span><span class="sxs-lookup"><span data-stu-id="42ac9-116">Message level</span></span>
    
 <span data-ttu-id="42ac9-117">_attAttachment_</span><span class="sxs-lookup"><span data-stu-id="42ac9-117">_attAttachment_</span></span>
  
> <span data-ttu-id="42ac9-118">Nivel de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="42ac9-118">Attachment level</span></span>
    
 <span data-ttu-id="42ac9-119">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="42ac9-119">**ulPropTag**</span></span>
  
> <span data-ttu-id="42ac9-120">Etiqueta de propiedad de la propiedad que provocó el problema de procesamiento TNEF, excepto cuando el problema se produce al decodificar un bloque de encapsulación, en cuyo caso **ulPropTag** se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="42ac9-120">Property tag of the property that caused the TNEF processing problem, except when the problem occurs when decoding an encapsulation block, in which case **ulPropTag** is set to zero.</span></span> 
    
 <span data-ttu-id="42ac9-121">**scode**</span><span class="sxs-lookup"><span data-stu-id="42ac9-121">**scode**</span></span>
  
> <span data-ttu-id="42ac9-122">Valor de error que indica el problema detectado durante el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="42ac9-122">Error value indicating the problem encountered during processing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42ac9-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="42ac9-123">Remarks</span></span>

<span data-ttu-id="42ac9-124">Si no se genera una estructura **STnefProblem** durante el procesamiento de un atributo o propiedad, la aplicación puede continuar con la suposición de que el procesamiento de ese atributo o propiedad se ha hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="42ac9-124">If an **STnefProblem** structure is not generated during the processing of an attribute or property, the application can continue under the assumption that the processing of that attribute or property succeeded.</span></span> <span data-ttu-id="42ac9-125">La única excepción se produce cuando el problema se produjo durante la decodificación de un bloque de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="42ac9-125">The only exception occurs when the problem arose during decoding of an encapsulation block.</span></span> <span data-ttu-id="42ac9-126">En este caso, la decodificación del componente correspondiente al bloque se detiene y la decodificación continúa en otro componente.</span><span class="sxs-lookup"><span data-stu-id="42ac9-126">In this case, the decoding of the component corresponding to the block is stopped and decoding is continued in another component.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42ac9-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="42ac9-127">See also</span></span>



[<span data-ttu-id="42ac9-128">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="42ac9-128">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="42ac9-129">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="42ac9-129">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)


[<span data-ttu-id="42ac9-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="42ac9-130">MAPI Structures</span></span>](mapi-structures.md)

