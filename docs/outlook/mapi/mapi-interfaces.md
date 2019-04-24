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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346686"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="7eeb6-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="7eeb6-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="7eeb6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7eeb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7eeb6-105">La documentación de cada interfaz consta de una sección introductoria que incluye una breve descripción del propósito de la interfaz seguido de una tabla que contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7eeb6-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-106">Header file:</span></span>  <br/> |<span data-ttu-id="7eeb6-107">El archivo de encabezado en el que se define la interfaz y que debe incluirse cuando se compila el código fuente.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7eeb6-109">Objeto que expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7eeb6-111">Una lista de los componentes que proporcionan una implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-112">Called by:</span></span>  <br/> |<span data-ttu-id="7eeb6-113">Una lista de los componentes que normalmente llaman a los métodos de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7eeb6-115">GUID del identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7eeb6-117">Tipo de puntero para el objeto que expone la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-118">Modelo de transacción:</span><span class="sxs-lookup"><span data-stu-id="7eeb6-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="7eeb6-119">Para interfaces derivadas de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7eeb6-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="7eeb6-120">Si no se trata de transacciones, los cambios se aplican inmediatamente; Si se transactuó, los cambios no tendrán efecto hasta que se llame a [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="7eeb6-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="7eeb6-121">A continuación de la primera tabla hay otra tabla en la que se enumeran todos los métodos de esta interfaz en orden vtable.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="7eeb6-122">Vtable es una matriz de punteros a funciones creada por el compilador que contiene un puntero de función para cada método de un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="7eeb6-123">Los métodos se enumeran en el mismo orden en que se declaran.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="7eeb6-124">Los métodos heredados de otras interfaces no se muestran en la tabla de orden vtable, sino que se pueden usar de la misma forma que se describe en la interfaz que los define.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="7eeb6-125">Después de cada tema de la interfaz, los métodos de la interfaz se documentan en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="7eeb6-126">Para cada método, la documentación incluye una breve declaración de propósito, un bloque de sintaxis y la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="7eeb6-127">**Título**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-127">**Heading**</span></span>|<span data-ttu-id="7eeb6-128">**Content**</span><span class="sxs-lookup"><span data-stu-id="7eeb6-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7eeb6-129">Parameters</span><span class="sxs-lookup"><span data-stu-id="7eeb6-129">Parameters</span></span>  <br/> |<span data-ttu-id="7eeb6-130">Una descripción de cada parámetro del método.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eeb6-131">Return Value</span></span>  <br/> |<span data-ttu-id="7eeb6-132">Descripción de los valores únicos que puede devolver el método.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="7eeb6-133">Estos son los valores que los autores de las llamadas deben buscar en el código.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7eeb6-134">Remarks</span></span>  <br/> |<span data-ttu-id="7eeb6-135">Una descripción de por qué y cómo se usa el método.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="7eeb6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eeb6-136">See Also</span></span>  <br/> |<span data-ttu-id="7eeb6-137">Referencias cruzadas a otros temas en esta referencia.</span><span class="sxs-lookup"><span data-stu-id="7eeb6-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7eeb6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eeb6-138">See also</span></span>



[<span data-ttu-id="7eeb6-139">Referencia MAPI</span><span class="sxs-lookup"><span data-stu-id="7eeb6-139">MAPI Reference</span></span>](mapi-reference.md)

