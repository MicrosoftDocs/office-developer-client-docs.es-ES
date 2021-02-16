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
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411683"
---
# <a name="mapinameid"></a><span data-ttu-id="a3295-103">MAPINAMEID</span><span class="sxs-lookup"><span data-stu-id="a3295-103">MAPINAMEID</span></span>

  
  
<span data-ttu-id="a3295-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3295-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3295-105">Describe una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="a3295-105">Describes a named property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3295-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a3295-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3295-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3295-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="a3295-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3295-108">Members</span></span>

 <span data-ttu-id="a3295-109">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="a3295-109">**lpguid**</span></span>
  
> <span data-ttu-id="a3295-110">Puntero a una [estructura GUID](guid.md) que define un conjunto de propiedades determinado; este miembro no puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="a3295-110">Pointer to a [GUID](guid.md) structure defining a particular property set; this member cannot be NULL.</span></span> <span data-ttu-id="a3295-111">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3295-111">Valid values are as follows:</span></span> 
    
<span data-ttu-id="a3295-112">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="a3295-112">PS_PUBLIC_STRINGS</span></span>
  
> 
    
<span data-ttu-id="a3295-113">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="a3295-113">PS_MAPI</span></span>
  
> 
    
<span data-ttu-id="a3295-114">Un valor definido por el cliente</span><span class="sxs-lookup"><span data-stu-id="a3295-114">A client-defined value</span></span>
  
> 
    
 <span data-ttu-id="a3295-115">**ulKind**</span><span class="sxs-lookup"><span data-stu-id="a3295-115">**ulKind**</span></span>
  
> <span data-ttu-id="a3295-116">Valor que describe el tipo de valor en el **miembro Kind.**</span><span class="sxs-lookup"><span data-stu-id="a3295-116">Value describing the type of value in the **Kind** member.</span></span> <span data-ttu-id="a3295-117">Los valores válidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3295-117">Valid values are as follows:</span></span> 
    
<span data-ttu-id="a3295-118">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="a3295-118">MNID_ID</span></span> 
  
> <span data-ttu-id="a3295-119">El **miembro Kind** contiene un valor entero que representa el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a3295-119">The **Kind** member contains an integer value that represents the property name.</span></span> 
    
<span data-ttu-id="a3295-120">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="a3295-120">MNID_STRING</span></span> 
  
> <span data-ttu-id="a3295-121">El **miembro Kind** contiene una cadena de caracteres Unicode que representa el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="a3295-121">The **Kind** member contains a Unicode character string representing the property name.</span></span> 
    
 <span data-ttu-id="a3295-122">**Kind**</span><span class="sxs-lookup"><span data-stu-id="a3295-122">**Kind**</span></span>
  
> <span data-ttu-id="a3295-123">Union que describe el nombre de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="a3295-123">Union describing the name of the named property.</span></span> <span data-ttu-id="a3295-124">El nombre puede ser un valor entero, almacenado en **lID** o una cadena de caracteres Unicode, almacenado en **lpwstrName**.</span><span class="sxs-lookup"><span data-stu-id="a3295-124">The name can be either an integer value, stored in **lID**, or a Unicode character string, stored in **lpwstrName**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3295-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3295-125">Remarks</span></span>

<span data-ttu-id="a3295-126">La **estructura MAPINAMEID** se usa para describir propiedades con nombre que tienen identificadores en 0x8000.</span><span class="sxs-lookup"><span data-stu-id="a3295-126">The **MAPINAMEID** structure is used to describe named properties properties that have identifiers over 0x8000.</span></span> <span data-ttu-id="a3295-127">Un conjunto de propiedades es una parte importante de una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="a3295-127">A property set is an important part a named property.</span></span> <span data-ttu-id="a3295-128">Por ejemplo PS_PUBLIC_STRINGS o PS_ROUTING_ADDRTYPE son conjuntos de propiedades definidos por MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3295-128">For example PS_PUBLIC_STRINGS or PS_ROUTING_ADDRTYPE are property sets defined by MAPI.</span></span> 
  
<span data-ttu-id="a3295-129">Las propiedades con nombre permiten a los clientes definir propiedades personalizadas en un espacio de nombres más grande del que está disponible en el intervalo de identificadores de propiedades definido por MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3295-129">Named properties enable clients to define custom properties in a larger namespace than is available in the MAPI-defined property identifier range.</span></span> <span data-ttu-id="a3295-130">Los nombres de propiedad no se pueden usar para obtener los valores de propiedad directamente; primero deben asignarse a identificadores de propiedad mediante el método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="a3295-130">Property names cannot be used to obtain property values directly; they must first be mapped to property identifiers through the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> <span data-ttu-id="a3295-131">Para objetos concretos, como mensajes, MAPI reserva un intervalo de identificadores de propiedad para propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="a3295-131">For particular objects such as messages, MAPI reserves a range of property identifiers for custom properties.</span></span> <span data-ttu-id="a3295-132">Por lo tanto, para estos objetos, los clientes no tienen que usar propiedades con nombre y pueden guardar la sobrecarga asociada.</span><span class="sxs-lookup"><span data-stu-id="a3295-132">Therefore, for these objects, clients do not have to use named properties and can save the associated overhead.</span></span> 
  
<span data-ttu-id="a3295-133">Para obtener más información acerca de las propiedades con nombre, vea [Propiedades con nombre.](mapi-named-properties.md)</span><span class="sxs-lookup"><span data-stu-id="a3295-133">For more information about named properties, see [Named Properties](mapi-named-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3295-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3295-134">See also</span></span>



[<span data-ttu-id="a3295-135">GUID</span><span class="sxs-lookup"><span data-stu-id="a3295-135">GUID</span></span>](guid.md)
  
[<span data-ttu-id="a3295-136">IMAPIProp::GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="a3295-136">IMAPIProp::GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md)


[<span data-ttu-id="a3295-137">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a3295-137">MAPI Structures</span></span>](mapi-structures.md)

