---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422666"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="2c0d0-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2c0d0-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="2c0d0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c0d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c0d0-105">La documentación de cada interfaz consta de una sección introductoria que incluye una breve descripción del propósito de la interfaz seguida de una tabla que contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c0d0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-106">Header file:</span></span>  <br/> |<span data-ttu-id="2c0d0-107">El archivo de encabezado donde se define la interfaz y que debe incluirse al compilar el código fuente.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="2c0d0-109">Objeto que expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2c0d0-111">Una lista de los componentes que proporcionan una implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-112">Called by:</span></span>  <br/> |<span data-ttu-id="2c0d0-113">Una lista de los componentes que normalmente llaman a los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2c0d0-115">GUID del identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="2c0d0-117">Tipo de puntero para el objeto que expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="2c0d0-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="2c0d0-119">Para interfaces derivadas de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="2c0d0-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="2c0d0-120">Si no se transduce, los cambios se realizarán inmediatamente; si se realiza una transacción, los cambios no tienen efecto hasta que se llama a [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="2c0d0-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="2c0d0-121">Después de la primera tabla hay otra tabla que enumera todos los métodos de esta interfaz en orden vtable.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="2c0d0-122">Una tabla virtual es una matriz de punteros de función creada por el compilador que contiene un puntero de función para cada método de un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="2c0d0-123">Los métodos se enumeran en el mismo orden en que se declaran.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="2c0d0-124">Los métodos heredados de otras interfaces no se muestran en la tabla Orden de tabla Vtable, pero se pueden usar de la misma manera que se documenta en la interfaz que las define.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="2c0d0-125">Después de cada tema de interfaz, los métodos de la interfaz se documentan en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="2c0d0-126">Para cada método, la documentación incluye una instrucción de propósito breve, un bloque de sintaxis y la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="2c0d0-127">**Título**</span><span class="sxs-lookup"><span data-stu-id="2c0d0-127">**Heading**</span></span>|<span data-ttu-id="2c0d0-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="2c0d0-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c0d0-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="2c0d0-129">Parameters</span></span>  <br/> |<span data-ttu-id="2c0d0-130">Una descripción de cada parámetro del método.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c0d0-131">Return Value</span></span>  <br/> |<span data-ttu-id="2c0d0-132">Una descripción de los valores únicos que el método puede devolver.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="2c0d0-133">Estos son los valores que los autores de llamadas deben comprobar en su código.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c0d0-134">Remarks</span></span>  <br/> |<span data-ttu-id="2c0d0-135">Una descripción de por qué y cómo se usa el método.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="2c0d0-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c0d0-136">See Also</span></span>  <br/> |<span data-ttu-id="2c0d0-137">Referencias cruzadas a otros temas de esta referencia.</span><span class="sxs-lookup"><span data-stu-id="2c0d0-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c0d0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c0d0-138">See also</span></span>



[<span data-ttu-id="2c0d0-139">Referencia MAPI</span><span class="sxs-lookup"><span data-stu-id="2c0d0-139">MAPI Reference</span></span>](mapi-reference.md)

