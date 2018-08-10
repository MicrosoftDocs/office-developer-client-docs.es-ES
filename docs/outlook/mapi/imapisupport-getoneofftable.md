---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51cd838164e3de28ab33d6ab8a08a021360f3183
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817491"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="de002-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="de002-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="de002-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de002-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de002-105">Devuelve un puntero a la tabla de uso único de MAPI (una lista de plantillas que todos los libreta de direcciones de proveedores de soporte técnico para la creación de nuevos destinatarios).</span><span class="sxs-lookup"><span data-stu-id="de002-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="de002-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="de002-106">Parameters</span></span>

 <span data-ttu-id="de002-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de002-107">_ulFlags_</span></span>
  
> <span data-ttu-id="de002-108">[entrada] Una máscara de bits de indicadores que controla el tipo de las columnas de cadena.</span><span class="sxs-lookup"><span data-stu-id="de002-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="de002-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="de002-109">The following flag can be set:</span></span>
    
<span data-ttu-id="de002-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="de002-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="de002-111">Las columnas de cadena se encuentran en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="de002-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="de002-112">Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="de002-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="de002-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="de002-113">_lppTable_</span></span>
  
> <span data-ttu-id="de002-114">[out] Un puntero a un puntero a la tabla de uso único.</span><span class="sxs-lookup"><span data-stu-id="de002-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de002-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de002-115">Return value</span></span>

<span data-ttu-id="de002-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="de002-116">S_OK</span></span> 
  
> <span data-ttu-id="de002-117">En la tabla de uso único se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="de002-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de002-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de002-118">Remarks</span></span>

<span data-ttu-id="de002-119">El método **IMAPISupport::GetOneOffTable** se implementa para objetos de compatibilidad con de proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="de002-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="de002-120">Los proveedores de la libreta de direcciones, llame a **GetOneOffTable** para recuperar la lista completa de las plantillas para la creación de nuevos destinatarios.</span><span class="sxs-lookup"><span data-stu-id="de002-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="de002-121">Esta tabla incluye plantillas que admiten los proveedores de la libreta de direcciones que están activos en la sesión, así como plantillas que es compatible con MAPI.</span><span class="sxs-lookup"><span data-stu-id="de002-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="de002-122">Los destinatarios recién creados se pueden usar para enviar un mensaje o pueden agregarse a un contenedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="de002-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="de002-123">Para obtener una lista de las propiedades que componen la columna requiere establecer en las tablas de uso único, vea [Las tablas de uso único](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="de002-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="de002-124">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="de002-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="de002-125">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="de002-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="de002-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="de002-126">Notes to callers</span></span>

<span data-ttu-id="de002-127">Si se ha registrado para recibir notificaciones de los cambios realizados en esta tabla de uso único, también recibirá notificaciones de los cambios realizados en las tablas de uso único de otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="de002-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="de002-128">En función de estas notificaciones, puede admitir nuevos tipos de dirección que se agregan durante la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="de002-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de002-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="de002-129">See also</span></span>



[<span data-ttu-id="de002-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="de002-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="de002-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="de002-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="de002-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de002-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="de002-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="de002-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="de002-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="de002-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="de002-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="de002-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="de002-136">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="de002-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="de002-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="de002-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="de002-138">Tablas puntuales</span><span class="sxs-lookup"><span data-stu-id="de002-138">One-Off Tables</span></span>](one-off-tables.md)
