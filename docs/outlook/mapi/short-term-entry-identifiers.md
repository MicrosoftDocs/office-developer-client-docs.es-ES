---
title: Identificadores de entrada a corto plazo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820665"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="4f827-103">Identificadores de entrada a corto plazo</span><span class="sxs-lookup"><span data-stu-id="4f827-103">Short-term entry identifiers</span></span>

<span data-ttu-id="4f827-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f827-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f827-105">Cuando el identificador debe crearse rápidamente y no es necesario que por última vez a través de tiempo o distancia, se asigna un identificador de entrada a corto plazo por un proveedor de servicios a un objeto.</span><span class="sxs-lookup"><span data-stu-id="4f827-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="4f827-106">Se garantiza que la exclusividad de un identificador de entrada a corto plazo sólo a través de la vida de la sesión actual en la estación de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="4f827-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="4f827-107">Normalmente, un identificador de entrada a corto plazo es válido sólo hasta que se libera el objeto que lo representa.</span><span class="sxs-lookup"><span data-stu-id="4f827-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="4f827-108">Los identificadores de entrada a corto plazo se asignan a las filas en las tablas y las entradas de los cuadros de diálogo, cuando sea necesario proporcionar rápidamente los datos para la exploración.</span><span class="sxs-lookup"><span data-stu-id="4f827-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="4f827-109">Por ejemplo, los proveedores de almacén de mensajes asignan los identificadores de entrada a corto plazo a las filas de los mensajes en una tabla de contenido a los destinatarios en una tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="4f827-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="4f827-110">Los clientes pueden usar estos identificadores de entrada a corto plazo para abrir los objetos representados por las filas de tabla.</span><span class="sxs-lookup"><span data-stu-id="4f827-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="4f827-111">Sin embargo, a diferencia de los identificadores de entrada a largo plazo que pueden usarse con cualquiera de los métodos de **OpenEntry** , los identificadores de entrada a corto plazo deben usarse con el método de **OpenEntry** del contenedor.</span><span class="sxs-lookup"><span data-stu-id="4f827-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="4f827-112">Implementación de los identificadores de entrada a corto plazo</span><span class="sxs-lookup"><span data-stu-id="4f827-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="4f827-113">Las formas más comunes para implementar los identificadores de entrada a corto plazo son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f827-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="4f827-114">Hacer que los identificadores de entrada a corto plazo la misma que los identificadores a largo plazo, dejando todas las marcas no definidas.</span><span class="sxs-lookup"><span data-stu-id="4f827-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="4f827-115">Hacer que los identificadores de entrada a corto plazo distintos de los identificadores a largo plazo, configuración de todas las marcas.</span><span class="sxs-lookup"><span data-stu-id="4f827-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="4f827-116">Los clientes pueden identificar un identificador de entrada a corto plazo del segundo tipo examinando su miembro **abFlags** como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="4f827-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="4f827-117">Algunos proveedores de servicios desactive uno o más indicadores para crear los identificadores de entrada a corto plazo que tienen validez mayor.</span><span class="sxs-lookup"><span data-stu-id="4f827-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="4f827-118">Por ejemplo, los siguientes miembros **abFlags** representan los identificadores de entrada a corto plazo que se pueden usar para varios días o para varias sesiones:</span><span class="sxs-lookup"><span data-stu-id="4f827-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="4f827-119">Los clientes rápidamente adquieren, usarán y descartar los identificadores de entrada a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="4f827-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="4f827-120">La mayor parte, se pueden usar en la misma manera que los identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="4f827-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="4f827-121">Se puedan recuperar de una tabla, se pasan al método **OpenEntry** y, en comparación con el método **CompareEntryIDs** .</span><span class="sxs-lookup"><span data-stu-id="4f827-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="4f827-122">La única excepción es que nunca se devuelven desde el método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="4f827-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="4f827-123">Las propiedades devueltas desde **GetProps** siempre son identificadores de entrada a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="4f827-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f827-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="4f827-124">See also</span></span>

- [<span data-ttu-id="4f827-125">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="4f827-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

