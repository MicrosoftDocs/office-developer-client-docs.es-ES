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
ms.openlocfilehash: ca3752e8f7e910994811dec85cc2f1b00e184661
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584813"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="f42b8-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f42b8-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="f42b8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f42b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f42b8-105">La documentación para cada interfaz consta de una sección introductoria que incluye una breve descripción del propósito de la interfaz seguido de una tabla que contiene la información siguiente.</span><span class="sxs-lookup"><span data-stu-id="f42b8-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f42b8-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f42b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="f42b8-107">El archivo de encabezado donde se define la interfaz de y que se debe incluir al compilar el código fuente.</span><span class="sxs-lookup"><span data-stu-id="f42b8-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="f42b8-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="f42b8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f42b8-109">El objeto que expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f42b8-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="f42b8-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="f42b8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f42b8-111">Una lista de los componentes que proporcionan una implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f42b8-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="f42b8-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f42b8-112">Called by:</span></span>  <br/> |<span data-ttu-id="f42b8-113">Una lista de los componentes que normalmente se llama a los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f42b8-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="f42b8-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="f42b8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f42b8-115">El identificador GUID de interfaz.</span><span class="sxs-lookup"><span data-stu-id="f42b8-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="f42b8-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="f42b8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f42b8-117">El tipo de puntero para el objeto que expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f42b8-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="f42b8-118">Modelo de transacciones:</span><span class="sxs-lookup"><span data-stu-id="f42b8-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="f42b8-119">Para las interfaces derivadas de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="f42b8-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="f42b8-120">Si nontransacted, los cambios surtan efecto inmediatamente; Si se negocian, cambios no tendrán efecto hasta que se llama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="f42b8-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="f42b8-121">Después de la primera tabla es otra tabla que enumera todos los métodos de esta interfaz en orden vtable.</span><span class="sxs-lookup"><span data-stu-id="f42b8-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="f42b8-122">Un vtable es una matriz de punteros a función creado por el compilador que contiene un puntero a una función para cada método de un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="f42b8-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="f42b8-123">Se enumeran los métodos en el mismo orden en que se declaran.</span><span class="sxs-lookup"><span data-stu-id="f42b8-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="f42b8-124">Métodos heredados de otras interfaces no se muestran en la tabla de orden Vtable, pero pueden usarse de la misma manera, tal como se describe en la interfaz que los define.</span><span class="sxs-lookup"><span data-stu-id="f42b8-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="f42b8-125">Después de cada tema de la interfaz, los métodos de la interfaz, a continuación, se documentan en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="f42b8-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="f42b8-126">Para cada método, la documentación incluye una instrucción breve propósito, un bloque de sintaxis y la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="f42b8-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="f42b8-127">**Encabezado**</span><span class="sxs-lookup"><span data-stu-id="f42b8-127">**Heading**</span></span>|<span data-ttu-id="f42b8-128">**Contenido**</span><span class="sxs-lookup"><span data-stu-id="f42b8-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f42b8-129">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f42b8-129">Parameters</span></span>  <br/> |<span data-ttu-id="f42b8-130">Una descripción de cada parámetro en el método.</span><span class="sxs-lookup"><span data-stu-id="f42b8-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="f42b8-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f42b8-131">Return Value</span></span>  <br/> |<span data-ttu-id="f42b8-132">Una descripción de los valores únicos que el método puede devolver.</span><span class="sxs-lookup"><span data-stu-id="f42b8-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="f42b8-133">Estos son los valores que se deben proteger los autores de llamadas para su código.</span><span class="sxs-lookup"><span data-stu-id="f42b8-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="f42b8-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f42b8-134">Remarks</span></span>  <br/> |<span data-ttu-id="f42b8-135">Una descripción de cómo y por qué se usa el método.</span><span class="sxs-lookup"><span data-stu-id="f42b8-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="f42b8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f42b8-136">See Also</span></span>  <br/> |<span data-ttu-id="f42b8-137">Referencias cruzadas a otros temas de esta referencia.</span><span class="sxs-lookup"><span data-stu-id="f42b8-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f42b8-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f42b8-138">See also</span></span>



[<span data-ttu-id="f42b8-139">Referencia MAPI</span><span class="sxs-lookup"><span data-stu-id="f42b8-139">MAPI Reference</span></span>](mapi-reference.md)

