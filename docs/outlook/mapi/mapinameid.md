---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818252"
---
# <a name="mapinameid"></a><span data-ttu-id="c259f-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="c259f-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="c259f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c259f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c259f-105">Describe una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="c259f-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c259f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="c259f-106">Header file:</span></span>  <br/> |<span data-ttu-id="c259f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c259f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a><span data-ttu-id="c259f-108">Members</span><span class="sxs-lookup"><span data-stu-id="c259f-108">Members</span></span>

 <span data-ttu-id="c259f-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="c259f-109">**lpguid**</span></span>
  
> <span data-ttu-id="c259f-110">Establece el puntero a una estructura [GUID](guid.md) definición de una propiedad determinada; Este miembro no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c259f-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="c259f-111">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c259f-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="c259f-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="c259f-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="c259f-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="c259f-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="c259f-114">Un valor definido por el cliente</span><span class="sxs-lookup"><span data-stu-id="c259f-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="c259f-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="c259f-115">**ulKind**</span></span>
  
> <span data-ttu-id="c259f-116">Valor que describe el tipo de valor en el miembro de **tipo** .</span><span class="sxs-lookup"><span data-stu-id="c259f-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="c259f-117">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c259f-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="c259f-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="c259f-118">MNID_ID</span></span> 
  
> <span data-ttu-id="c259f-119">El miembro de **tipo** contiene un valor entero que representa el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c259f-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="c259f-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="c259f-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="c259f-121">El **tipo** de miembro contiene una cadena de caracteres Unicode que representa el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c259f-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="c259f-122">**Clase**</span><span class="sxs-lookup"><span data-stu-id="c259f-122">**Kind**</span></span>
  
> <span data-ttu-id="c259f-123">Unión que describe el nombre de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="c259f-123">Union describing the name of the named property.</span></span> <span data-ttu-id="c259f-124">El nombre puede ser un valor entero, que se almacenan en **tapa**, o una cadena de caracteres Unicode, que se almacenan en **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="c259f-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c259f-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c259f-125">Remarks</span></span>

<span data-ttu-id="c259f-126">La estructura **MAPINAMEID** se usa para describir las propiedades de las propiedades con nombre que tienen identificadores más 0 x 8000.</span><span class="sxs-lookup"><span data-stu-id="c259f-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="c259f-127">Un conjunto de propiedades es una parte importante de una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="c259f-127">A property set is an important part a named property.</span></span> <span data-ttu-id="c259f-128">Por ejemplo PS_PUBLIC_STRINGS o PS_ROUTING_ADDRTYPE son conjuntos de propiedades definidos por MAPI.</span><span class="sxs-lookup"><span data-stu-id="c259f-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="c259f-129">Propiedades con nombre que los clientes puedan definir propiedades personalizadas en un espacio de nombres más grande que se encuentra disponible en el intervalo de identificadores de propiedad definida por el de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c259f-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="c259f-130">Los nombres de propiedad no se puede usar para obtener los valores de propiedad directamente; que deben en primer lugar se asignadas a identificadores de propiedad a través del método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="c259f-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="c259f-131">De determinados objetos, como mensajes, MAPI reserva un intervalo de identificadores de propiedad para las propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c259f-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="c259f-132">Por lo tanto, para estos objetos, los clientes no es necesario usar propiedades con nombre y puede guardar el asociado sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="c259f-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="c259f-133">Para obtener más información acerca de las propiedades con nombre, vea [Las propiedades con nombre](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c259f-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c259f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c259f-134">See also</span></span>



[<span data-ttu-id="c259f-135">GUID</span><span class="sxs-lookup"><span data-stu-id="c259f-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="c259f-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="c259f-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="c259f-137">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="c259f-137">MAPI Structures</span></span>](mapi-structures.md)

