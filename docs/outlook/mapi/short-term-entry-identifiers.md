---
title: Identificadores de entrada a corto plazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439565"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="e6843-103">Identificadores de entrada a corto plazo</span><span class="sxs-lookup"><span data-stu-id="e6843-103">Short-term entry identifiers</span></span>

<span data-ttu-id="e6843-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6843-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6843-105">Un proveedor de servicios asigna un identificador de entrada a corto plazo a un objeto cuando el identificador debe construirse rápidamente y no es necesario que dure con el tiempo o la distancia.</span><span class="sxs-lookup"><span data-stu-id="e6843-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="e6843-106">La singularidad de un identificador de entrada a corto plazo solo se garantiza durante la vida de la sesión actual en la estación de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="e6843-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="e6843-107">Normalmente, un identificador de entrada a corto plazo solo es válido hasta que se libera el objeto que representa.</span><span class="sxs-lookup"><span data-stu-id="e6843-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="e6843-108">Los identificadores de entrada a corto plazo se asignan a las filas de las tablas y a las entradas de los cuadros de diálogo, donde es necesario proporcionar datos rápidamente para la exploración.</span><span class="sxs-lookup"><span data-stu-id="e6843-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="e6843-109">Por ejemplo, los proveedores de almacenes de mensajes asignan identificadores de entrada a corto plazo a filas de mensajes de una tabla de contenido y a destinatarios de una tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e6843-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="e6843-110">Los clientes pueden usar estos identificadores de entrada a corto plazo para abrir los objetos representados por las filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="e6843-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="e6843-111">Sin embargo, a diferencia de los identificadores de entrada a largo plazo que se pueden usar con cualquiera de los métodos **OpenEntry,** los identificadores de entrada a corto plazo deben usarse con el método **OpenEntry del** contenedor.</span><span class="sxs-lookup"><span data-stu-id="e6843-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="e6843-112">Implementación de identificadores de entrada a corto plazo</span><span class="sxs-lookup"><span data-stu-id="e6843-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="e6843-113">Las formas más comunes de implementar identificadores de entrada a corto plazo son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="e6843-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="e6843-114">Hacer que los identificadores de entrada a corto plazo sea igual que los identificadores a largo plazo, dejando todas las marcas sin marcar.</span><span class="sxs-lookup"><span data-stu-id="e6843-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="e6843-115">Hacer que los identificadores de entrada a corto plazo se diferencian de los identificadores a largo plazo, estableciendo todas las marcas.</span><span class="sxs-lookup"><span data-stu-id="e6843-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="e6843-116">Los clientes pueden identificar un identificador de entrada a corto plazo del segundo tipo examinando su **miembro abFlags** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e6843-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="e6843-117">Algunos proveedores de servicios borran una o más marcas para crear identificadores de entrada a corto plazo con mayor validez.</span><span class="sxs-lookup"><span data-stu-id="e6843-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="e6843-118">Por ejemplo, los siguientes **miembros abFlags** representan identificadores de entrada a corto plazo que se pueden usar durante varios días o para varias sesiones:</span><span class="sxs-lookup"><span data-stu-id="e6843-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="e6843-119">Los clientes adquieren, usan y descartan rápidamente identificadores de entrada a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="e6843-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="e6843-120">En su mayoría, se pueden usar de la misma manera que los identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="e6843-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="e6843-121">Se pueden recuperar de una tabla, pasar al método **OpenEntry** y compararlos con el **método CompareEntryIDs.**</span><span class="sxs-lookup"><span data-stu-id="e6843-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="e6843-122">La única excepción es que nunca se devuelven desde el [método IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="e6843-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="e6843-123">Las propiedades **devueltas de GetProps** siempre son identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="e6843-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6843-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6843-124">See also</span></span>

- [<span data-ttu-id="e6843-125">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="e6843-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

