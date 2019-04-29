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
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412761"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="6dc00-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="6dc00-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="6dc00-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dc00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dc00-105">Devuelve un puntero a la tabla única de MAPI (una lista de plantillas que todos los proveedores de la libreta de direcciones admiten para crear nuevos destinatarios).</span><span class="sxs-lookup"><span data-stu-id="6dc00-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6dc00-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6dc00-106">Parameters</span></span>

 <span data-ttu-id="6dc00-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dc00-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6dc00-108">a Máscara de máscara de marcadores que controla el tipo de las columnas de cadena.</span><span class="sxs-lookup"><span data-stu-id="6dc00-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="6dc00-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="6dc00-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6dc00-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6dc00-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6dc00-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6dc00-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6dc00-112">Si no se establece la marca MAPI_UNICODE, las columnas de la cadena tienen formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6dc00-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="6dc00-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6dc00-113">_lppTable_</span></span>
  
> <span data-ttu-id="6dc00-114">contempla Un puntero a un puntero a la tabla de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="6dc00-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dc00-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dc00-115">Return value</span></span>

<span data-ttu-id="6dc00-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dc00-116">S_OK</span></span> 
  
> <span data-ttu-id="6dc00-117">La tabla de uso único se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6dc00-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dc00-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dc00-118">Remarks</span></span>

<span data-ttu-id="6dc00-119">El método **IMAPISupport:: GetOneOffTable** se implementa para los objetos de compatibilidad del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6dc00-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="6dc00-120">Los proveedores de la libreta de direcciones llaman a **GetOneOffTable** para recuperar la lista completa de plantillas para crear nuevos destinatarios.</span><span class="sxs-lookup"><span data-stu-id="6dc00-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="6dc00-121">En esta tabla se incluyen plantillas que admiten proveedores de libretas de direcciones activos en la compatibilidad con sesiones, así como plantillas admitidas por MAPI.</span><span class="sxs-lookup"><span data-stu-id="6dc00-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="6dc00-122">Los destinatarios recién creados pueden usarse para dirigir un mensaje o pueden agregarse a un contenedor de libretas de direcciones.</span><span class="sxs-lookup"><span data-stu-id="6dc00-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="6dc00-123">Para obtener una lista de las propiedades que conforman el conjunto de columnas necesario en las tablas de uso único, consulte [tablas de uso único](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6dc00-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="6dc00-124">La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc00-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="6dc00-125">Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc00-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6dc00-126">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6dc00-126">Notes to callers</span></span>

<span data-ttu-id="6dc00-127">Si está registrado para recibir notificaciones de cambios en esta tabla única, también recibirá notificaciones de los cambios realizados en las tablas de un solo uso de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="6dc00-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="6dc00-128">En función de estas notificaciones, puede admitir nuevos tipos de direcciones que se agregan durante la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="6dc00-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6dc00-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="6dc00-129">See also</span></span>



[<span data-ttu-id="6dc00-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6dc00-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="6dc00-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="6dc00-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="6dc00-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dc00-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="6dc00-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="6dc00-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="6dc00-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="6dc00-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="6dc00-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="6dc00-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="6dc00-136">Propiedad canónica PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="6dc00-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="6dc00-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dc00-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="6dc00-138">Tablas de un solo uso</span><span class="sxs-lookup"><span data-stu-id="6dc00-138">One-Off Tables</span></span>](one-off-tables.md)

