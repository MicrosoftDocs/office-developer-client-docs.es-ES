---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434476"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="63eeb-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="63eeb-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="63eeb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63eeb-105">Proporciona acceso a la tabla de proveedor del servicio de mensajes, una lista de los proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63eeb-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="63eeb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="63eeb-106">Parameters</span></span>

 <span data-ttu-id="63eeb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63eeb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="63eeb-108">[in] Máscara de bits de marcas que controla el tipo de cadenas devueltas en las columnas de la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="63eeb-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="63eeb-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="63eeb-109">The following flag can be set:</span></span>
    
<span data-ttu-id="63eeb-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63eeb-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="63eeb-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="63eeb-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="63eeb-112">Si la MAPI_UNICODE no está establecida, las columnas tienen el formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="63eeb-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="63eeb-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="63eeb-113">_lppTable_</span></span>
  
> <span data-ttu-id="63eeb-114">[salida] Puntero a un puntero a la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="63eeb-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63eeb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63eeb-115">Return value</span></span>

<span data-ttu-id="63eeb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="63eeb-116">S_OK</span></span> 
  
> <span data-ttu-id="63eeb-117">La tabla de proveedor se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="63eeb-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="63eeb-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63eeb-118">Remarks</span></span>

<span data-ttu-id="63eeb-119">El **método IProviderAdmin::GetProviderTable** recupera un puntero a la tabla de proveedor del servicio de mensajes, una tabla que MAPI mantiene que contiene información sobre cada proveedor de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63eeb-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="63eeb-120">A diferencia de la tabla de proveedor devuelta por el método [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) la tabla de proveedor devuelta por **IProviderAdmin::GetProviderTable** puede incluir filas adicionales que representen información asociada a uno o varios de los proveedores de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63eeb-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="63eeb-121">Esta información adicional se agrega al perfil con la palabra clave "Secciones" del archivo Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="63eeb-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="63eeb-122">Cuando un proveedor tiene secciones de perfil adicionales, almacena las estructuras **MAPIUID** para estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63eeb-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="63eeb-123">**PR_SERVICE_EXTRA_UIDS** se guarda en la sección perfil de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="63eeb-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="63eeb-124">Los proveedores que se han eliminado o están en uso pero que se han marcado para su eliminación, no se incluyen en la tabla de proveedores.</span><span class="sxs-lookup"><span data-stu-id="63eeb-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="63eeb-125">Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del servicio de mensajes no se reflejan en la tabla.</span><span class="sxs-lookup"><span data-stu-id="63eeb-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="63eeb-126">Si el servicio de mensajes no tiene proveedores, **IProviderAdmin::GetProviderTable** devuelve una tabla con cero filas y el S_OK valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="63eeb-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="63eeb-127">Establecer la marca MAPI_UNICODE en el _parámetro ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="63eeb-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="63eeb-128">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el [método IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="63eeb-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="63eeb-129">Para obtener una lista completa de las columnas de la tabla del proveedor, vea [Tabla del proveedor](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="63eeb-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="63eeb-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="63eeb-130">Notes to callers</span></span>

<span data-ttu-id="63eeb-131">Para recuperar las filas de una tabla de proveedor en orden de transporte, ordene la tabla por la **columna PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63eeb-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="63eeb-132">Para recuperar solo las filas que representan proveedores de servicios (sin incluir filas adicionales), limite la recuperación a las filas que tienen un valor de PT_ERROR en su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="63eeb-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="63eeb-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="63eeb-133">MFCMAPI reference</span></span>

<span data-ttu-id="63eeb-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="63eeb-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63eeb-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="63eeb-135">**File**</span></span>|<span data-ttu-id="63eeb-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="63eeb-136">**Function**</span></span>|<span data-ttu-id="63eeb-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="63eeb-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="63eeb-138">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="63eeb-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="63eeb-139">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="63eeb-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="63eeb-140">MFCMAPI usa el **método IProviderAdmin::GetProviderTable** para obtener la tabla de proveedores que se representará en un nuevo cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="63eeb-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63eeb-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="63eeb-141">See also</span></span>



[<span data-ttu-id="63eeb-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="63eeb-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="63eeb-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="63eeb-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="63eeb-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="63eeb-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="63eeb-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="63eeb-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="63eeb-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="63eeb-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="63eeb-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63eeb-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="63eeb-148">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="63eeb-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

